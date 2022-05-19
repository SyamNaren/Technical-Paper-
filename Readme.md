

SQL Definition
==============

Basically, SQL stands for **Structured Query Language** which is basically a language used by databases. This language allows to handle the information using tables and shows a language to query these tables and other objects related (views, functions, procedures, etc.). Most of the databases like SQL Server, Oracle, PostgreSQL, MySQL, MariaDB handle this language (with some extensions and variations) to handle the data.

With SQL you can insert, delete, and update data. You can also create, delete, or alter database objects.


### Version table

*   SQL 86
*   SQL 89
*   SQL 92
*   SQL 99
*   SQL 2003
*   SQL 2006
*   SQL 2008
*   SQL 2011
*   SQL 2016

SQL Definition Syntax
---------------------

Let’s say that we have a small table named students with some data:
| ID | First Name  | Last Name  |
| :---:   | :-: | :-: |
| 1 | John | Rambo |
| 2 | Luke | Skywalker |
| 3 | Peter | Chewbacca |
| 4 | John | Matrix |

If we want to see all the data, the SQL query will be:

**Select \* from students**

Basically, we are saying show me all the columns (\*) from the table students. If we want to get just the ID column and the Name, the query will be like the below:

Select ID, Name from students

In this example, the SQL query is getting the ID, the Name columns from the student’s table. Something important to say is that we can specify the column names in any order. I will not talk about the performance and indexes when using queries, but the order of the columns may affect the performance in tables with several millions of rows or with joins to other columns.



Something that is great in SQL is that you can query multiple tables. For example, if I have the grades of the students, I could query information from both tables. Let’s say that we have the student’s score in a table:

| ID | Score  |
| :---:   | :-: |
| 1 | 52 |
| 2 | 63 |
| 3 | 57 |
| 4 | 69 |


ID is the student’s ID. This is a common column between the student and the score table. We need the common column to create a relationship. If we want the name, lastname and the student’s score, the query will be this one:

1

2

3

4

5

**Select Name,Lastname,Score**

**From student**

**Inner join**

**Score**

**ON students.ID\=score.ID**

The first line is simple. We are calling the columns with the data required. The second line is just the first Table and the inner join is to use the second table named score. Finally, we need to tell in the query what are the common columns to match the data. In this example, the IDs. To differentiate the ID column from the different tables, we need to specify the table names followed by a period and then the column name.


SQL Definition for UNION, INTERSECT, EXCEPT
-------------------------------------------

SQL defined a standard syntax to create a union between 2 tables or to get the common rows (intersect) or the rows that are not common (except). The following article explains how to use them:


Extensions of the SQL definition
--------------------------------

Each database system has its own SQL extension. For example, SQL Server uses T-SQL that is a SQL extension. Oracle uses PL-SQL, MySQL and MariaDB use SQL/PSM (SQL and Persistent Stored Module). PSM is an ISO standard for stored procedures. Teradata and Informix use SPL and there are several different extensions used by different System Databases.


Conclusion
----------
Basically, it is a language to handle data. It was initially created to handle structured data, but even the NoSQL databases (databases that are non-relational), usually use a SQL extension to retrieve data. Big Data platforms are also using SQL extensions to handle their data, so the SQL definition will be useful for a long time.
