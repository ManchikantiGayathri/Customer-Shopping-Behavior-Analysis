# 🛒 Customer Shopping Behavior Analysis

### 📊 Overview
This project explores **customer shopping patterns and purchasing behavior** using **SQL** and **Power BI**.  
The goal is to uncover insights that help businesses understand their customers better — who buys the most, which products perform well, and how discounts, subscriptions, and shipping types affect revenue.

---

## 🎯 Objectives
- Analyze total revenue by gender and age group.  
- Identify products with the highest ratings and purchase counts.  
- Compare average spend of **subscribed vs. non-subscribed** customers.  
- Evaluate the impact of **discounts** and **shipping types** on overall revenue.  
- Build an **interactive Power BI dashboard** to visualize key business KPIs.

---

## 🧠 Key Insights
1. **Female customers contributed ~58%** of total revenue.  
2. **Subscribed customers spent 35% more on average** than non-subscribers.  
3. **Express shipping orders** had higher average purchase amounts than standard shipping.  
4. **Top 5 most reviewed products** drove nearly **40% of total sales**.  
5. **Loyal customers (5+ purchases)** showed a high likelihood of being subscribed members.

---

## 🗂️ Dataset
The dataset used (`customer_behavior.csv`) contains **6,000+ records** with the following attributes:

| Column | Description |
|:--------|:-------------|
| `Customer_ID` | Unique ID for each customer |
| `Gender` | Male / Female |
| `Age_Group` | Customer’s age category |
| `Item_Purchased` | Product name purchased |
| `Category` | Product category |
| `Purchase_Amount` | Amount spent on the purchase |
| `Discount_Applied` | Whether a discount was used (Yes/No) |
| `Shipping_Type` | Standard / Express |
| `Review_Rating` | Customer rating for the product |
| `Previous_Purchases` | Number of past purchases by the customer |
| `Subscription_Status` | Subscribed / Not Subscribed |

---

## 🧮 SQL Analysis
All queries were written in **MySQL** and executed via **Jupyter Notebook**.

Some key queries include:
- **Revenue by Gender**
  ```sql
  SELECT gender, SUM(purchase_amount) AS total_revenue
  FROM customer
  GROUP BY gender;

