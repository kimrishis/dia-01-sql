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