# 🛍️ Retail Sales Analysis Project (SQL)

This project involves analyzing a **Retail Sales** dataset using **PostgreSQL**. It covers **data cleaning**, **exploration**, and **business problem-solving** through structured SQL queries.

---

## 🗂️ Project Features

- 🧱 **Database & Table Creation**
- 🧹 **Data Cleaning**: Handling null values
- 📊 **Exploration**: Sales count, customer demographics, category insights
- 🧠 **Business Intelligence Queries**: Insights on sales, customer behavior, best months, etc.

---

## 🧾 Key Tables

- **`retail_sales`**: Stores each transaction with detailed sales attributes including:
  - `transactions_id`, `sale_date`, `sale_time`, `customer_id`
  - `gender`, `age`, `category`, `quantity`
  - `price_per_unit`, `cogs`, `total_sale`

---

## ❓ Business Questions Answered

✔️ Retrieve sales on a specific date  
✔️ Find high-quantity clothing sales in November  
✔️ Total sales by category  
✔️ Average age of beauty category buyers  
✔️ High-value transactions (> 1000)  
✔️ Orders by gender/category  
✔️ Best-selling month per year  
✔️ Top 5 customers by total sale  
✔️ Unique customers per category  
✔️ Orders by time-based shifts (Morning, Afternoon, Evening)

---

## 🧪 Sample SQL Snippet

```sql
-- Q.3 Write a SQL query to calculate the total sales (total_sale) for each category.
SELECT category, SUM(total_sale) AS net_sale,
COUNT(*) AS total_orders 
FROM retail_sales
GROUP BY 1;

