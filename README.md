🍕 Pizza Sales Report Dashboard (SQL Project)
📌 Project Overview

The Pizza Sales Report Dashboard is a SQL-based data analysis project designed to analyze sales performance of a pizza store.
This project focuses on extracting business insights such as revenue trends, top-selling pizzas, order patterns, and category performance using SQL queries.

The goal of this project is to demonstrate strong SQL skills, data analysis capability, and business intelligence understanding.

🎯 Objectives

Analyze total revenue and total orders

Identify best and worst-selling pizzas

Analyze sales by category and size

Determine peak order times

Generate KPIs for business decision-making

Create dashboard-ready insights using SQL queries

🛠️ Tech Stack

Database: MySQL / SQL Server

Language: SQL

Tools Used:

MySQL Workbench / SSMS

Excel / Power BI (for visualization – optional)

Version Control: Git & GitHub

📂 Dataset Description

The dataset contains pizza sales transaction data with the following tables:

orders

order_details

pizzas

pizza_types

Key Columns:

Order ID

Order Date & Time

Pizza Name

Category

Size

Quantity

Price

📊 Key Performance Indicators (KPIs)

💰 Total Revenue

🛒 Total Orders

🍕 Total Pizzas Sold

📈 Average Order Value

⏰ Peak Order Hours

🏆 Top 5 Best Selling Pizzas

📉 Bottom 5 Selling Pizzas

🔎 Sample SQL Analysis Performed
1️⃣ Total Revenue
SELECT SUM(quantity * price) AS Total_Revenue
FROM order_details od
JOIN pizzas p ON od.pizza_id = p.pizza_id;

2️⃣ Total Orders
SELECT COUNT(DISTINCT order_id) AS Total_Orders
FROM orders;

3️⃣ Top 5 Best-Selling Pizzas
SELECT pizza_name, SUM(quantity) AS Total_Sold
FROM order_details od
JOIN pizzas p ON od.pizza_id = p.pizza_id
GROUP BY pizza_name
ORDER BY Total_Sold DESC
LIMIT 5;

📊 Business Insights

Classic category contributes the highest revenue.

Large size pizzas are most preferred.

Weekends show higher order volume.

Certain pizzas consistently perform as top sellers.

📈 Dashboard Features (If Created in Power BI / Excel)

Revenue Trend by Date

Sales by Category

Sales by Pizza Size

Top & Bottom Performers

Hourly Order Distribution

🚀 How to Run This Project

Clone this repository:

git clone https://github.com//puneetsinghal9114/Pizza-sales-dashboard-project.git


Import the dataset into your SQL database.

Run the SQL queries provided in the project files.

(Optional) Connect database to Power BI or Excel for dashboard creation.

📁 Project Structure
📦 Pizza-Sales-Report
 ┣ 📜 pizza_sales.sql
 ┣ 📊 dashboard_screenshots/
 ┣ 📄 Pizza_Sales_Report.pdf
 ┣ 📜 SQL_Queries.docx
 ┗ 📄 README.md

💡 Learning Outcomes

Advanced SQL queries (JOIN, GROUP BY, HAVING, Aggregation)

KPI calculation

Business data interpretation

Dashboard-ready data preparation

Data-driven decision making

📌 Future Improvements

Add stored procedures

Implement views for reusable queries

Build live dashboard with Power BI

Deploy project using cloud database (AWS RDS)
