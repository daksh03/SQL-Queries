# SQL-Queries from LeetCode

# 🔗 Database Management System (DBMS) Relationships

In DBMS, relationships define how data is structured and interconnected across multiple tables. There are three primary types:

## 📌 One-to-One (1:1)
A single record in one table corresponds to a single record in another table.  
**Example:** A `Person` table linked to a `Passport` table, where each person has only one passport.

## 📌 One-to-Many (1:M)
A single record in one table can be associated with multiple records in another table.  
**Example:** A `Customer` table linked to an `Orders` table, where each customer can place multiple orders.

## 📌 Many-to-Many (M:M)
Multiple records in one table can be associated with multiple records in another table.  
**Example:** A `Students` table linked to a `Courses` table, where students can enroll in multiple courses, and each course can have multiple students.

# SQL Commands Overview

SQL commands are categorized into different types based on their functionality:

## 📌 Data Definition Language (DDL)
Used for defining and modifying database structures.
- `CREATE` – Create a new database object (table, index, view, etc.)
- `ALTER` – Modify an existing database object
- `DROP` – Delete an existing database object
- `TRUNCATE` – Remove all records from a table without logging individual row deletions

## 📌 Data Manipulation Language (DML)
Used for managing data within tables.
- `SELECT` – Retrieve data from a table
- `INSERT` – Add new records to a table
- `UPDATE` – Modify existing records
- `DELETE` – Remove records from a table

## 📌 Data Control Language (DCL)
Used for controlling access to data.
- `GRANT` – Provide privileges to users
- `REVOKE` – Remove granted privileges

## 📌 Transaction Control Language (TCL)
Used for handling transactions within a database.
- `COMMIT` – Save changes permanently
- `ROLLBACK` – Undo changes since last commit
- `SAVEPOINT` – Set a checkpoint to rollback to if needed

---
