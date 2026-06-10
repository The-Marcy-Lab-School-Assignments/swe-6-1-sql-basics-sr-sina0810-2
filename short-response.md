# Short Response: SQL Basics

Answer each question below. Write in complete sentences (3–5 per answer).

---

## Question 1

What is a database? Why do we use one instead of storing data in a JavaScript array on your server?

**Your answer:**

- A database is a system designed for storing, organizing, and retrieving 
data in a structured and permanent way.
- Data can't survive when we are using JavaScript because as soon as we restart, we no longer have access to that array. We use a database so the data can survive the restart.
- The server may have limited memory, but databases are specifically built to store huge amounts of data.


## Question 2

What is a primary key? Why does every table need one?

**Your answer:**

- A primary key is column that uniquely identifies every row in a table. Also it can never be NULL because it needs some value to be passed in. 

- Every table needs one because without it we cannot safely point to a 
specific row.

- It's very useful when we want to update or delete something in the table safely, so we can get the exact one that we need. 


## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: *"It returns the 5 most recently published fiction books."*

**Your answer:**
- It returns the 5 most recently published fiction books, ordered from newest to oldest.
 

## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

**Your answer:**

- It's dangerous to run `DELETE FROM books` without a `WHERE` clause because it deletes every single row in the table — not the table itself, but all the data inside it.This is why you should always include a WHERE clause to target only the specific rows you want to remove.


## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

**Your answer:**

- `ORDER BY` sorts the rows in the result set based on a column, either ascending or descending. 
- `LIMIT` cuts the result down to what we limit it for. 
- Yes we can use each without the other, for example, `SELECT * FROM books ORDER BY year DESC` give us all the books sorted by newest. Also  `SELECT * FROM books LIMIT 10` give us 10 rows. 