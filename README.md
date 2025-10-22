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

# 4.1 CREATE
Used to create new database objects such as tables or indexes.
<img width="1679" height="772" alt="Screenshot 2025-10-22 183443" src="https://github.com/user-attachments/assets/e6b1acb7-bead-48b6-b5dc-09ab42539bc5" />
<img width="1408" height="823" alt="Screenshot 2025-10-22 184339" src="https://github.com/user-attachments/assets/a3c3ff95-8f8b-4926-b662-23367815aad3" />

* PRIMARY KEY → unique identifier for each row.
* FOREIGN KEY → link between two tables.
* CHECK → ensure data follows certain rules.

# 4.2 ALTER
Used to change the structure of an existing table.
<img width="918" height="748" alt="Screenshot 2025-10-22 184609" src="https://github.com/user-attachments/assets/1e47fe91-6972-44bb-84e4-513bf0aa6d9d" />


# 4.3 DROP
Used to delete database objects permanently.

# 4.4 TRUNCATE
Used to delete all rows from a table, but keep the table structure.


# 5. DML (Data Manipulation Language)

DML commands are used to work with the data stored in tables — inserting, updating, deleting, or reading it.

# 5.1 INSERT
Used to add new records to a table.
<img width="1498" height="931" alt="Screenshot 2025-10-22 185431" src="https://github.com/user-attachments/assets/4d394475-1654-4a4f-81d1-7577ec69a515" />


# 5.2 UPDATE
Used to change existing records.
<img width="808" height="761" alt="Screenshot 2025-10-22 185835" src="https://github.com/user-attachments/assets/c479f2bd-6dd7-4384-859e-206896f3f0ab" />

# 5.3 DELETE

Used to remove specific rows from a table.
<img width="1073" height="706" alt="Screenshot 2025-10-22 190142" src="https://github.com/user-attachments/assets/38fd062b-d3df-4a77-95c1-f8a022b55c72" />

# 5.4 SELECT
Used to fetch data from tables.

<img width="1276" height="957" alt="Screenshot 2025-10-22 185444" src="https://github.com/user-attachments/assets/2a191e93-ffe6-4559-942e-54fa33df062f" />
