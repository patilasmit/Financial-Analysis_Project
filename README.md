# 📊 Credit Card Financial & Customer Analytics Dashboard

## 🔹 Project Summary

Built an end-to-end Credit Card Analytics Dashboard to analyze transaction behavior, customer demographics, revenue trends, and risk indicators. The dashboard enables stakeholders to monitor performance, identify high-value customers, and make data-driven decisions for growth and risk mitigation.

### 🔹 Key Business Objectives

Analyze credit card revenue & transaction trends

Understand customer demographics & spending behavior

Identify high-revenue segments & risk patterns

Track week-on-week revenue performance

### 🔹 Key Features & Analysis

✔ Revenue & transaction analysis by Quarter, Card Category & State
✔ Customer segmentation by Age Group, Income Group, Gender & Job Type
✔ Spending pattern analysis by Expense Type & Payment Method
✔ KPI tracking: Total Revenue, Interest Earned, Transaction Count
✔ Week-on-Week revenue comparison using DAX measures
✔ Interactive slicers for Time, Card Type & Customer Attributes

### 🔹 DAX & Data Modeling Highlights
Created calculated columns for Age Group & Income Group
Built custom revenue calculation combining fees, transactions & interest
Developed WoW Revenue Measures for performance tracking
Optimized model using date intelligence & filters

Revenue = 'public cc_detail'[annual_fees] + 'public cc_detail'[total_trans_amt] + 'public cc_detail'[interest_earned]

Current_week_Revenue =
CALCULATE(
    SUM('public cc_detail'[Revenue]),
    FILTER(
        ALL('public cc_detail'),
        'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2])
    )
)

### 🔹 Business Insights Delivered
📌 Blue card category contributes the highest revenue
📌 Swipe transactions dominate overall revenue share
📌 Businessman & White-collar segments generate maximum revenue
📌 Certain states consistently outperform others in transaction volume
📌 Week-on-week analysis highlights revenue fluctuations for monitoring risk

### 🔹 Outcome
This dashboard provides a 360° view of credit card business performance, helping decision-makers improve customer targeting, optimize product offerings, and strengthen risk monitoring.
