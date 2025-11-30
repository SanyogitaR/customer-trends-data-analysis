# 🛒 Customer Shopping Behavior Analysis

## 📌 Project Overview
This project explores **customer shopping behavior** using transactional data from 3,900 purchases across multiple product categories.  
The goal is to derive insights about spending patterns, customer demographics, shipping preferences, loyalty behavior, and product performance to support data-driven business decisions.



## 📊 Dashboard Preview
<!-- Add your dashboard image here -->
![Dashboard Preview](dashboard.png)



## 📂 Dataset Summary
- **Rows:** 3,900  
- **Columns:** 18  
- **Contains:**
  - Customer demographics: `age`, `gender`, `location`, `subscription_status`
  - Purchase details: `item_purchased`, `category`, `purchase_amount`, `season`, `size`, `color`
  - Behavioral metrics: `discount_applied`, `previous_purchases`, `frequency_of_purchases`, `review_rating`, `shipping_type`
- **Missing Values:** 37 in `review_rating`



## 🧹 Exploratory Data Analysis (Python)

### ✔ Data Cleaning Steps
- Loaded dataset using **Pandas**
- Inspected structure using `df.info()` and summary stats using `df.describe()`
- Imputed missing `review_rating` values with **median rating by category**
- Renamed columns to **snake_case**
- Dropped redundant column: `promo_code_used`

### ✔ Feature Engineering
- Created **age_group** from age bins  
- Created **purchase_frequency_days** from timestamps  
- Verified data consistency across discount fields

### ✔ Database Integration
- Connected cleaned dataset to **PostgreSQL** using SQLAlchemy  
- Loaded records into a database table for SQL-based business analysis  



## 🧮 SQL Business Analysis
Key analyses performed using PostgreSQL:

1. **Revenue by Gender**  
2. **High-Spending Customers Who Used Discounts**  
3. **Top 5 Products by Average Rating**  
4. **Shipping Type vs. Average Purchase Amount**  
5. **Subscribers vs. Non-Subscribers (Revenue + Avg Spend)**  
6. **Products Most Dependent on Discounts**  
7. **Customer Segmentation:** New, Returning, Loyal  
8. **Top 3 Purchased Products in Each Category**  
9. **Subscription Likelihood of Repeat Buyers (>5 purchases)**  
10. **Revenue Contribution by Age Group**

_All SQL queries are included inside the `sql_queries/` folder._



## 📈 Power BI Dashboard
A fully interactive Power BI dashboard includes:

- Revenue breakdowns by **gender, age group, subscription status**
- **Top products**, **category performance**, **ratings overview**
- Shipping type comparison (Standard, Express, Free Shipping)
- Filters for:
  - Category  
  - Season  
  - Shipping Type  
  - Subscription Status  



## 💡 Business Recommendations
- **Promote subscription benefits** to increase customer lifetime value  
- **Launch loyalty programs** to retain returning buyers  
- **Reevaluate discount policies** to control margin loss  
- **Highlight top-rated and bestselling products** in campaigns  
- **Target high-revenue age groups & express-shipping users**  
 





