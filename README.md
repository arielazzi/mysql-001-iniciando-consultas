# mysql-001-iniciando-consultas

Lista de comandos básicos: 
- mysql -uroot -p
  - Acessar o MySQL
- create database controle_compras;
  - Criar um banco de dados
- use controle_compras;
  - Acessar o banco
- create table COMPRAS (id int auto_increment primary key, valor double, data date, observacoes varchar(255), recebido boolean);
  - Criar uma tabela
- INSERT INTO COMPRAS (VALOR, DATA, OBSERVACOES, RECEBIDO) VALUES (100.0, '2007-05-12', 'COMPRAS DE MAIO', 1);
  - Inserir dados na tabela
- SELECT * FROM COMPRAS
  - Selecionar todos os dados da tabela
- mysql -uroot -p controle_compras < cap2.sql
  - Importar dados 
- SELECT VALOR, DATA FROM COMPRAS
  - Selecionar colunas
- SELECT VALOR, VALOR * 3 AS TRIPLO, DATA FROM COMPRAS
  - Realizar expressões na consulta
- SELECT * FROM COMPRAS WHERE (VALOR > 1000 AND VALOR < 3000) OR (DATA < '2010-02-12');
  - Busca especificas
- SELECT * FROM COMPRAS WHERE OBSERVACOES LIKE 'COMPRAS%';
  - busca para buscar apenas uma parte de campos text
