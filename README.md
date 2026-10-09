# Chocolate Sales Intelligence Dashboard

## 📌 Project Overview

The **Chocolate Sales Intelligence Dashboard** is an interactive Power BI project designed to analyze chocolate sales performance across products, brands, categories, countries, and stores for FY 2023–2024.

The dashboard helps understand revenue generation, profitability, customer distribution, and sales trends. It transforms raw sales data into actionable business insights to support data-driven decisions related to product performance, regional sales opportunities, and business growth.

## Business Objectives

* Monitor key performance indicators such as total revenue, total profit, profit margin, orders, and customers.
* Identify top-performing and underperforming chocolate categories, products, and brands.
* Compare revenue performance across countries and profitability across stores.
* Analyze monthly revenue trends and identify unusual fluctuations.
* Explore sales performance across customer types, gender, and cocoa percentages.

## Tools & Technologies

* **Power BI Desktop** - Dashboard development and data visualization
* **Power Query** - Data preparation and transformation
* **DAX** - KPI calculations and business metrics
* **Data Modeling** - Relationships between sales and dimension tables

## Dashboard Features

### 1. Key Performance Indicators

* Total Revenue
* Total Profit
* Profit Margin
* Total Orders
* Total Customers

### 2. Revenue by Country

Compares revenue across countries to identify leading markets and regions that may require further investigation.

### 3. Revenue by Chocolate Category

Analyzes revenue across five categories: White, Milk, Dark, Praline, and Truffle.

### 4. Revenue Trend Analysis

Compares monthly revenue across 2023 and 2024 to identify trends, fluctuations, and potential seasonal patterns.

### 5. Top Brands by Revenue

Uses a treemap to compare brand-level revenue and highlight major contributors.

### 6. Top Products by Revenue

Ranks products by revenue to identify the strongest-performing chocolate varieties.

### 7. Top Stores by Profit

Compares store profitability to identify leading stores and investigate differences in performance.

### 8. Interactive Filters

Allows users to explore the dashboard using:

* Cocoa Percent
* Customer Type
* Gender

## 💡 Key Business Insights

Based on the displayed dashboard results:

* **Category performance:** Praline leads the displayed chocolate categories in revenue, while Milk has the lowest revenue.
* **Regional performance:** Canada is the highest-revenue country among those displayed, while Germany has the lowest revenue.
* **Brand performance:** Cadbury and Ferrero are the leading brands by displayed revenue.
* **Product performance:** Dark Chocolate 50% is the highest-revenue product among the products displayed.
* **Profitability:** The dashboard reports an overall profit margin of approximately 40%.

These findings indicate areas for further investigation, including category-level profitability, regional growth opportunities, and the factors driving product and brand performance. They are descriptive observations, not proof of the underlying causes.

## Data Model

The project uses a sales fact table supported by dimension tables.

| Table       | Purpose                                                                |
| ----------- | ---------------------------------------------------------------------- |
| `sales`     | Transaction-level sales, quantity, revenue, cost, profit, and discount |
| `products`  | Product names, categories, brands, cocoa percentages, and weights      |
| `customers` | Customer attributes, loyalty status, and join dates                    |
| `stores`    | Store information, cities, countries, and store types                  |
| `calendar`  | Date attributes for time-based analysis                                |

The model supports analysis across products, customers, stores, and time periods.

## Key DAX Measures

```dax
Total Revenue =
SUM(sales[revenue])
```

```dax
Total Profit =
SUM(sales[profit])
```

```dax
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Revenue],
    0
)
```

```dax
Total Orders =
DISTINCTCOUNT(sales[order_id])
```

```dax
Total Customers =
DISTINCTCOUNT(sales[customer_id])
```

These measures provide the foundation for the dashboard's primary KPIs and performance comparisons.


## Skills Demonstrated

* Data cleaning and preparation
* Data modeling and relationships
* DAX measures and KPI development
* Interactive dashboard design
* Sales and profitability analysis
* Trend analysis and business insight generation
* Data-driven business recommendations

## Project Purpose

This project demonstrates the use of Power BI to turn sales data into an interactive business intelligence solution, connecting performance metrics with insights that support business analysis and decision-making.
