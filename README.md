# 🏭 Production & Inventory Analysis using SQL

## 📌 Project Overview
This project analyzes production and inventory data from a manufacturing company using **SQL in Google BigQuery**. The goal is to identify stock levels, production efficiency, defect rates, and warehouse values to support data-driven business decisions.

---

## 🛠️ Tools Used
- **Google BigQuery** — SQL queries and analysis
- **Google Sheets** — Dataset preparation
- **SQL** — Data analysis and insights

---

## 📂 Dataset
Three tables were created in BigQuery under the dataset `manufacturing_db`:

| Table | Rows | Description |
|---|---|---|
| `products` | 10 | Product catalogue with cost and reorder info |
| `inventory` | 10 | Current stock levels per warehouse |
| `production` | 20 | Production run records over Jan–Feb 2024 |

---

## 🔍 Queries & Analysis

### Query 1 — Inventory Status Overview
Joined `products` and `inventory` tables to see current stock levels and assigned status labels (Sufficient / Critical / Low Stock) using CASE WHEN logic.

📸 ![Q1 Inventory Status](screenshots/Q1_Inventory_Status.png)

---

### Query 2 — Products Needing Reorder
Filtered products where stock is below reorder level and calculated estimated reorder cost in PKR.

📸 ![Q2 Reorder Alert](screenshots/Q2_Reorder_Alert.png)

---

### Query 3 — Production Efficiency by Product
Used GROUP BY and aggregate functions to compare planned vs actual production and calculate defect rate per product.

📸 ![Q3 Production Efficiency](screenshots/Q3_Production_Efficiency.png)

---

### Query 4 — Production by Shift
Analyzed Morning, Afternoon and Night shift performance to identify which shift is most efficient and has the lowest defect rate.

📸 ![Q4 Production By Shift](screenshots/Q4_Production_By_Shift.png)

---

### Query 5 — Warehouse Value in PKR
Calculated total inventory value stored in each warehouse by joining inventory and products tables.

📸 ![Q5 Warehouse Value](screenshots/Q5_Warehouse_Value.png)

---

## 💡 Key Insights
- **5 out of 10 products** are below reorder level and need immediate procurement
- **Control Panel Unit** is the most critically low stock item (only 3 units)
- **Morning shift** is the most efficient with the lowest defect rate
- **Warehouse-B** holds the highest inventory value due to expensive components
- **Electric Motor 5HP** has the highest defect rate and needs quality review

---

## 📊 SQL Concepts Used
- `JOIN` — combining multiple tables
- `WHERE` — filtering data
- `GROUP BY` — grouping results
- `CASE WHEN` — conditional logic
- `SUM, COUNT, ROUND` — aggregate functions
- `ORDER BY` — sorting results

---

## 👤 Author
**[Your Name]**
Google Certified Data Analyst
📧 [Your Email]
🔗 [Your LinkedIn URL]
