# Amazon Sales Performance Dashboard

## 📊 Introduction

This project analyzes e-commerce sales data to understand overall sales
performance, product performance, revenue trends, returns, cancellations,
and geographical performance.

The dataset contains **100,000 synthetic Amazon e-commerce orders from 2020–2024**.

I created an interactive Excel dashboard to provide a descriptive overview
of the business and allow users to analyze performance by year.

### Dashboard

![Dashboard](https://github.com/user-attachments/assets/0b8d4d6e-05cb-44dd-8197-2981cc71f009)

---

## 📁 Excel File

My final dashboard can be found here:

[Download the Excel Dashboard](Amazon%20Sales%20Analysis%20Dashboard.xlsx)

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

I utilized the following Excel skills for the analysis:

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

## Key Performance Indicators

The dashboard contains five primary KPIs:

- **Total Orders**
- **Total Revenue**
- **Revenue Lost**
- **Return Rate**
- **Cancellation Rate**

These metrics provide a high-level overview of the sales performance of Amazon.

### Why These KPIs?

I selected these KPIs because they show both the positive and negative
sides of the sales performance.

While **Total Revenue** and **Total Orders** measure overall sales activity,
**Revenue Lost**, **Return Rate**, and **Cancellation Rate** highlight
potential areas of revenue leakage.

---

## 🔍 Analysis

### Revenue by Product Category

![Revenue by Product Category](https://github.com/user-attachments/assets/981fe2e1-5661-45e8-bedd-6c272e44a4d0)

**Insights:**
- **Electronics** generated the highest revenue at approximately **$14.0M**.
- Revenue across the other categories was relatively close, indicating that sales were fairly evenly distributed across product categories.

### Top 10 Products by Revenue

![Top 10 Products by Revenue](https://github.com/user-attachments/assets/2490a966-e428-4f9d-91d1-668307a80c00)

**Insights:**
- Identifies the products that contributed the most revenue.
- Highlights the strongest individual product performers.

### Bottom 10 Products by Revenue

![Bottom 10 Products by Revenue](Bottom_10_Products.png)

**Insights:**
- Identifies the lowest revenue-generating products.
- These products may require further investigation to understand their lower performance.

### Revenue by Month

![Revenue by Month](Revenue_by_Month.png)

**Insights:**
- Revenue fluctuated throughout the year.
- The analysis highlights the strongest and weakest sales months.

### Revenue by Country

![Revenue by Country](Revenue_by_Country.png)

**Insights:**
- Shows how revenue was distributed geographically.
- Highlights the markets contributing the most revenue.
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
