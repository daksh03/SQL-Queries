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

## Difference between CHAR and VARCHAR2 data types?
- `CHAR`: Fixed-length storage. If the defined length is not fully used, it is padded with spaces.
- `VARCHAR2`: Variable-length storage. Only the actual data is stored, saving space when the full length is not needed.

##  Different types of joins in SQL?
- `INNER JOIN`: Returns rows that have matching values in both tables.
-  `LEFT JOIN` (LEFT OUTER JOIN): Returns all rows from the left table, and matching rows from the right table.
-  `RIGHT JOIN` (RIGHT OUTER JOIN): Returns all rows from the right table, and matching rows from the left table.
-  `FULL JOIN` (FULL OUTER JOIN): Returns all rows when there is a match in either table.
-  `CROSS JOIN`: Produces the Cartesian product of two tables.

# Difference between WHERE and HAVING Clauses

| Feature            | WHERE                                | HAVING                               |
|--------------------|--------------------------------------|--------------------------------------|
| Filtering Stage    | Before any grouping                  | After `GROUP BY` has been applied    |
| Applies To         | Individual rows                      | Groups (aggregate results)           |
| Aggregate Support  | Cannot reference aggregates (SUM, COUNT, etc.) | Can reference aggregates            |
| Typical Order      | `WHERE` → `GROUP BY` → `HAVING` → `SELECT` | `GROUP BY` → `HAVING` → `SELECT`  |

## 🔍 Difference Between `DELETE` and `TRUNCATE` Commands

| Command   | Description |
|-----------|-------------|
| **DELETE**   | - Removes rows **one at a time**.<br>- Each deletion is **logged** in the transaction log.<br>- **Supports** a `WHERE` clause for conditional deletion.<br>- **Can be rolled back** if within a transaction. |
| **TRUNCATE** | - Removes **all rows at once** from a table.<br>- **Does not log** individual row deletions.<br>- **Does not support** a `WHERE` clause.<br>- **Faster** than `DELETE` for large datasets.<br>- **Cannot be rolled back** in some databases. |

## 🆚 Differences Between SQL and NoSQL Databases

| Feature                  | **SQL Databases**                                         | **NoSQL Databases**                                                  |
|--------------------------|-----------------------------------------------------------|----------------------------------------------------------------------|
| **Data Structure**       | Structured tables with rows and columns                  | Schema-less structures (e.g., key-value, document, graph, column)   |
| **Schema**               | Fixed schema, predefined before inserting data           | Flexible schema, allows dynamic changes                             |
| **Consistency**          | Adheres to **ACID** properties for reliable transactions | Prioritizes **CAP** properties; may sacrifice consistency for speed |
| **Scalability**          | Vertically scalable (adding more power to servers)       | Horizontally scalable (adding more servers)                         |
| **Use Cases**            | Best for complex queries and structured data             | Ideal for handling big data, real-time apps, and rapid development  |

> ⚠️ Note: The choice between SQL and NoSQL depends on your application's needs—no one-size-fits-all!

---
