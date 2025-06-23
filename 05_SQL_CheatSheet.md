# SQL Cheatsheet

## Data Definition
```sql
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(100),
  age INT
);
```

## Basic Queries
```sql
SELECT * FROM users;
SELECT name FROM users WHERE age > 18;
```

## Joins
```sql
SELECT * FROM users u
JOIN orders o ON u.id = o.user_id;
```

## Aggregates
```sql
SELECT COUNT(*) FROM users;
SELECT AVG(age) FROM users;
```

## Window Functions
```sql
SELECT name, RANK() OVER (ORDER BY age DESC) FROM users;
```
