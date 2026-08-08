# Amazon Sales Performance Dashboard

## 📊 Introduction

This project aims to give a descriptive analysis on e-commerce sales data to understand overall sales
performance, product performance, revenue trends, returns, cancellations,
and geographical performance.

The dataset contains 100,000 synthetic Amazon style e-commerce orders from 2020–2024.

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

These metrics provide a high-level overview of the sales performance of the business.

### Why These KPIs?

I selected these KPIs because they show both the positive and negative
sides of the sales performance.

While Total Revenue and Total Orders measure overall sales activity,
Revenue Lost, Return Rate, and Cancellation Rate highlight
potential areas of revenue leakage.

---

## 🔍 Analysis

### Revenue by Product Category

![Revenue by Product Category](https://github.com/user-attachments/assets/d6670eb6-fafc-4334-a9be-40185151c794)

**Insights:**
- Electronics generated the highest revenue at approximately $14.0M.
- Revenue across the other categories was relatively close,
  indicating that sales were fairly evenly distributed across product categories.

### Top 10 Products by Revenue

![Top 10 Products by Revenue](https://github.com/user-attachments/assets/71167740-94d4-47c4-a22f-d63aea852557)

**Insights:**
- This shows that the LED Desk Lamp was the highest revenue generating product at approximately $1.74M.
- The Top 10 includes products from different categories, suggesting that high revenue is not concentrated around one type of product.

### Top 10 Products Contributing to Revenue Loss

![Bottom 10 Products by Revenue](https://github.com/user-attachments/assets/925d3c7c-3f0e-4818-8beb-b29bf1e8eb71)

**Insights:**
- Gaming Mouse recorded the highest revenue lost from returned and cancelled orders at approximately $148K.
- Most of the products recorded between $126K and $133K in lost revenue.

### Revenue by Month

![Revenue by Month](https://github.com/user-attachments/assets/c04e0e32-eab1-4589-ad81-a01ce0a12ce8)

**Insights:**
- January generated the highest monthly revenue at approximately $7.1M.
- Apart from the February decline, revenue remained relatively stable throughout the months of the different years, generally ranging between $6.7M and $7.1M.

### Revenue by Country

![Revenue by Country](https://github.com/user-attachments/assets/3054770f-bc2a-40f6-8e69-89d144af39bf)

**Insights:**
- The United States generated the highest revenue compared to the other countries.
- Revenue was heavily concentrated in the United States, while Canada, India, and Australia contributed considerably smaller shares.
---

# 🎛️ Dashboard Interactivity

A Year slicer was added to allow the user to filter the entire dashboard
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

Three essential measures were created to support the analysis.

### Total Orders

```DAX
=DISTINCTCOUNT(Amazon[OrderID])
```

### Revenue Losses by Products

```DAX
=CALCULATE(
	SUM('Amazon Table'[TotalAmount]),
	'Amazon Table'[OrderStatus] IN {"Returned","Cancelled"}
	)
```

### Revenue Gained by Products

```DAX
=CALCULATE(
 	SUM('Amazon Table'[TotalAmount]),
 	'Amazon Table'[OrderStatus] IN { "Shipped" ,"Delivered"}
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

---

# 💡 Conclusion

The Amazon Sales Performance Dashboard provides a descriptive
overview of sales performance between 2020 and 2024.

The analysis examines revenue, order volume, product performance,
geographical performance, monthly trends, returns, cancellations,
and revenue losses.

The interactive dashboard allows users to explore these metrics by year
and quickly identify patterns in the business's historical performance.

This project demonstrates how Microsoft Excel can be used to transform
large transactional datasets into an interactive business intelligence
dashboard.
