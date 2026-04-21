# 📊 E-Commerce Sales Dashboard (Power BI)

## 🧾 Project Overview

This project is a **Power BI Dashboard** designed to analyze and visualize e-commerce sales data.  
The data is sourced from a **MySQL database** and transformed into meaningful business insights using Power BI and DAX.

It helps in understanding sales performance, product trends, and customer behavior.

---

## 🎯 Objectives

- Analyze overall sales performance
- Identify top-selling products
- Track monthly sales trends
- Understand customer purchasing behavior
- Provide interactive filtering for better decision-making

---

## 🗄️ Data Source (SQL Database)

This project uses a **MySQL database** as the primary data source.

### 🔌 Data Connection
- Data is imported into Power BI using **MySQL Connector**
- Tables are linked through relationships in Power BI Data Model

### 📊 SQL Tables Used
- Orders Table
- Products Table
- Order Details Table
- ### 🔄 Data Flow
SQL Database → Power BI Data Model → DAX Measures → Dashboard Visualization

## 📊 Key Metrics (KPIs)

* 💰 Total Sales
* 🧾 Total Orders
* 💵 Profit *(estimated based on margin)*

## 📈 Dashboard Features

* **Sales by Category** → Compare performance of different categories
* **Monthly Sales Trend** → Track growth over time
* **Top Products Analysis** → Identify best-performing products
* **Interactive Filters (Slicers)**:

  * Category filter
 
## 🧠 DAX Measures Used

```DAX
Total Sales = 
SUMX(order_details, order_details[quantity] * RELATED(products[price]))

Total Orders = 
COUNT(order_details[order_id])

Avg Order Value = 
[Total Sales] / [Total Orders]

Profit = 
[Total Sales] * 0.3
```

## 🗂️ Dataset Description

The dataset includes:

### 🧾 Orders Table

* order_id
* order_date
* customer_id

### 📦 Products Table

* product_id
* product_name
* category
* price

### 📊 Order Details Table

* order_id
* product_id
* quantity


## 🛠️ Tools & Technologies

* Power BI
* DAX (Data Analysis Expressions)
* Data Modeling (Relationships)


## 🎨 Dashboard Design

* Clean layout with KPI cards on top
* Charts in the middle for analysis
* Slicers for interactivity
* User-friendly and simple design

