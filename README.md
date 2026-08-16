# 📊 E-Commerce Sales Performance Dashboard

An interactive **E-Commerce Sales Performance Dashboard** built with **Microsoft Power BI** to analyze sales performance, customer behavior, order trends, product performance, and inventory-related metrics.

## 🎯 Project Overview

This project transforms e-commerce transactional data into interactive business insights using data modeling, DAX calculations, and Power BI visualizations.

The dashboard is designed to help users quickly understand overall business performance and identify important sales, customer, and product trends.

## 🛠️ Tools & Technologies

* Microsoft Power BI
* Power Query
* DAX
* MySQL
* Data Modeling
* Data Visualization

## 🗂️ Dataset

The project contains four main tables:

### Customers

Contains customer information such as:

* Customer ID
* Customer Name
* Gender
* Age
* City
* Country
* Signup Date

### Orders

Contains order-level information such as:

* Order ID
* Customer ID
* Order Date
* Payment Method
* Order Status
* Total Amount

### Order_Items

Contains product-level information for each order:

* Order Item ID
* Order ID
* Product ID
* Quantity
* Unit Price

### Products

Contains product information such as:

* Product ID
* Product Name
* Category
* Price
* Stock Quantity

## 🔗 Data Model

The Power BI model uses relationships between the four tables:

```text
Customers (1) ───── (*) Orders
                         │
                         │
                         ▼
                    Order_Items
                         ▲
                         │
Products (1) ───────── (*) 
```

Relationships:

* `Customers[customer_id]` → `Orders[customer_id]`
* `Orders[order_id]` → `Order_Items[order_id]`
* `Products[product_id]` → `Order_Items[product_id]`

## 📈 Dashboard Pages

### 1. Sales Performance Overview

Provides a high-level view of overall e-commerce performance.

**Key Performance Indicators:**

* Total Sales
* Total Orders
* Total Customers
* Total Products
* Average Order Value

**Visualizations:**

* Monthly Sales Trend
* Sales by Category
* Sales by Payment Method
* Top 10 Products by Sales
* Orders by Status

**Interactive Filters:**

* Order Date
* Category
* Payment Method
* Order Status

---

### 2. Customer & Order Analysis

Focuses on customer behavior and order-related insights.

**Key Performance Indicators:**

* Total Customers
* Average Customer Age
* Total Orders
* Average Order Value

**Visualizations:**

* Sales by City
* Customers by Gender
* Customer Signup Trend
* Top 10 Customers by Sales

---

### 3. Product Performance Analysis

Focuses on product sales and inventory performance.

**Key Performance Indicators:**

* Total Products
* Total Quantity Sold
* Average Product Price
* Total Stock

**Visualizations:**

* Top 10 Products by Sales
* Quantity Sold by Category
* Product Price vs Sales
* Product Performance Details

## 🧮 DAX Measures

The project uses DAX measures to calculate key business metrics.

Example:

```DAX
Total Sales =
SUMX(
    Order_Items,
    Order_Items[quantity] * Order_Items[unit_price]
)
```

```DAX
Total Quantity Sold =
SUM(Order_Items[quantity])
```

These measures are used across the dashboard to support dynamic analysis.

## 🔍 Key Business Questions

The dashboard helps answer questions such as:

* What is the overall sales performance?
* Which product categories generate the most sales?
* Which products are the top performers?
* Which payment methods are most frequently used?
* How are orders distributed by status?
* Which cities generate the highest sales?
* How are customers distributed by gender and age?
* How has the customer base changed over time?
* Which customers contribute the most sales?
* How do product prices relate to sales performance?

## 📁 Project Structure

```text
Ecommerce-Sales-Performance-PowerBI/
│
├── Sales_Performance_Dashboard.pbix
├── README.md
└── screenshots/
    ├── sales-performance-overview.png
    ├── customer-order-analysis.png
    └── product-performance-analysis.png
```

## 🚀 Skills Demonstrated

This project demonstrates practical skills in:

* Data Cleaning
* Data Modeling
* Power Query
* DAX
* KPI Development
* Interactive Dashboard Design
* Data Visualization
* Business Analysis
* Customer Analysis
* Product Analysis
* Sales Performance Analysis

  ## 📸 Dashboard Preview

### Sales Performance Overview

![Sales Performance Overview](screenshots/sales-performance-overview.png)

### Customer & Order Analysis

![Customer & Order Analysis](screenshots/customer-order-analysis.png)

### Product Performance Analysis

![Product Performance Analysis](screenshots/product-performance-analysis.png)

## 👩‍💻 Author

**Jayani Kaveesha**

B.Sc. Physical Science
University of Sri Jayewardenepura

---

⭐ If you find this project useful, feel free to explore the dashboard and data model.
