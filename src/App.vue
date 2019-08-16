<template>
  <div id="app">
    <calendar v-model="agenda"/>
  </div>
</template>

<script>
import Calendar from './components/Calendar'

export default {
  name: 'App',
  components: {
    Calendar
  },
  data: () => ({
    agenda: [
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 5,
        'impedimentos': [],
        'agendamentos': []
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 6,
        'impedimentos': [],
        'agendamentos': []
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 7,
        'impedimentos': [],
        'agendamentos': [
          {
            'id': 111,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '07/08/2019',
            'aula': 2,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': []
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 8,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 88,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '08/08/2019',
            'aula': 2,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 27,
                'turmaDisciplina': {
                  'id': 34,
                  'gradeDisciplina': {
                    'id': 11,
                    'disciplina': {
                      'id': 9,
                      'nome': 'ENSINO RELIGIOSO',
                      'sigla': 'ENSINO RELIGIOSO'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 179,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          },
          {
            'id': 22,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '08/08/2019',
            'aula': 1,
            'conteudo': 'ADASDASD',
            'situacao': 'CANCELADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 24,
                'turmaDisciplina': {
                  'id': 31,
                  'gradeDisciplina': {
                    'id': 8,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 37,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 9,
        'impedimentos': [

        ],
        'agendamentos': [

        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 12,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 108,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '12/08/2019',
            'aula': 2,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 13,
        'impedimentos': [

        ],
        'agendamentos': [

        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 14,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 116,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '14/08/2019',
            'aula': 2,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 15,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 117,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '15/08/2019',
            'aula': 3,
            'conteudo': null,
            'situacao': 'CONFIRMADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 16,
        'impedimentos': [

        ],
        'agendamentos': [

        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 19,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 123,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 8,
              'pessoaFisica': {
                'id': 67406,
                'nome': 'ANA PAULA CAZAROTI VEIGA',
                'nomeSocial': null
              },
              'nome': 'ANA PAULA CAZAROTI VEIGA'
            },
            'turno': {
              'id': 4,
              'descricao': 'INTEGRAL'
            },
            'data': '19/08/2019',
            'aula': 2,
            'conteudo': null,
            'situacao': 'AGENDADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 42,
                'turmaDisciplina': {
                  'id': 49,
                  'gradeDisciplina': {
                    'id': 27,
                    'disciplina': {
                      'id': 2,
                      'nome': 'CIÊNCIAS DA NATUREZA',
                      'sigla': 'CIÊNCIAS DA NATUREZA'
                    }
                  }
                }
              },
              {
                'id': 46,
                'turmaDisciplina': {
                  'id': 53,
                  'gradeDisciplina': {
                    'id': 31,
                    'disciplina': {
                      'id': 7,
                      'nome': 'HISTÓRIA',
                      'sigla': 'HISTÓRIA'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 191,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          },
          {
            'id': 122,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 4,
              'descricao': 'INTEGRAL'
            },
            'data': '19/08/2019',
            'aula': 2,
            'conteudo': null,
            'situacao': 'AGENDADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 31,
                'turmaDisciplina': {
                  'id': 38,
                  'gradeDisciplina': {
                    'id': 15,
                    'disciplina': {
                      'id': 1,
                      'nome': 'MATEMÁTICA',
                      'sigla': 'MATEMÁTICA'
                    }
                  }
                }
              },
              {
                'id': 46,
                'turmaDisciplina': {
                  'id': 53,
                  'gradeDisciplina': {
                    'id': 31,
                    'disciplina': {
                      'id': 7,
                      'nome': 'HISTÓRIA',
                      'sigla': 'HISTÓRIA'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 190,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          },
          {
            'id': 124,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 6,
              'pessoaFisica': {
                'id': 3572,
                'nome': 'ABADIA APARECIDA LINO PEREIRA SILVA',
                'nomeSocial': null
              },
              'nome': 'ABADIA APARECIDA LINO PEREIRA SILVA'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '19/08/2019',
            'aula': 2,
            'conteudo': null,
            'situacao': 'AGENDADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 46,
                'turmaDisciplina': {
                  'id': 53,
                  'gradeDisciplina': {
                    'id': 31,
                    'disciplina': {
                      'id': 7,
                      'nome': 'HISTÓRIA',
                      'sigla': 'HISTÓRIA'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 192,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 20,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 101,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '20/08/2019',
            'aula': 10,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 21,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 89,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '21/08/2019',
            'aula': 1,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 47,
                'turmaDisciplina': {
                  'id': 54,
                  'gradeDisciplina': {
                    'id': 32,
                    'disciplina': {
                      'id': 3,
                      'nome': 'LÍNGUA PORTUGUESA',
                      'sigla': 'LÍNGUA PORTUGUESA'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 180,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          },
          {
            'id': 106,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '21/08/2019',
            'aula': 3,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 22,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 96,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '22/08/2019',
            'aula': 2,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          },
          {
            'id': 90,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '22/08/2019',
            'aula': 1,
            'conteudo': null,
            'situacao': 'CANCELADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 28,
                'turmaDisciplina': {
                  'id': 35,
                  'gradeDisciplina': {
                    'id': 12,
                    'disciplina': {
                      'id': 8,
                      'nome': 'GEOGRAFIA',
                      'sigla': 'GEOGRAFIA'
                    }
                  }
                }
              },
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 181,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          },
          {
            'id': 95,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '22/08/2019',
            'aula': 5,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 29,
                'turmaDisciplina': {
                  'id': 36,
                  'gradeDisciplina': {
                    'id': 13,
                    'disciplina': {
                      'id': 7,
                      'nome': 'HISTÓRIA',
                      'sigla': 'HISTÓRIA'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 23,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 120,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '23/08/2019',
            'aula': 5,
            'conteudo': null,
            'situacao': 'CONFIRMADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 29,
                'turmaDisciplina': {
                  'id': 36,
                  'gradeDisciplina': {
                    'id': 13,
                    'disciplina': {
                      'id': 7,
                      'nome': 'HISTÓRIA',
                      'sigla': 'HISTÓRIA'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 26,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 107,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '26/08/2019',
            'aula': 3,
            'conteudo': null,
            'situacao': 'REALOCADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 27,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 121,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '27/08/2019',
            'aula': 3,
            'conteudo': null,
            'situacao': 'CONFIRMADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 41,
                'turmaDisciplina': {
                  'id': 48,
                  'gradeDisciplina': {
                    'id': 26,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [

            ]
          },
          {
            'id': 125,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '27/08/2019',
            'aula': 1,
            'conteudo': null,
            'situacao': 'AGENDADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 28,
                'turmaDisciplina': {
                  'id': 35,
                  'gradeDisciplina': {
                    'id': 12,
                    'disciplina': {
                      'id': 8,
                      'nome': 'GEOGRAFIA',
                      'sigla': 'GEOGRAFIA'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 193,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          }
        ]
      },
      {
        'idSala': 3,
        'ano': 2019,
        'mes': 8,
        'dia': 29,
        'impedimentos': [

        ],
        'agendamentos': [
          {
            'id': 79,
            'sala': {
              'id': 3,
              'escolaEstrutura': {
                'id': 12,
                'descricao': 'SALA DE TECNOLOGIA ',
                'dimensao': '20X20',
                'tamanho': 400.0,
                'observacao': null,
                'localizacao': 1,
                'quantidadePessoas': 30,
                'tipoEstrutura': {
                  'id': 22,
                  'descricao': 'SALA DE TECNOLOGIA'
                },
                'escola': {
                  'id': 33,
                  'nome': 'ESCOLA ESTADUAL HUDSON MENDES MACHADO'
                }
              },
              'nome': 'SALA DE TECNOLOGIA ',
              'ativo': true,
              'quantidadeAula': 2,
              'salasProfissionais': [
                {
                  'id': 4,
                  'profissional': {
                    'id': 7,
                    'pessoaFisica': {
                      'id': 14166,
                      'nome': 'HUDSON MACHADO',
                      'nomeSocial': null
                    },
                    'nome': 'HUDSON MACHADO'
                  },
                  'turno': {
                    'id': 1,
                    'descricao': 'MATUTINO'
                  },
                  'dataEntrada': '12/08/2019',
                  'dataSaida': '16/08/2019'
                }
              ]
            },
            'profissional': {
              'id': 7,
              'pessoaFisica': {
                'id': 14166,
                'nome': 'HUDSON MACHADO',
                'nomeSocial': null
              },
              'nome': 'HUDSON MACHADO'
            },
            'turno': {
              'id': 1,
              'descricao': 'MATUTINO'
            },
            'data': '29/08/2019',
            'aula': 1,
            'conteudo': null,
            'situacao': 'CONFIRMADO',
            'realocacao': null,
            'turmasProfissionais': [
              {
                'id': 24,
                'turmaDisciplina': {
                  'id': 31,
                  'gradeDisciplina': {
                    'id': 8,
                    'disciplina': {
                      'id': 5,
                      'nome': 'ARTE',
                      'sigla': 'ARTE'
                    }
                  }
                }
              }
            ],
            'salasAtendimentosRecursos': [
              {
                'id': 162,
                'recurso': {
                  'id': 9,
                  'descricao': 'TABLET',
                  'ativo': true,
                  'cliente': {
                    'id': 25,
                    'nome': 'TERENOS'
                  }
                },
                'salaRecurso': null
              }
            ]
          }
        ]
      }
    ]
  })
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
