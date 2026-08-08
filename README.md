# Amazon Sales Performance Dashboard

## 📊 Introduction

This project analyzes e-commerce sales data to understand overall sales
performance, product performance, revenue trends, returns, cancellations,
and geographical performance.

The dataset contains **100,000 synthetic Amazon e-commerce orders from 2020–2024**.

I created an interactive Excel dashboard to provide a descriptive overview
of the business and allow users to analyze performance by year.

### Dashboard

![Dashboard 2](https://github.com/user-attachments/assets/0b8d4d6e-05cb-44dd-8197-2981cc71f009)

---

## 📁 Excel File

My final dashboard can be found here:

👉 [Download the Excel Dashboard](E-Commerce-Sales-Performance-Dashboard.xlsx)

---

## 🎯 The Questions I Wanted To Answer

To understand the performance of the e-commerce business, I focused on
the following questions:

1. How much revenue did the business generate?
2. How many orders were placed?
3. How much revenue was lost through returned and cancelled orders?
4. What percentage of orders were returned?
5. What percentage of orders were cancelled?
6. Which product categories generated the most revenue?
7. Which individual products generated the most revenue?
8. Which products generated the least revenue?
9. How did revenue change throughout the year?
10. Which countries generated the most revenue?

---

## 🛠️ Excel Skills Used

The following Excel skills were utilized for analysis:

- 📊 **Pivot Tables**
- 📈 **Pivot Charts**
- 🧮 **DAX**
- 🔗 **Power Pivot**
- 🧹 **Power Query**
- 🎛️ **Slicers**
- 🗺️ **Map Charts**
- 🔍 **Data Cleaning**
- 📉 **Data Visualization**
- 📊 **Dashboard Design**

---

# 📊 Dashboard Analysis

## 1. Key Performance Indicators

The dashboard contains five primary KPIs:

- **Total Orders**
- **Total Revenue**
- **Revenue Lost**
- **Return Rate**
- **Cancellation Rate**

These metrics provide a high-level overview of the performance of the
e-commerce business.

### Why These KPIs?

I selected these KPIs because they show both the positive and negative
sides of sales performance.

While **Total Revenue** and **Total Orders** measure overall sales activity,
**Revenue Lost**, **Return Rate**, and **Cancellation Rate** highlight
potential areas of revenue leakage.

---

## 2. Revenue by Product Category

![Revenue by Product Category](assets/revenue_by_category.png)

### Insights

This analysis compares revenue generated across the different product
categories.

It helps identify:

- The highest revenue-generating categories
- The lowest revenue-generating categories
- How evenly revenue is distributed across categories

One important observation is that category revenues are relatively close,
suggesting that revenue is not heavily dependent on a single product
category.

---

## 3. Top 10 Products by Revenue

![Top 10 Products](assets/top_10_products.png)

### Insights

This chart identifies the ten products generating the highest revenue.

Analyzing individual products alongside product categories provides a
more detailed understanding of which specific products contribute most
to sales.

This information could help the business identify products that deserve
greater inventory or marketing attention.

---

## 4. Bottom 10 Products by Revenue

![Bottom 10 Products](assets/bottom_10_products.png)

### Insights

This analysis identifies products generating the lowest revenue.

These products may require further investigation to determine whether
their performance is related to:

- Low customer demand
- Pricing
- Product positioning
- Limited marketing
- Inventory availability

Since this project focuses on **descriptive analysis**, the dashboard
identifies the underperforming products but does not establish the cause
of their performance.

---

## 5. Revenue by Month

![Revenue by Month](assets/revenue_by_month.png)

### Insights

The monthly revenue analysis shows how sales performance changes
throughout the year.

This makes it possible to identify:

- Strong revenue months
- Weak revenue months
- Potential seasonal patterns
- Changes in sales performance over time

---

## 6. Revenue by Country

![Revenue by Country](assets/revenue_by_country.png)

### Insights

The geographical analysis shows how revenue is distributed across the
countries represented in the dataset.

This provides a quick overview of the business's strongest and weakest
markets by revenue.

---

# 🎛️ Dashboard Interactivity

A **Year slicer** was added to allow users to filter the entire dashboard
between:

- 2020
- 2021
- 2022
- 2023
- 2024

Selecting a year dynamically updates the KPIs and visualizations,
allowing sales performance to be compared across different periods.

---

# 🧮 Key Calculations

Several measures were created to support the analysis.

### Total Orders

```DAX
Total Orders =
DISTINCTCOUNT(Amazon[OrderID])
```

### Total Revenue

```DAX
Total Revenue =
CALCULATE(
    SUM(Amazon[TotalAmount]),
    Amazon[OrderStatus] = "Delivered"
)
```

> Replace this formula with your exact DAX measure if your revenue
> definition includes other order statuses.

### Return Rate

```DAX
Return Rate =
DIVIDE(
    [Returned Orders],
    [Total Orders],
    0
)
```

### Cancellation Rate

```DAX
Cancellation Rate =
DIVIDE(
    [Cancelled Orders],
    [Total Orders],
    0
)
```

---

# 🔍 What I Learned

This project strengthened my understanding of how Excel can be used
beyond spreadsheets for business data analysis.

I gained practical experience in:

- Transforming raw transactional data into business KPIs
- Creating DAX measures
- Working with Pivot Tables and Pivot Charts
- Designing interactive dashboards
- Using slicers to dynamically filter reports
- Selecting appropriate visualizations for different business questions
- Presenting analytical results in a clear and concise format
- Distinguishing between descriptive findings and assumptions about
  why those results occurred

---

# 💡 Conclusion

The E-Commerce Sales Performance Dashboard provides a descriptive
overview of sales performance between **2020 and 2024**.

The analysis examines revenue, order volume, product performance,
geographical performance, monthly trends, returns, cancellations,
and revenue losses.

The interactive dashboard allows users to explore these metrics by year
and quickly identify patterns in the business's historical performance.

This project demonstrates how **Microsoft Excel can be used to transform
large transactional datasets into an interactive business intelligence
dashboard.**
