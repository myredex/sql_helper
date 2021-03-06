# SQL Examples and Cheat Sheet

## Simple SQL queries

| SQL query  | What it does |
| ------------- | ------------- |
| SELECT name FROM sqlite_master WHERE type='table'; | Get all the tables from the database |
| PRAGMA table_info(table_name);  | Shows data types and info about columns in the table |
| SELECT * FROM table_name; | select all data in the table |
| SELECT column_1, column_2 FROM table_name; | select two columns from the table |
| SELECT column_1, column_2 FROM table_name WHERE condition_is; | select only those rows from the table which is compatible with condition |
| SELECT column_1, column_2 FROM table_name WHERE any_column LIKE '%Elinoice%'; | We have two columns and choose all the rows in which field ADDRESS contains **Elincoice** |
| SELECT column_1_1 FROM table_1 WHERE column_1_2 IN (SELECT column_2_1 FROM table_2 WHERE column_2_2='ABC') | We have depency between two tables and show data from first depending of the result of the query from the second table  |
| SELECT column_1_1 FROM table_1 JOIN table_2 ON table_1.column_1_2 = table_2.column_2_2  JOIN table_3 ON table_2.column_2_3=table_3.column_3_1 WHERE column_3_3='ABC' | Selections through three connected tables  |

## Where variants

SQL query  | What it does
------------- | -------------
WHERE column_1 LIKE 'Joh%'; | where string starts from **"Joh"** for example **Johan**
WHERE column_1 = 5  AND (column_2 BETWEEN 60000 AND 70000) | rows whrere data from column 1 is equal to 5 and data in column 2 in range from 60000 to 70000

## Counting

SQL query  | What it does
------------- | -------------
SELECT column_1, COUNT(coulumn_2) AS count FROM table GROUP BY column_1; | Counted all values of column_2 where column_2's values match

## Sorting

SQL query  | What it does
------------- | -------------
SELECT * FROM table_name ORDER BY column_1; | select all data from the table and sort it by values of the **column_1** acsending
SELECT * FROM table_name ORDER BY column_1 DESC; | select all data from the table and sort it by values of the **column_1** Decsending
SELECT * FROM table_name ORDER BY column_1 DESC, column_2 DESC; | select all data from the table and sort it by values of the **column_1** Decsending and then column_2 Decsending

## Functions
Freeqently used functions.

SQL query  | Example | What it does 
------------- | ------------- | -------------
AVG() | SELECT AVG(column_1) FROM table_1; | Average value
DISTINCT() | SELECT DISTINCT(column_1) from table_1; | Only unique values
DAY() | SELECT DAY(column_1) from table_1; | Returns day of the month from the date
LENTH() | SELECT LENGTH(column_1) from table_1; | Lenth of the value
LCASE() | SELECT LCASE(column_1) from table_1; | Shows results in lowercase
MAX() | SELECT MAX(column_1) FROM table_1; | Extract maximum value of the column
MONTH() | SELECT MONTH(column_1) from table_1; | Returns month from the date
ROUND() | SELECT ROUND(column_1) from table_1; | Round values
SUM() | SELECT SUM(column_1) from table_1; | Aggregates all the data in column
TIMEDIFF() | SELECT TIMEDIFF(end_date, start_date); | It counts time between two dates 
UCASE() | SELECT UCASE(column_1) from table_1; | Shows results in uppercase

