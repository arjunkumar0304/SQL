# SQL
# 1. Relational Database Basics:
It is a type of database that stores data in tables — just like an Excel sheet.
Each table has rows (data records) and columns (data fields).

* Example:
A table called Students might have columns like ID, Name, and Age, and rows with actual student details.

Relation:
Different tables can be linked using a key (like a student’s ID can link to their marks in another table).

# 2. Database Management System (DBMS)
A DBMS is a software that helps us store, manage, and use data easily.
It allows users to add, update, delete, and fetch data from databases.

Examples:
* MySQL
* PostgreSQL
* SQL Server

These tools help us write and run SQL queries.

# 3. Basic SQL Syntax

SQL (Structured Query Language) is used to talk to the database.
We use it to:

Get data: SELECT * FROM students;

Add data: INSERT INTO students (name, age) VALUES ('Arjun', 22);

Update data: UPDATE students SET age = 23 WHERE name = 'Arjun';

Delete data: DELETE FROM students WHERE name = 'Arjun';


# 4. DDL (Data Definition Language)
DDL commands help manage the structure of the database (not the data itself).
Main commands: CREATE, ALTER, DROP, and TRUNCATE.
