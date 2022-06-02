# Dia 01 sql #

estudo sql, pelo site https://www.w3schools.com/sql/sql_intro.asp

## intro 

uso do comando SELECT * FROM Customers; para consultar dados

## syntax

comandos mais importantes 
    SELECT - extracts data from a database (extrai dados do banco de dados)
    UPDATE - updates data in a database (atualiza dado no banco de dados)
    DELETE - deletes data from a database (apaga dado no banco de dados)
    INSERT INTO - inserts new data into a database (insere novo dado no banco de dados)
    CREATE DATABASE - creates a new database (cria um novo banco de dados)
    ALTER DATABASE - modifies a database (modifica o banco)
    CREATE TABLE - creates a new table (cria uma nova tabela)
    ALTER TABLE - modifies a table (modifica uma tabela)
    DROP TABLE - deletes a table (apaga uma tabela)
    CREATE INDEX - creates an index (search key) (cria um indice)
    DROP INDEX - deletes an index (apaga um indice)

## SELECT Statement

uso de comandos para especificar colunas e a tabela.

SELECT column1, column2, ...
FROM table_name;

## SELECT DISTINCT Status

uso do comando SELECT DISTINCT Country FROM Customers; para restrigir apenas para a coluna selecionada

## WHERE Clause

=	Equal(ex SELECT * FROM Products WHERE Price = 18;)[puxa valores iguais a 18 no banco de dados]

>	Greater than (ex SELECT * FROM Products WHERE Price > 30;)	[mostra os dados de todos os produtos com valor acima de 30]

<	Less than(ex SELECT * FROM Products WHERE Price < 30;)[resulta em dados com valores abaixo de 30]

>=	Greater than or equal (ex SELECT * FROM Products WHERE Price >= 30)[apenas dados maiores ou iguais]

<=	Less than or equal (ex SELECT * FROM Products WHERE Price <= 30)[apenas dados menores ou iguais]	

<>	Not equal. (ex SELECT * FROM Products WHERE Price <> 30) [mostra apenas dados nao iguais]

BETWEEN	Between a certain range	(ex SELECT * FROM Products WHERE BETWEEN 50 AND 60;) [apresenta os dados neste intervalo de 50 a 60]

LIKE	Search for a pattern	(ex SELECT * FROM Customers WHERE City LIKE 's%';) [faz a pesquisa buscando um padrao neste exemplo envia palavras iniciando com a LETRA S]

IN	To specify multiple possible values for a column (SELECT * FROM Customers WHERE City IN ('Paris','London');)[possibilita a busca por mais de um parametro]

## AND, OR and NOT no where

(SELECT * FROM Customers WHERE Country='Germany' AND (City='Berlin' OR City='München');) [exemplo usando "AND" e "OR"]
(SELECT * FROM Customers WHERE NOT Country='Germany' AND NOT Country='USA';) [exemplo excluindo 2 parametros pra busca de dados]
adiciona na busca outros parametros como and (e), or(ou), NOT (fazendo a exclusao especifica)

## ORDER BY Keyword

(SELECT * FROM Customers ORDER BY Country;)
adiciona parametros para a ordenaçao dos dados dentro da tabela ... podendo ser do maior para o menor ou vice e versa.

## INSERT INTO Statement

(INSERT INTO Customers (CustomerName, City, Country) VALUES ('Cardinal', 'Stavanger', 'Norway');) usamos esse exemplo para inserir uma informacao na tabela q pudesse estar faltando informaçao ou ela estive invalidade por algum motivo


## What is a NULL Value?

(SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;)

faz a pesquisa no banco de dados buscando valores null (q seriam inexistentes ou erroneos q n foram aceitos pelo banco de dados)

## UPDATE Statement

(UPDATE Customers
SET ContactName='Juan'
WHERE Country='Mexico';)
exemplo da maneira correta de buscar para atualizar o contato JUAN... se atentar a forma correta fazendo uso do "WHERE" pq se usar,(UPDATE Customers
SET ContactName='Juan';) ir sobreescrever tds os customers para o nome JUAN fazendo assim a atualizacao e n busca do banco de dados

## DELETE SYNTAX

DELETE FROM table_name WHERE condition; com esse comando podemos fazer a exclusao de um dado no lugar definido 
DELETE FROM Customers WHERE CustomerName='Kim rishis'; apagando Kim Rishis da tabela, querendo apagar  a tabela td podemos usar o seguinte codigo
(DELETE FROM table_name;)

