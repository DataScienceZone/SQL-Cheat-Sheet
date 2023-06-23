# SQL Notes 📝💾

## Introduction 👋
SQL (Structured Query Language) is a standard programming language used for managing relational databases. It enables you to store, retrieve, modify, and manipulate data stored in tables.

## Basic SQL Syntax ⌨️
- SQL statements typically start with a keyword, such as `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
- Tables are the primary way to store data in SQL, identified by a unique name.
- Columns represent specific attributes or data fields within a table.
- Rows contain individual records or data entries in a table.

## SELECT Statement 🔍
The `SELECT` statement is used to retrieve data from a database.

Syntax:
```sql
SELECT column1, column2, ...
FROM table_name;
```

Example:
```sql
SELECT * FROM customers;
```

## INSERT Statement ➕
The `INSERT` statement is used to insert new records into a table.

Syntax:
```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

Example:
```sql
INSERT INTO customers (name, email) 
VALUES ('John Doe', 'john@example.com');
```

## UPDATE Statement ✏️
The `UPDATE` statement is used to modify existing records in a table.

Syntax:
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

Example:
```sql
UPDATE customers
SET email = 'newemail@example.com'
WHERE customer_id = 1;
```

## DELETE Statement ❌
The `DELETE` statement is used to remove records from a table.

Syntax:
```sql
DELETE FROM table_name
WHERE condition;
```

Example:
```sql
DELETE FROM customers
WHERE customer_id = 1;
```

## Additional SQL Commands 📚

### ALTER TABLE
The `ALTER TABLE` command is used to add, modify, or delete columns in an existing table.

Syntax:
```sql
ALTER TABLE table_name
ADD column_name datatype;

ALTER TABLE table_name
MODIFY column_name datatype;

ALTER TABLE table_name
DROP COLUMN column_name;
```

### CREATE TABLE
The `CREATE TABLE` command is used to create a new table in the database.

Syntax:
```sql
CREATE TABLE table_name (
  column1 datatype,
  column2 datatype,
  ...
);
```

### DROP TABLE
The `DROP TABLE` command is used to delete an existing table from the database.

Syntax:
```sql
DROP TABLE table_name;
```

### JOIN
The `JOIN` command is used to combine rows from two or more tables based on a related column between them.

Syntax:
```sql
SELECT column_name(s)
FROM table1
JOIN table2
ON table1.column_name = table2.column_name;
```

### GROUP BY
The `GROUP BY` command is used to group rows in a table based on one or more columns.

Syntax:
```sql
SELECT column_name(s)
FROM table_name
GROUP BY column_name;
```

### ORDER BY
The `ORDER BY` command is used to sort the result set in ascending or descending order.

Syntax:
```sql
SELECT column_name(s)
FROM table_name
ORDER BY column_name ASC|DESC;
```

### WHERE
The `WHERE` clause is used to filter records based on a specified condition.

Syntax:
```sql
SELECT column_name(s)
FROM table_name
WHERE condition;
```
## DISTINCT
The `DISTINCT` keyword is used to retrieve unique values from a column in a table.

Syntax:
```sql
SELECT DISTINCT column_name
FROM table_name;
```

Example:
```sql
SELECT DISTINCT country
FROM customers;
```

## IN
The `IN` keyword is used to match a value against a list of possible values.

Syntax:
```sql
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);
```

Example:
```sql
SELECT name
FROM employees
WHERE department IN ('Sales', 'Marketing');
```

## LIKE
The `LIKE` keyword is used in a WHERE clause to search for a specific pattern in a column.

Syntax:
```sql
SELECT column_name(s)
FROM table_name
WHERE column_name LIKE pattern;
```

Example:
```sql
SELECT name
FROM customers
WHERE name LIKE 'J%';
```

## BETWEEN
The `BETWEEN` keyword is used to select values within a specified range.

Syntax:
```sql
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

Example:
```sql
SELECT price
FROM products
WHERE price BETWEEN 10 AND 20;
```

## COUNT
The `COUNT` function is used to count the number of rows in a table or the number of occurrences of a specific value in a column.

Syntax:
```sql
SELECT COUNT(column_name)
FROM table_name;

SELECT COUNT(*)
FROM table_name;
```

Example:
```sql
SELECT COUNT(customer_id)
FROM customers;

SELECT COUNT(*)
FROM orders
WHERE status = 'Pending';
```

Keep up the good work! :thumbsup:

These are just a few additional SQL commands. There are many more advanced concepts and statements to explore. Have fun coding! 🚀
