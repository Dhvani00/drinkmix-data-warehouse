# 🍹 DrinkMix Data Warehouse

A complete Data Warehouse implementation for a beverage retail chain built with Oracle SQL.

This project demonstrates the design and implementation of a dimensional Data Warehouse, including data integration, ETL processes, data cleansing, deduplication, and analytical reporting across multiple heterogeneous source systems.

---

## 📖 Project Overview

The DrinkMix retail chain operates several independent branch databases with different data structures and formats. The goal of this project was to consolidate customer, product, and sales data into a centralized Data Warehouse that supports business intelligence and analytical reporting.

The solution was implemented using a ⭐ Star Schema architecture and Oracle SQL.

---

## 🚀 Key Features

### 🔄 Data Integration

- Integrated data from 3 independent branch systems
- Unified heterogeneous customer, product, and sales structures
- Standardized inconsistent source data

### ⚙️ ETL Pipeline

- Customer deduplication across branches
- Address normalization
- Product category harmonization
- Data cleansing and transformation
- Loading into dimensional tables

### 🏗️ Dimensional Modeling

Implemented a Star Schema consisting of:

- 👤 Customer Dimension
- 🥤 Product Dimension
- 📅 Time Dimension
- 🏪 Branch Dimension
- 📊 Fact Sales

### 📈 Business Analytics

Supports analysis by:

- Product Category
- Customer Demographics
- Age Group
- Gender
- Region
- Day / Week / Month / Quarter / Year
- Sales Volume
- Revenue (Turnover)

---

## 🏛️ Data Warehouse Architecture

### Dimensions

| Dimension | Description |
|------------|------------|
| 👤 Customer | Customer master data and demographics |
| 🥤 Product | Product information, category, size and price |
| 📅 Time | Day, week, month, quarter and year |
| 🏪 Branch | Branch and regional information |

### Fact Table

| Measure |
|----------|
| 📊 Quantity Sold (Liters) |

---

## 🧹 ETL Challenges Solved

### 👥 Customer Matching

Customers appearing in multiple branch systems were identified and merged using:

- First Name
- Last Name
- Street
- House Number
- ZIP Code
- City

### 🔧 Product Standardization

| Source Value | Warehouse Value |
|-------------|----------------|
| Alkoholisch | Alcoholic |
| Alkoholfrei | Non-Alcoholic |

### ✅ Data Quality Improvements

- Duplicate customer detection
- Attribute normalization
- Address parsing and standardization
- Missing value handling

---

## 📊 Results

| Metric | Value |
|---------|---------|
| 👥 Integrated Customers | 141,753 |
| 🥤 Unique Products | 65 |
| 📈 Sales Transactions | 212,622 |
| 🏪 Branch Systems | 3 |
| 🌍 Regions | 3 |

---

## 🛠️ Technologies

- Oracle SQL
- Data Warehousing
- ETL
- Star Schema
- Dimensional Modeling
- Data Cleansing
- Data Integration
- Business Intelligence

---

## 📂 Repository Structure

```text
sql/
├── create_dimensions.sql
├── create_fact_table.sql
├── create_views.sql
├── etl_customers.sql
├── etl_products.sql
├── etl_sales.sql
└── analytics.sql

docs/
├── StarSchema.png
└── MER_Diagramodel.png

screenshots/
├── customer_dimension.png
├── fact_table.png
└── analytics_results.png
