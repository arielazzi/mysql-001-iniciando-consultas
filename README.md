# mysql-001-iniciando-consultas

Lista de comandos básicos: 
- mysql -uroot -p
  - Acessar o MySQL
- create database controle_compras;
  - Criar um banco de dados
- show tables;
  - Exibir tabelas
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
- UPDADE compras set valor = 5 where id = 20;
  - Atulizar dados
- delete from compras where data between '2009-03-05' and '2009-03-20';
  - Deletar registros
- select * from where not valor = 108;
  - Operador NOT para negação
- desc compras;
  - describe table
- alter table compras modify observacoes varchar(255) not null;
  - altera a estrutura da tabela
- alter table compras modify recebido tinyint(1) default '1';
  - default
- alter table compras add column forma_pagt enum('cartao', 'boleto', 'dinheiro')
  - aceita somente os paramentros passados

CREATE TABLE FUNCIONARIOS (
            NOME VARCHAR(100) NOT NULL,
            CARGO ENUM('DIRETOR', 'FUNCIONARIO') NOT NULL,
            SALARIO DECIMAL(10,2) DEFAULT '10000'
        )

CREATE TABLE compras (
          id int NOT NULL AUTO_INCREMENT,
          valor double,
          data datetime,
          observacoes text NOT NULL,
          recebido tinyint(1) DEFAULT 1,
          forma_pagto ENUM('DINHEIRO', 'CARTAO', 'BOLETO'),
          PRIMARY KEY (id)
        )

 - select sum(valor)
- soma os valores
 - select count(valor)
- contador
 - group by 
	- agrupamento

- select month(data), year(data), sum(valor) from compras group by month(data),year(data)

-media
- select month(data), year(data), avg(valor) from compras group by month(data),year(data)