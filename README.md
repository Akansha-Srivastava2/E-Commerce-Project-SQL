# E-Commerce SQL Analysis

## 📌 Project Overview

This project focuses on analyzing e-commerce data using SQL to generate meaningful business insights.

The analysis is performed using order, product, and product-order data. SQL queries are used to calculate revenue, identify top-performing products, analyze orders, and solve various business-related questions.

The main objective of this project is to demonstrate practical SQL skills required for a Data Analyst role.

---

## 🗂️ Dataset

The dataset contains the following tables:

* **Orders** – Contains information related to customer orders and order status.
* **Products** – Contains product-related information.
* **Product_Order** – Contains product-level order details such as quantity and unit price.

> Note: This dataset does not contain a separate Customer table.

---

## 🛠️ Tools & Technologies

* MySQL
* SQL
* GitHub

---

## 📊 SQL Concepts Used

This project demonstrates the following SQL concepts:

* SELECT
* WHERE
* GROUP BY
* HAVING
* ORDER BY
* Aggregate Functions
* JOINs
* INNER JOIN
* LEFT JOIN
* Subqueries
* Window Functions
* RANK()
* DENSE_RANK()
* ROW_NUMBER()
* String Functions
* Conditional Aggregation

---

## 💰 Revenue Calculation

The dataset does not contain a separate revenue column.

Revenue is calculated using:

```sql
Quantity × Unit Price
```

For example:

```sql
SUM(quantity * unit_price) AS total_revenue
```

This calculation is used throughout the analysis to determine product-level and order-level revenue.

---

## 🔍 Business Questions

The project answers business-oriented questions such as:

Total number of orders
Total quantity of products sold 
Total Revenue 
Average selling price
Highest priced product 
Lowest priced product 
Revenue Generated  by each product 
Rank product by revenue 
Average ordered value 
Provide whose sold more quantity is more than 5 
Product that never ordered



---

## 📈 Key Analysis

### 1. Total Revenue

Revenue is calculated using:

```sql
SUM(quantity * unit_price)
```

This helps determine the overall sales generated from the available order data.

### 2. Product Revenue Analysis

Products are joined with the `Product_Order` table using `product_id` to calculate revenue for each product.

### 3. Top Revenue Products

Products are ranked according to their total revenue to identify the highest-performing products.

### 4. Second-Highest Revenue Product

Window functions such as `DENSE_RANK()` are used to identify the product with the second-highest total revenue.

### 5. Order Analysis

The `Orders` table is analyzed to understand order volume and order status.

---

## 🔗 Table Relationships

The tables are connected using common keys.

```text
Products
   |
   | product_id
   |
Product_Order
   |
   | order_id
   |
Orders
```

### Relationship

```text
Products.product_id
        ↓
Product_Order.product_id

Product_Order.order_id
        ↓
Orders.order_id
```

---

## 📁 Project Structure

```text
ecommerce-sql-analysis/
│
├── README.md
├── ecommerce_schema.sql
├── products.sql
├── product_order.sql
├── orders.sql
└── analysis_queries.sql
```

---

## 🎯 Project Objective

The objective of this project is to strengthen practical SQL and data analysis skills by solving real-world e-commerce business problems.

The project demonstrates the ability to:

* Extract data using SQL
* Combine multiple tables using JOINs
* Perform calculations using aggregate functions
* Analyze product and order performance
* Use subqueries and CTEs
* Apply window functions for ranking and comparisons
* Convert raw transactional data into meaningful business insights

---

## 👩‍💻 Author

**Akansha Shrivastava**

Data Analyst | SQL | Python | Power BI | Excel

GitHub: Akansha-Srivastava2
