# Bright-coffee-shop-sales-analysis
Sales analysis project using SQL and Excel
📄 Overview
This project analyzes historical transactional data from **Bright Coffee Shop** to help the new CEO make data-driven decisions.  
It uncovers sales trends, identifies top-performing products, and highlights peak revenue periods.

---

## 🎯 Objectives
- Determine which products generate the most revenue  
- Identify peak sales hours and daily patterns  
- Analyze sales trends across time and product categories  
- Recommend actionable strategies to improve performance  

---

## 🛠️ Tools & Technologies
| Category | Tools Used |
|-----------|-------------|
| **Data Processing** | Snowflake, MySQL Workbench, Databricks |
| **Visualization** | Microsoft Excel, Power BI, Tableau |
| **Planning & Presentation** | Miro, PowerPoint, Canva |

---

## 🧩 Project Tasks

### 🗺️ Task 1: Planning & Architecture (Miro)
Designed a **data flow diagram** showing:
- Data source and ETL process  
- Storage in Snowflake  
- Analysis and reporting workflow  

**Key Calculations**
```sql
total_amount = unit_price * transaction_qty
💾 Task 2: Data Processing (Snowflake)
Converted the Excel file into CSV format

Imported the CSV into Snowflake

Cleaned and transformed the data:

Corrected price formats (e.g., '3,1' → 3.1)

Added a time bucket column for grouping

Calculated total sales per transaction

Sample Query

sql
Copy code
SELECT 
    product_type,
    DATE_TRUNC('hour', transaction_time) AS time_bucket,
    SUM(unit_price * transaction_qty) AS total_amount,
    SUM(transaction_qty) AS total_units
FROM bright_coffee_sales
GROUP BY product_type, time_bucket
ORDER BY time_bucket;
📊 Task 3: Data Analysis (Excel / Power BI)
Created dashboards showing:

Total revenue by product type

Peak sales hours

Quantity of items sold

Top-performing and low-performing products

🎤 Task 4: Presentation
Presented findings and recommendations to management.

Recommendations

Launch marketing campaigns during slow periods

Stock up on top-selling items

Promote underperforming products

Automate daily sales tracking

Introduce loyalty programs during high-traffic hours

📦 Deliverables
✅ Miro Architecture Diagram

✅ Cleaned Dataset (Excel / CSV)

✅ SQL Scripts

✅ PowerPoint Presentation



Scale reporting for multiple store locations

Integrate customer loyalty data for advanced insights

👩🏽‍💻 Author
Amukelani Khosa
Junior Data Analyst
📧 aymowhlakudi@gmail.com
📊 Bright Coffee Shop Sales Analysis – BrightLearn Project

