# Lab 3: SQL Database Design and Querying

[cite_start]This laboratory focuses on the implementation of relational databases using Python's `sqlite3` module[cite: 8]. [cite_start]It covers database schema creation, enforcing integrity constraints, and performing complex data analysis[cite: 17, 71, 210].

---

## Exercise 1: Aviation Database
**Goal:** Manage flight operations, aircraft inventory, and pilot assignments.

* **Schema Design**: 
    * [cite_start]Create a `Plane` table with an auto-incrementing primary key (`PLN`), aircraft name, capacity, and current location[cite: 17, 18, 19, 20, 21].
    * [cite_start]Create a `Pilot` table containing pilot numbers (`PN`), names, and addresses[cite: 24, 25, 26, 27].
    * [cite_start]Create a `Flight` table that links pilots and planes, including origin/arrival codes and scheduled times[cite: 30, 32, 33, 34, 35].
* [cite_start]**Constraint Enforcement**: Demonstrate a `UNIQUE` constraint violation by attempting to insert a record with a duplicate primary key[cite: 71].
* [cite_start]**Relational Querying**: Use `INNER JOIN` and subqueries to retrieve the names of all pilots who have operated an aircraft with the name "AIRBUS"[cite: 73, 75, 79].

---

## Exercise 2: Library Management System
**Goal:** Build a relational structure to track a library's catalog and member activity.

* [cite_start]**Author Management**: Define an `Author` table with a non-null name and birth year[cite: 91, 93, 94].
* [cite_start]**Book Catalog**: Design a `Book` table that includes a unique ISBN and a foreign key referencing the `Author` table[cite: 98, 103, 104].
* [cite_start]**Member Registry**: Implement a `Member` table with unique email addresses and membership dates[cite: 108, 111].
* [cite_start]**Borrowing History**: Create a `Borrow` table to track book loans between members and the catalog, utilizing multiple foreign key relationships[cite: 115, 121, 122].

---

## Exercise 3: Sales and Inventory Analytics
**Goal:** Perform business intelligence queries on electronic product sales data.



### Key Analytical Tasks:
* **Revenue Analysis**:
    * [cite_start]Calculate the total revenue generated specifically by the "Electronics" category using the `SUM` function[cite: 210, 214].
    * [cite_start]List every product name alongside its total calculated revenue ($unit\_price \times quantity\_sold$)[cite: 220].
* **Advanced Metrics**:
    * [cite_start]**Top Performer**: Identify the product with the highest quantity sold using the `MAX` subquery[cite: 236, 239].
    * [cite_start]**Zero Sales Detection**: Utilize a `LEFT JOIN` to identify products that have no recorded sales[cite: 244, 245, 248].
    * [cite_start]**Category Insights**: Determine the category with the highest average unit price using `GROUP BY` and `ORDER BY`[cite: 263, 265, 266].
* **Pattern & Conditional Queries**:
    * [cite_start]Use the `LIKE` operator to filter sales data for products starting with "Smart"[cite: 290].
    * [cite_start]Calculate the average quantity sold specifically for high-value products (unit price > 100)[cite: 298, 301].

---
