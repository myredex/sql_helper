# SQL Examples and Cheat Sheet

## Simple SQL queries

SQL query  | What it does
------------- | -------------
SELECT * FROM table_name; | select all data in the table
SELECT column_1, column_2 FROM table_name; | select two columns from the table
SELECT column_1, column_2 FROM table_name WHERE condition_is; | select only those rows from the table which is compatible with condition
SELECT column_1, column_2 FROM table_name WHERE any_column LIKE '%Elinoice%'; | We have two columns and choose all the rows in which field ADDRESS contains **Elincoice**
SELECT column_1_1 FROM table_1 WHERE column_1_2 IN (SELECT column_2_1 FROM table_2 WHERE column_2_2='ABC') | We have depency between two tables and show data from first depending of the result of the query from the second table 

## Where variants

SQL query  | What it does
------------- | -------------
WHERE column_1 LIKE 'Joh%'; | where string starts from **"Joh"** for example **Johan**
WHERE column_1 = 5  AND (column_2 BETWEEN 60000 AND 70000) | rows whrere data from column 1 is equal to 5 and data in column 2 in range from 60000 to 70000

## Sorting

SQL query  | What it does
------------- | -------------
SELECT * FROM table_name ORDER BY column_1; | select all data from the table and sort it by values of the **column_1** acsending
SELECT * FROM table_name ORDER BY column_1 DESC; | select all data from the table and sort it by values of the **column_1** Decsending
SELECT * FROM table_name ORDER BY column_1 DESC, column_2 DESC; | select all data from the table and sort it by values of the **column_1** Decsending and then column_2 Decsending

## String patterns and Ranges



SQL query  | What it does
------------- | -------------


