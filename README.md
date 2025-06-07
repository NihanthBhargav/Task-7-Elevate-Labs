# Task 7: Sales Summary using SQLite and Python

## 📌 Objective
Analyze basic sales data from a SQLite database using SQL inside Python and visualize the revenue by product with a bar chart.

---

## 🧾 Dataset
- **Database**: `sales_data.db`
- **Table**: `sales(product TEXT, quantity INTEGER, price REAL)`
- **Rows**: 1500 randomly generated entries

---

## 🛠 Tools Used
- `sqlite3` for database connection
- `pandas` for data handling
- `matplotlib` for data visualization

---

## 🔍 SQL Query Used

```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
