
# Task 7 - Basic Sales Summary from SQLite in Python

## Objective
Pull simple sales info (total quantity sold, total revenue) from a SQLite database and display it using print statements and a bar chart.

## Tools Used
- Python
- SQLite (via sqlite3)
- pandas
- matplotlib

## How It Works
1. Creates a database `sales_data.db` and a `sales` table.
2. Inserts sample sales records.
3. Executes an SQL query to summarize sales data (GROUP BY product).
4. Loads results into a pandas DataFrame.
5. Displays a bar chart of revenue by product.

## Output
- Printed summary of sales.
- A bar chart saved as `sales_chart.png`.

## SQL Query Used
```sql
SELECT product, SUM(quantity) AS total_qty, SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product
