TakeHome Assessment

This assignment consists of two parts - SQL questions and an open ended data question. 
Please return your answers to Part 1 and Part 2 in a single document, as either 
1. A Google Document (making sure to grant viewing permissions), or 
1. A plain text file.

# Part 1 - SQL questions
In this exercise you will connect to a live database and write SQL queries to answer various questions. Your submission for this part should include only the SQL queries. 


## The Database
The task focuses on the “financial” schema (see explanation on how to access the DB below). 
The relevant tables are: loan, order, trans, account.
The relationships between the tables
A loan belongs to 1 account, an account can have multiple loans.
An order belongs to 1 account, an account can have multiple orders.
A transaction belongs to 1 account, an account can have multiple transactions.

![Financial Database](https://user-images.githubusercontent.com/35533263/134050206-8308c6c8-54f2-465d-89b2-9350c64d908a.png)

## How to connect to the database:
Download [MySQL Workbench](https://www.mysql.com/products/workbench/) or use a database client of your choice.
Within MySQL Workbench or your database client, add a new connection using the following credentials:

- hostname: relational.fit.cvut.cz
- port: 3306
- username: guest
- password: relational

An example for querying the order table from the financial scheme:
“Select * from financial.order”

## Questions:
1. Write a query that returns the account_id, number of orders, and total amount of all orders for each account with more than 3 orders.

1. Write a query that returns the account_id, number of orders, total amount of all orders, number of loans, and total amount of all loans for each account.

1. Use the same query as #2 and add the logic for only keeping the accounts that the total loan amount is lower than the total orders amount (including accounts without any loans)

1. Write a query that returns the account_id, order_id, order amount, and the share out of the total order amount for that account.
For example, for account_id = 2 the total amount of all orders is 10638.7, that account has 2 orders: order_id=29402  and order_id=29403. The amount of order_id=29402 is 3372.7. The share of this order is 31.7% out of all the orders of that account. We want to calculate that share for every order.

1. Write a query that returns a list of all “k_symbol” unique values from both order and trans tables.
	


# Part 2 - Data question

# Pharmaceutical supplier
We are working for DrugBasics Co., a company that sells chemicals to pharmaceutical manufacturers all over the world. 

# The data
Pharmaceuticals are tricky because every country has different regulations. This impacts which items we can sell to which clients. Fortunately, we know the location of all of our customers’ factories. The table below contains a sample of our data.

Customer ID | Factory ID | Country
----------- | ---------- | -------
1 | 1| USA
1|2|Canada
1|3|France
2|4|USA
2|5|Russia
2|6|UK
2|7|Mexico
3|8|USA
3|9|UK
3|10|China
3|11|China
3|12|Germany
4|13|France


# Context:
The head of the sales division wants to determine which customers to assign to each of her teams in a way that improves regulation specialization for each team. Each customer only works with one sales team.

# Task:
She has asked you to help in this task by calculating which customers are most similar to each other **based on the countries they have factories in**. Specifically, she wants to know the **similarity between any two customers.**

Given two customers, how would you calculate their similarity? In what situations might your approach not work well?

Your answer should include a formula and high level reasoning. Feel free to provide any details about your thought process you think are helpful, but your answer should be no more than 2 paragraphs. Coding/queries are not required.


