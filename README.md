# Lab 3: SQL Database Design and Querying

This laboratory focuses on the implementation of relational databases using Python's `sqlite3` module. It covers database schema creation, enforcing integrity constraints, and performing complex data analysis.

---

## Exercise 1: Aviation Database
**Goal:** Manage flight operations, aircraft inventory, and pilot assignments.

* **Schema Design**: 
    * Create a `Plane` table with an auto-incrementing primary key (`PLN`), aircraft name, capacity, and current location.
    * Create a `Pilot` table containing pilot numbers (`PN`), names, and addresses.
    * Create a `Flight` table that links pilots and planes, including origin/arrival codes and scheduled times.
* **Constraint Enforcement**: Demonstrate a `UNIQUE` constraint violation by attempting to insert a record with a duplicate primary key.
* **Relational Querying**: Use `INNER JOIN` and subqueries to retrieve the names of all pilots who have operated an aircraft with the name "AIRBUS".

---

## Exercise 2: Library Management System
**Goal:** Build a relational structure to track a library's catalog and member activity.

* **Author Management**: Define an `Author` table with a non-null name and birth year.
* **Book Catalog**: Design a `Book` table that includes a unique ISBN and a foreign key referencing the `Author` table.
* **Member Registry**: Implement a `Member` table with unique email addresses and membership dates.
* **Borrowing History**: Create a `Borrow` table to track book loans between members and the catalog, utilizing multiple foreign key relationships.

---

## Exercise 3: Sales and Inventory Analytics
**Goal:** Perform business intelligence queries on electronic product sales data.



### Key Analytical Tasks:
* **Revenue Analysis**:
    * Calculate the total revenue generated specifically by the "Electronics" category using the `SUM` function.
    * List every product name alongside its total calculated revenue ($unit\_price \times quantity\_sold$).
* **Advanced Metrics**:
    * **Top Performer**: Identify the product with the highest quantity sold using the `MAX` subquery.
    * **Zero Sales Detection**: Utilize a `LEFT JOIN` to identify products that have no recorded sales.
    * **Category Insights**: Determine the category with the highest average unit price using `GROUP BY` and `ORDER BY`.
* **Pattern & Conditional Queries**:
    * Use the `LIKE` operator to filter sales data for products starting with "Smart".
    * Calculate the average quantity sold specifically for high-value products (unit price > 100).
