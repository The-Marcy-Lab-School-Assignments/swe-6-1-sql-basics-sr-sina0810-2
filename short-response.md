# Short Response: SQL Basics

Answer each question below. Write in complete sentences (3–5 per answer).

---

## Question 1

What is a database? Why do we use one instead of storing data in a JavaScript array on your server?

**Your answer:**

- A database is a system designed for sorting, and managing data. The system specifically organized to handle data efficiently.

- Data can't survive when we are using JavaScript because as soon as we restart, we no longer have access to that array. We use a database so the data can survive the restart.
- The server may have limited memory, but databases are specifically built to store huge amounts of data.


## Question 2

What is a primary key? Why does every table need one?

**Your answer:**

- A primary key is column that uniquely identifies every row in a table. Also it can never be NULL because it needs some value to be passed in. 

- Every table needs one because without out it we can't point at specific row. 
- It's very useful when we want to update or delete something in the table safely, so we can get the exact one that we need. 


## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: *"It returns the 5 most recently published fiction books."*

**Your answer:**
- It returns the 5 most recently published fiction books. From all the books that have specific genre type, and the year is from the most recente years. Plus we need only 5 of them. 

## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

**Your answer:**

- It's dangerous to run `DELETE FROM books` without a `WHERE` clause because we are not removing anything specific in the books, rather we are getting ride of the whole book table. Which means everything is gone. (finita)

## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

**Your answer:**
