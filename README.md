# mysql-001-iniciando-consultas

## mysql -uroot -p
## create database controle_compras;
## use controle_compras;
## create table COMPRAS (id int auto_increment primary key, valor double, data date, observacoes varchar(255), recebido boolean);
## INSERT INTO COMPRAS (VALOR, DATA, OBSERVACOES, RECEBIDO) VALUES (100.0, '2007-05-12', 'COMPRAS DE MAIO', 1);
## SELECT * FROM COMPRAS
## mysql -uroot -p controle_compras < cap2.sql
## SELECT VALOR, DATA FROM COMPRAS
## SELECT VALOR, VALOR * 3 AS TRIPLO, DATA FROM COMPRAS
## SELECT * FROM COMPRAS WHERE VALOR > 1000
## SELECT * FROM COMPRAS WHERE (VALOR > 1000 AND VALOR < 3000) OR (DATA < '2010-02-12');
## SELECT * FROM COMPRAS WHERE OBSERVACOES LIKE 'COMPRAS%';