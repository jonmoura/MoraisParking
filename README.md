# MoraisParking
- Projeto da disciplina de Estrutura de Dados: Sistema de Estacionamento de uma Universidade.

- Grupo: Jonathan Moura / Bárbara Braz / Suzana 

- Linguagem de programação: Python

- Banco de Dados: PostgreSQL12

    Data Base criada: moraisparking_python 
    Tabelas criadas: veiculo e funcionario
    Tabela veiculo: possui as colunas nome_veiculo, matricula_veiculo, curso_veiculo, placa_veiculo e vaga_veiculo, sendo       nome_veiculo a primary key
    Tabela funcionario: possui as colunas nome_funcionario, matricula_funcionario e senha_funcionario, sendo nome_funcionario a primary key

  Conectando o banco de dados no Python:
  con = psycopg2.connect(host="localhost",database="moraisparking_python",user="postgres",password="123456",port=5432)

  Para inicializar o banco de dados é necessário executar os seguintes comandos no CMD:
  cd c://program files/postgresql/12/bin
  pg_ctl -D "c:/program files/postgresql/12/data" start
  O primeiro comando leva para o diretório da pasta bin. 
  O segundo comando inicia o banco buscando na pasta data.

  Biblioteca importada: psycopg2
  Queries utilizadas: 
  queryCadVeiculo = "INSERT INTO veiculo (nome_veiculo, matricula_veiculo, curso_veiculo, placa_veiculo, vaga_veiculo) values (%s, %s, %s, %s, %s)"
  queryCadFuncionario = "INSERT INTO funcionario (nome_funcionario, matricula_funcionario, senha_funcionario) values (%s, %s, %s)"

  Biblioteca importada: reportlab
  Query utilizada:
  BancoDeDados.cur.execute("SELECT * FROM public.funcionario")
