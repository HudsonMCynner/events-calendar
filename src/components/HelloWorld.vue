<template>
  <div class="calendar-wrapper ">
    <div
      id="divCal"
    >
      <div class="table-title">
        <div class="legend">
          <label
            class="legend-situacao sub-title"
            style="width: 70px; font-size: 12px;"
          >Legenda: </label>
          <label class="legend-situacao confirmed">CONFIRMADO </label>
          <label class="legend-situacao marked">AGENDADO </label>
          <label class="legend-situacao relocated">REALOCADO </label>
          <label class="legend-situacao caceled">CANCELADO </label>
        </div>
        <q-select
          class="select-years"
          @input="selectYear"
          :value="currYear"
          :options="anos"
        />
        <q-select
          class="select-month"
          @input="selectMonth"
          :value="currMonth + 1"
          :options="meses"
        />
        <span class="btn-calendar btn-reset">
          <q-btn
            @click="currentDate"
            dense
            flat
            round
          >
            <q-tooltip>
              {{ tooltipReset }}
            </q-tooltip>
            <q-icon name="fas fa-undo" />
          </q-btn>
        </span>
      </div>
      <table
        class="table-calendar"
      >
        <thead>
        <tr class="days">
          <td
            v-for="(day, index) in diasDaSemana"
            :key="index"
          >
            {{ day.nome }}
          </td>
        </tr>
        </thead>
        <tbody>
        <template v-for="(semana, indexSemana) in semanas">
          <tr
            v-if="semana.length > 0"
            :key="indexSemana"
          >
            <td
              :ref="'events'+dia.data"
              v-for="(dia, indexDia) in semana"
              :key="indexDia"
              style="position: relative"
              :class="[{ 'diaSelecionado': dataSelecionada === dia.data}, dia.class]"
              @click="click(dia, 'click')"
              @dblclick="click(dia, 'dbClick')"
            >
                <span class="dia-numero">
                  {{ dia.dia }}
                </span>
              <div
                @dragenter.prevent="dragEnter($event ,dia, 'events'+dia.data)"
                @dragleave.prevent="dragLeave($event ,dia, 'events'+dia.data)"
                @dragend="dragEnd(dia)"
                class="lista-agenda"
              >
                <div
                  v-for="(agendamento, indexAgenda) in dia.agenda.agendamentos"
                  :draggable="agendamento.situacao === 'CONFIRMADO' || agendamento.situacao === 'AGENDADO'"
                  @dragstart="dragStart($event ,indexAgenda, indexDia, indexSemana)"
                  :key="indexAgenda"
                  class="agendamento"
                  :class="getClasseSituacao(agendamento.situacao)"
                >
                  <a>{{ agendamento.profissional.nome }} - Aula {{ agendamento.aula }} - {{ agendamento.turno.descricao.substring(0, 3) }}</a>
                </div>
              </div>
            </td>
          </tr>
        </template>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>

export default {
  name: 'LancamentoFaltaConteudoListaTurmas',
  components: {},
  props: {
    value: {
      type: Array,
      default: () => ([])
    },
    tooltipReset: {
      type: String,
      default: () => ('Data Atual')
    },
    dataAtual: {
      type: String,
      default: () => (new Date().toLocaleDateString('pt-BR'))
    }
  },
  created () {
    this.dias = this.value
    this.currDay = parseInt(this.dataAtual.split('/')[0])
    this.currMonth = parseInt(this.dataAtual.split('/')[1]) - 1
    this.currYear = parseInt(this.dataAtual.split('/')[2])
    this.currentDate()
  },
  watch: {
    value: {
      handler (dias) {
        this.dias = dias
        this.showcurr()
      },
      deep: true
    },
    dataAtual: {
      handler (data) {
        this.currDay = parseInt(data.split('/')[0])
        this.currMonth = parseInt(data.split('/')[1]) - 1
        this.currYear = parseInt(data.split('/')[2])
      }
    }
  },
  data () {
    return {
      dias: [],
      anos: [],
      dragDropDataTemp: {},
      dradEnter: null,
      diasDaSemana: [
        {
          nome: 'Domingo',
          sigla: 'Dom'
        },
        {
          nome: 'Segunda-Feira',
          sigla: 'Seg'
        },
        {
          nome: 'Terça-Feira',
          sigla: 'Ter'
        },
        {
          nome: 'Quarta-Feira',
          sigla: 'Qua'
        },
        {
          nome: 'Quinta-Feira',
          sigla: 'Qui'
        },
        {
          nome: 'Sexta-Feira',
          sigla: 'Sex'
        },
        {
          nome: 'Sábado',
          sigla: 'Sáb'
        }],
      meses: [
        {
          label: 'Janeiro',
          value: 1
        },
        {
          label: 'Fevereiro',
          value: 2
        },
        {
          label: 'Março',
          value: 3
        },
        {
          label: 'Abril',
          value: 4
        },
        {
          label: 'Maio',
          value: 5
        },
        {
          label: 'Junho',
          value: 6
        },
        {
          label: 'Julho',
          value: 7
        },
        {
          label: 'Agosto',
          value: 8
        },
        {
          label: 'Setembro',
          value: 9
        },
        {
          label: 'Outubro',
          value: 10
        },
        {
          label: 'Novembro',
          value: 11
        },
        {
          label: 'Dezembro',
          value: 12
        }],
      currMonth: '',
      currYear: '',
      currDay: '',
      semanas: [],
      mesAnoSelecionado: '',
      dataSelecionada: ''

    }
  },
  methods: {
    getClasseSituacao (situacao) {
      switch (situacao) {
        case 'CANCELADO': return 'caceled'
        case 'REALOCADO': return 'relocated'
        case 'CONFIRMADO': return 'confirmed draggable'
        case 'AGENDADO': return 'marked draggable'
      }
    },
    dragEnter (event, data, ref) {
      let element = this.$util.ref(ref)
      element.classList.add('hovered')
      this.dradEnter = data
    },
    dragLeave (event, data, ref) {
      let element = this.$util.ref(ref)
      element.classList.remove('hovered')
    },
    dragStart (event, indexAgenda, indexDia, indexSemana) {
      this.dragDropDataTemp['evento'] = this.semanas[indexSemana][indexDia].agenda.agendamentos[indexAgenda]
      this.dragDropDataTemp['indexDia'] = indexDia
      this.dragDropDataTemp['indexAgenda'] = indexAgenda
      this.dragDropDataTemp['indexSemana'] = indexSemana
      this.$emit('dagStart', this.dragDropDataTemp['evento'])
    },
    dragEnd () {
      let index = this.dradEnter.agenda.agendamentos.findIndex((item) => item.id === this.dragDropDataTemp.evento.id)
      if (index === -1) {
        this.$emit('dragEnd', { evento: this.dragDropDataTemp['evento'], dataRealocacao: this.dradEnter.data })
      }
      this.dragDropDataTemp = {}
    },
    currentDate () {
      this.generateYears()
      this.currMonth = parseInt(this.dataAtual.split('/')[1]) - 1
      this.currYear = parseInt(this.dataAtual.split('/')[2])
      this.showcurr()
      this.$emit('change', { dia: this.currDay, mes: this.currMonth + 1, ano: this.currYear })
    },
    /**
       * Retorna informação da data (Nome do dia da semana, numero do dia do mes e numero do ano)
       * Ex:(Sexta-Feira, 15 de Março de 2019")
       * @param dia
       * @param mes
       * @param ano
       * @returns {string}
       */
    getDataCompleta (dia, mes, ano) {
      let novaData = new Date(ano + '/' + mes + '/' + dia)
      return this.diasDaSemana[novaData.getDay()].nome + ', ' + novaData.getDate() + ' de ' + this.meses[novaData.getMonth()].label + ' de ' + novaData.getFullYear()
    },
    click (event, eventName) {
      this.dataSelecionada = event.data
      this.$emit(eventName, { event: event, dataCompleta: this.getDataCompleta(event.dia, event.mes, event.ano), data: this.formatarCaracteres(`${event.dia}/${event.mes}/${event.ano}`) })
    },
    generateYears () {
      let years = []
      for (let i = -5; i < 6; i++) {
        years.push({ value: this.currYear + (i), label: `${this.currYear + (i)}` })
      }
      this.anos = years
    },
    selectMonth (event) {
      this.currMonth = event - 1
      this.$emit('change', { mes: event, ano: this.currYear })
      this.showcurr()
    },
    selectYear (event) {
      this.currYear = event
      this.$emit('change', { mes: this.currMonth + 1, ano: event })
      this.showcurr()
      this.generateYears()
    },
    showcurr () {
      this.montarCalendario(this.currYear, this.currMonth)
    },
    /**
       * Converte uma data no formato String
       * @param stringData
       * @param type {string} string || object
       * @returns {{ano: (*|string), mes: (*|string), dia: (*|string)}}
       */
    formatarCaracteres (stringData, type) {
      let dia = stringData.split('/')[0]
      if (dia.toString().length === 1) {
        dia = '0' + dia
      }
      let mes = stringData.split('/')[1]
      if (mes.toString().length === 1) {
        mes = '0' + mes
      }
      let ano = stringData.split('/')[2]

      if (!type) {
        return `${dia}/${mes}/${ano}`
      }
      if (type === 'object') {
        return {
          dia: dia,
          mes: mes,
          ano: ano
        }
      }
    },
    /**
       * Atribui um objeto dia ja com suas configurações ao vetor de semanas
       * @param index
       * @param dia
       * @param mes
       * @param ano
       * @param data
       * @param config
       */
    setSemana (index, dia, mes, ano, data, config) {
      this.semanas[index].push({
        class: config.class,
        dia: dia,
        mes: mes + 1,
        ano: ano,
        data: this.formatarCaracteres(data),
        agenda: config.agenda
      })
    },
    verificarDia (dia, mes, ano) {
      let evento = this.dias.find((item) => item.dia === dia && item.mes === mes && item.ano === ano)
      if (evento) {
        return { class: 'diaDeAula', agenda: evento }
      }
      return { class: 'not-current', agenda: {} }
    },
    montarCalendario (ano, mes) {
      let primeiroDiaDoMes = new Date(ano, mes, 1).getDay()
      let ultimaDataDoMes = new Date(ano, mes + 1, 0).getDate()
      let ultimoDiaDoUltimoMes = mes === 0 ? new Date(ano - 1, 11, 0).getDate() : new Date(ano, mes, 0).getDate()
      this.mesAnoSelecionado = this.meses[mes].label + ' ' + ano
      this.semanas = []
      // Write the days
      let i = 1
      let aux = -1
      do {
        let dow = new Date(ano, mes, i).getDay()
        // If Sunday, start new row
        if (dow === 0) {
          aux = this.semanas.push([]) - 1
        }
        /*
           * Se não domingo, mas primeiro dia do mês
           * vai escrever os últimos dias do mês anterior
           */
        if (i === 1) {
          aux = this.semanas.push([]) - 1
          let dia = ultimoDiaDoUltimoMes - primeiroDiaDoMes + 1
          for (let j = 0; j < primeiroDiaDoMes; j++) {
            if (aux !== -1) {
              this.setSemana(aux, dia, mes, ano, dia + '/' + mes + '/' + ano, this.verificarDia(dia, mes, ano))
            }
            dia++
          }
        }
        // Escreva o dia atual no loop
        let novaData = new Date()
        let novoAno = novaData.getFullYear()
        let novoMes = novaData.getMonth()
        if (novoAno === this.currYear && novoMes === this.currMonth && i === this.currDay) {
          if (aux !== -1) {
            // today
            this.setSemana(aux, i, mes, ano, i + '/' + (mes + 1) + '/' + ano, this.verificarDia(i, mes + 1, ano))
          }
        } else {
          if (aux !== -1) {
            // normal
            this.setSemana(aux, i, mes, ano, i + '/' + (mes + 1) + '/' + ano, this.verificarDia(i, mes + 1, ano))
          }
        }
        if (i === ultimaDataDoMes) {
          let dia = 1
          for (dow; dow < 6; dow++) {
            if (aux !== -1) {
              this.setSemana(aux, dia, mes, ano, dia + '/' + (mes + 2) + '/' + ano, this.verificarDia(dia, mes + 2, ano))
            }
            dia++
          }
        }
        i++
      } while (i <= ultimaDataDoMes)
    }
  }
}
</script>

<style scoped>
  :focus {
    outline: none;
  }
  .dia-aula {
    background: #209618;
    color: #fff !important;
    cursor: pointer;
  }
  .day-status {
    border-radius: 200px 200px 200px 200px;
    -moz-border-radius: 200px 200px 200px 200px;
    -webkit-border-radius: 200px 200px 200px 200px;
    border: 0px solid #000;
    background: #022dff;
    height: 7px;
    width: 7px;
    position: absolute;
    bottom: 1px;
    right: 1px;
  }
  .table-calendar td.normal:hover,
  td.today:hover {
    background: #189688;
    color: #fff !important;
    cursor: pointer;
  }
  .diaSelecionado {
    background: #e7b53d;
    color: #fff !important;
    cursor: pointer;
  }
  .calendar-wrapper {
    display: table;
    width: 100%;
    padding: 2px;
    border: 1px solid #6b737c;
    border-radius: 5px;
    background: #fff;
  }
  .table-title {
    position: relative;
    display: flex;
    flex-direction: row-reverse;
    background: #ab8732;
    text-align: center;
    height: 33px;
    padding: 2px;
    color: #fff;
  }
  .table-title .btn-calendar {
    width: 40px;
  }
  .table-title .btn-reset {
    height: 30px;
    margin-top: -2px;
  }
  .table-title .select-month {
    width: 130px;
  }
  .table-title .select-years {
    width: 100px;
  }
  .table-calendar {
    width: 100%;
    border: 1px solid #6b737c;
    border-radius: 3px;
    border-collapse: collapse;
    color: #444;
    height: calc(100vh - 320px);
    user-select: none; /* supported by Chrome and Opera */
    -webkit-user-select: none; /* Safari */
    -khtml-user-select: none; /* Konqueror HTML */
    -moz-user-select: none; /* Firefox */
    -ms-user-select: none; /* Internet Explorer/Edge */
  }
  .table-calendar thead td {
    height: 30px;
    text-align: center;
    border: 1px solid #6b737c;
    width: 15%;
    color: #28283b;
  }
  .table-calendar tbody td {
    vertical-align: top;
    padding-top: 20px;
    height: 100px;
    text-align: center;
    border: 1px solid #6b737c;
    width: 15%;
  }
  .dia-numero {
    font-size: 14px;
    position: absolute;
    top: 0;
    left: 0;
    width: 20px;
    height: 18px;
    background: #ab8732;
    color: #fff;
    text-align: center;
    border-bottom-right-radius: 5px;
  }
  .lista-agenda {
    display: flex;
    flex-direction: column;
    cursor: grabbing;
    height: 100%;
  }
  .agendamento,
  .legend-situacao {
    position: relative;
    height: 20px;
    width: 100%;
    font-size: 10px;
    color: #fff;
    margin: 1px 0;
    display: flex;
    align-items: center;
    padding: 0 5px;
    border-left: 10px solid transparent;
  }
  .agendamento.dragged,
  .legend-situacao.dragged {
    background: #00f;
    opacity: 0.4;
    color: #000;
  }
  .draggable {
    cursor: grab;
  }
  .caceled {
    border-top: 10px solid #d4182d;
    border-bottom: 10px solid #d4182d;
  }
  .marked {
    border-top: 10px solid #2370ff;
    border-bottom: 10px solid #2370ff;
  }
  .relocated {
    border-top: 10px solid #37a6b8;
    border-bottom: 10px solid #37a6b8;
  }
  .confirmed {
    border-top: 10px solid #2b8713;
    border-bottom: 10px solid #2b8713;
  }
  .hovered {
    border: dotted 3px #aa8217 !important;
  }
  .legend {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  .legend-situacao {
    width: 100px;
    margin-right: 3px;
  }
  .multiplydays a:after {
    content: "";
    border-top: 10px solid transparent;
    border-bottom: 10px solid transparent;
    border-left: 10px solid #2370ff;
    position: absolute;
    right: -10px;
    top: -10px;
    z-index: 1;
  }
  .not-current {
    color: #c0c0c0;
    pointer-events: none;
    opacity: 0.5;
  }
  .diaDeAula {
    color: #008000;
    font-size: 1.2em;
    cursor: pointer;
  }
  .today {
    font-weight: 700;
    color: #009688;
    font-size: 1em;
  }
  .btnBack {
    position: absolute;
    left: 0;
    top: 0;
    transform: translate(0%, 50%);
    width: 20px;
    height: 20px;
  }
  .btnNext {
    position: absolute;
    right: 0;
    top: 0;
    transform: translate(0%, 50%);
    width: 20px;
    height: 20px;
  }
  .btnCurrentDay {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
  .btnBack,
  .btnNext,
  .btnCurrentDay {
    border: 1px solid;
    border-radius: 5px;
    padding: 1px;
    font-size: 1em;
    color: #009688;
    cursor: pointer;
    font-family: "Roboto Condensed", sans-serif;
    text-transform: uppercase;
    transition: all 0.3s ease;
  }
  .btnBack:hover,
  .btnNext:hover,
  .btnCurrentDay:hover {
    color: #28283b;
    font-weight: bold;
  }
  .btnBack:focus,
  .btnNext:focus,
  .btnCurrentDay:focus {
    outline: none;
    box-shadow: none;
  }

</style>
