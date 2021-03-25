# BD_Ecommerce
Modelo de banco de dados otimizado para um ecommerce com mais de um milhão de usuários.


#################################################
#################################################
######### Scripts de geração de dados ###########
#########		e	      ###########
#########     restauração do BD       ###########
#################################################


------------ Restauração do backup do BD --------

Para restaurar o banco de dados elaborado para o
projeto da disciplina de Sistema de Banco de Dados,
primeiro abra o pgAdmin, crie um banco de dados,
com nome a sua escolha, e ao criar, clique com o
botão direito sobre o banco e selecione a opção
'restore'. Selecione o arquivo 'ecommerce.bakcup',
na pasta 'Backup', e clique em restore. Espere a 
execução do processo. O backup contém 50mil tuplas 
inseridas  na tabela produto, 100mil tuplas na 
tabela cliente e 1milhão de tuplas na tabela compra.

------------ Scripts de geração de dados --------

Os scripts são de autoria própria e foram criados 
para popular o banco de dados do trabalho de 
Sistemas de Banco de Dados. Cada script é
responsável por realizar a inserção de dados em
uma tabela do banco, sendo elas: cliente, produto
e compra.
Os scripts são rodados no próprio pgAdmin, pois
foram construídos na forma de transações,
portanto, caso queira utiliza-los, copie-os e
execute-os no pgAdmin como se fosse executar uma
sql comum, mas tenha em vista que algum dos 
scripts pode demorar para serem concluidos.
Abaixo vou listar os passos para suas execuções.

1) Caso não tenha feito o restore no arquivo de
backup do banco de dados, crie um banco de dados
com nome a sua escolha.

2) Execute as DDLs de criação de tabelas, na pasta
'DDL', e a execução do script de função trigger,
na pasta 'Funções'.

3) Após execute as scripts de inserção de dados,
começando pela script de população da tabela
produto, contida no arquivo txt 
'script_produto.txt', na pasta 'Scripts'.

4) Em seguida execute os scripts de inserção
na tabela cliente, contido no arquivo txt 
'script_cliente.txt', na pasta 'Scripts'.

5) Por último execute o script de inserção na
tabela compra, contido no arquivo txt 
'script_compra.txt', na pasta 'Scripts'.

6) Caso queira variar o número de inserções em
cada tabela, controle o volume de dados através
do número presente no loop de cada script. Por
padrão os números são: 50mil tuplas inseridas 
na tabela produto, 100mil tuplas na tabela
cliente e 1milhão de tuplas na tabela compra.

As inserções nas tabelas cliente e produto 
demoram, respectivamente, 13 sec e 12 sec, em média.
A inserção na tabela compra é mais demorada,
demorando em média 1hra e 20min para realizar
as inserções.
