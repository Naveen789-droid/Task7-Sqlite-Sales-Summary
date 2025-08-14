# Task 7 – Basic Sales Summary (SQLite + Python in Google Colab)

## Overview
This project connects Python to a SQLite database, runs SQL queries to summarize sales data, and visualizes the results in a bar chart.

## Steps Performed
1. Created `sales_data.db` with a `sales` table containing sample data.
2. Ran SQL query to calculate:
   - Total quantity sold per product
   - Total revenue per product
3. Loaded query results into a pandas DataFrame.
4. Printed results in tabular form.
5. Created a bar chart showing revenue by product.
6. Downloaded chart and database for submission.

## SQL Used
```sql
SELECT 
    product,
    SUM(quantity) AS total_qty,
    ROUND(SUM(quantity * price), 2) AS revenue
FROM sales
GROUP BY product
ORDER BY revenue DESC;
