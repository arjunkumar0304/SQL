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

# 6. DCL (Data Control Language) 
Used to control access or permissions to the data in a database.
It helps in granting and revoking privileges to users on database objects (like tables, views, etc.).

# EXAMPLE: 
# GRANT
Used to give permissions to a user.

( SYNTAX :  GRANT privilege_name ON object_name TO user_name; )

Example for student database  
* (GRANT SELECT, INSERT ON student TO teacher1;)
* This allows teacher1 to view (SELECT) and add (INSERT) records in the student table.

# REVOKE
Used to take back permissions that were previously granted.

( Syntax: REVOKE privilege_name ON object_name FROM user_name;)

Example for student Database
* (REVOKE INSERT ON student FROM teacher1;)
* This removes teacher1’s permission to insert data into the student table.
  
# 7. DQL (Data Query Language)
Used to fetch or retrieve data from the database.

# GROUP BY
Used to group rows that have the same value in one or more columns.
Usually used with aggregate functions like COUNT, SUM, AVG, etc.
<img width="1091" height="1003" alt="Screenshot 2025-10-23 161651" src="https://github.com/user-attachments/assets/eb46e13f-e7a6-486a-85a6-b6480c7f31a7" />

# HAVING 
is like WHERE, but it is used after GROUP BY to filter groups.
<img width="1286" height="767" alt="Screenshot 2025-10-23 161803" src="https://github.com/user-attachments/assets/f29e131f-6e23-4e7e-9d68-45c7c344cc51" />

# ORDER BY 
used to sort the result — either ascending (ASC) or descending (DESC) order
<img width="1185" height="932" alt="Screenshot 2025-10-23 161550" src="https://github.com/user-attachments/assets/ec3022b1-5597-4ef3-a3c5-cbb2761af8b1" />

# 8. TCL (Transaction Control Language)
TCL commands are used to manage transactions in a database.
A transaction is a group of SQL operations that are treated as a single unit of work — either all succeed or all fail.

* COMMIT-- permanently saves changes,
* ROLLBACK -- undoes uncommitted changes,
* SAVEPOINT  -- lets you set a point to roll back to within a transaction.\
  
# 9.Constraints
* rules you set on your table to keep your data correct and safe.
* They make sure no wrong or duplicate data goes inside your table.
# 9.1 PRIMARY KEY
* Uniquely identifies each record in a table.
* It cannot be NULL and must be unique.
Example: studentID INT PRIMARY KEY

<img width="882" height="608" alt="Screenshot 2025-10-24 190624" src="https://github.com/user-attachments/assets/2edbf7e5-789b-4865-b5fe-efb49c738ce8" />


# 9.2 FOREIGN KEY
* Creates a link between two tables.
* It ensures the value in one table matches a value in another table.
Example: FOREIGN KEY (deptID) REFERENCES department(deptID)
<img width="1146" height="687" alt="Screenshot 2025-10-24 190930" src="https://github.com/user-attachments/assets/2eb9f2ca-7eff-4787-8675-55dfb889e6d7" />


# 9.3 UNIQUE
Makes sure all values in a column are different (no duplicates).
Example: email VARCHAR(30) UNIQUE

# 9.4 CHECK
Ensures that the values in a column meet a specific condition.
Example: CHECK (age >= 18)

# 9.5 NOT NULL
Ensures a column cannot have a NULL (empty) value.
Example: name VARCHAR(20) NOT NULL

# 10. Joins:
* INNER JOIN: rows that match in both tables.
* LEFT JOIN: all rows from the left table, plus matching rows from the right (or NULL when no match).
* RIGHT JOIN: all rows from the right table, plus matching rows from the left (or NULL when no match).
* FULL JOIN: all rows from both tables; where no match exists, columns show NULL.
* CROSS JOIN: every row from left paired with every row from right (Cartesian product).

# INNER JOIN

<img width="1151" height="496" alt="Screenshot 2025-10-24 190955" src="https://github.com/user-attachments/assets/c7d2a815-b8bb-449f-9a27-b94fec098766" />

# LEFT JOIN
<img width="1075" height="666" alt="Screenshot 2025-10-24 191134" src="https://github.com/user-attachments/assets/4950f81a-23a7-4dec-80fa-f5b1246ba28b" />

# RIGHT JOIN:
<img width="1272" height="742" alt="Screenshot 2025-10-24 191154" src="https://github.com/user-attachments/assets/df8b4233-b49d-45dd-940b-03b4b672c623" />

# FULL JOIN:
<img width="1281" height="743" alt="Screenshot 2025-10-24 191223" src="https://github.com/user-attachments/assets/17a3765a-23ea-4e67-8d55-9be5e5c1a2a9" />

# CROSS JOIN
<img width="1134" height="1034" alt="Screenshot 2025-10-24 191240" src="https://github.com/user-attachments/assets/557d92fe-ce44-42d9-8f17-be8b256c3aae" />

# Aggregation functions

* COUNT(*) — count rows
<img width="1122" height="627" alt="Screenshot 2025-10-24 193142" src="https://github.com/user-attachments/assets/424edd70-54f3-40dc-8113-a68e7ee3f37c" />


* SUM(column) — add values in a column

<img width="1465" height="743" alt="Screenshot 2025-10-24 193509" src="https://github.com/user-attachments/assets/e0caa2df-4a97-4fd3-9f1c-c6f0b10a3064" />


* AVG(column) — average value
<img width="1136" height="715" alt="Screenshot 2025-10-24 193202" src="https://github.com/user-attachments/assets/2c6fe103-6c9b-4b4a-a9e0-23c6b7495764" />


* MIN(column) and MAX(column) — smallest / largest
<img width="1397" height="806" alt="Screenshot 2025-10-24 193229" src="https://github.com/user-attachments/assets/6d84de57-6195-49a4-82a3-f94b3c443086" />

 # SQL Clause:
* SELECT — choose columns / expressions

* FROM — table(s)

* WHERE — filter rows before grouping

<img width="1407" height="760" alt="Screenshot 2025-10-24 193832" src="https://github.com/user-attachments/assets/74d07d67-c860-450e-b154-d88a15fedb4b" />


* GROUP BY — form groups of rows

<img width="1463" height="686" alt="Screenshot 2025-10-24 194011" src="https://github.com/user-attachments/assets/c1a77505-7a02-437b-bc7c-6c860ff28381" />


* HAVING — filter groups after grouping

<img width="1500" height="713" alt="Screenshot 2025-10-24 194044" src="https://github.com/user-attachments/assets/2bf378b2-7c34-482d-8043-7a54ec704787" />


* ORDER BY — sort the final result

<img width="1163" height="759" alt="Screenshot 2025-10-24 194100" src="https://github.com/user-attachments/assets/6c7f9989-4fae-4e36-abab-13921d369506" />

# 12.1 Arithmetic Operators: +, -, , /
# Add

<img width="1149" height="776" alt="Screenshot 2025-10-24 194754" src="https://github.com/user-attachments/assets/210054ef-7bb6-4517-94d2-7480c20889e0" />


# Sub

<img width="1350" height="823" alt="Screenshot 2025-10-24 194809" src="https://github.com/user-attachments/assets/b8d055c3-5cbe-4f04-9327-d1e5d2f918a3" />


# Mul

<img width="1371" height="770" alt="Screenshot 2025-10-24 194833" src="https://github.com/user-attachments/assets/040db2dc-25eb-4f18-892b-25d1c15264a4" />


# div

<img width="1239" height="788" alt="Screenshot 2025-10-24 194846" src="https://github.com/user-attachments/assets/14a322ee-8a71-4492-844c-177a81a03c57" />

# 12.2 Comparison Operators

<img width="829" height="518" alt="Screenshot 2025-10-24 195337" src="https://github.com/user-attachments/assets/694e7e7a-980c-4ca0-b491-2af7d230a555" />

<img width="1286" height="1001" alt="Screenshot 2025-10-24 200758" src="https://github.com/user-attachments/assets/8f846179-5636-41d5-810a-54708c8ba25d" />



# 12.3 Logical Operators

<img width="819" height="309" alt="Screenshot 2025-10-24 195354" src="https://github.com/user-attachments/assets/0ee307da-161e-493d-8b61-4498c71a301c" />

<img width="1034" height="923" alt="Screenshot 2025-10-24 201018" src="https://github.com/user-attachments/assets/e26aa530-8ebe-4194-9e89-5a559cac9f67" />

# 12.4 String Concatenation Operator: ||

<img width="1319" height="752" alt="Screenshot 2025-10-24 201252" src="https://github.com/user-attachments/assets/2ea5c1c8-4fda-4a23-b0a2-c784795550d4" />


# 13.Procedures:
Procedure in SQL is like a saved program or a set of SQL commands that you can reuse anytime.
# 13.1 CREATE PROCEDURE: Creating stored procedures.
<img width="1108" height="891" alt="Screenshot 2025-10-27 130955" src="https://github.com/user-attachments/assets/cb4234a0-fbd5-4bcf-b635-2b38d6d54264" />


# 13.2 ALTER PROCEDURE: Modifying existing stored procedures.
<img width="1233" height="946" alt="Screenshot 2025-10-27 131155" src="https://github.com/user-attachments/assets/714743d0-2c41-45a4-a8ad-3124a54349f3" />

#  13.3 DROP PROCEDURE: Deleting stored procedures.

#  13.4 EXECUTE: Running a stored procedure.
<img width="1079" height="870" alt="Screenshot 2025-10-27 131118" src="https://github.com/user-attachments/assets/d979be6e-042a-48f5-8ac0-eb6726f0b75f" />


# 14. Subquery
A Subquery is a query inside another query.
It helps to get data from one query and use it inside another.

Find the oldest student
<img width="1036" height="749" alt="Screenshot 2025-10-27 175807" src="https://github.com/user-attachments/assets/50413bbd-1972-481b-8e59-8bc6a0b3be07" />

Find youngest student name
<img width="909" height="718" alt="Screenshot 2025-10-27 181521" src="https://github.com/user-attachments/assets/28826724-1644-4851-9ee8-8dc5538c6a9d" />

# 14.2 CTE

CTE means Common Table Expression.
It is like a temporary table that you create inside a query — only for that query.

<img width="928" height="617" alt="Screenshot 2025-10-27 184853" src="https://github.com/user-attachments/assets/26a38a8d-a070-471a-8784-a68424066208" />


# 15. Views:
A view is a virtual table. It’s used to see specific data easily without writing long queries again and again.
We use CREATE VIEW to make it and DROP VIEW to remove it.”
  
# 3.1 CREATE VIEW: Creating views for simplified querying.
<img width="1223" height="684" alt="Screenshot 2025-10-27 145458" src="https://github.com/user-attachments/assets/f9f8b8e6-e4a8-4d5e-8925-55401b614764" />

# 3.2 DROP VIEW: Removing views.
<img width="1227" height="769" alt="Screenshot 2025-10-27 145652" src="https://github.com/user-attachments/assets/df8e22d4-87a2-43ff-bf23-21f7a7cebb41" />

 







