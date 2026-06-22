# Customer Shopping Behavior Analysis 🛒📊

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=Jupyter&logoColor=white)

## 📌 Project Overview
A leading retail company is seeking to better understand its customers' shopping behaviors to improve sales, enhance customer satisfaction, and drive long-term loyalty. This project analyzes transactional data to uncover critical factors—such as discounts, product reviews, seasonal trends, and payment preferences—that drive consumer decision-making and repeat purchases.

This repository contains an end-to-end data analysis pipeline leveraging **Python**, **SQL**, and **Power BI** to extract insights, segment customers, and deliver actionable business recommendations.

## 📂 Dataset Summary
The analysis is based on a dataset of **3,900 purchases** across multiple product categories.
* **Customer Demographics:** Age, Gender, Location, Subscription Status
* **Purchase Details:** Item Purchased, Category, Purchase Amount (USD), Season, Size, Color
* **Shopping Behavior:** Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

## 🛠️ Tech Stack & Methodology
1. **Data Preparation & ETL (Python):** * Handled missing values (e.g., imputing missing Review Ratings using category medians).
   * Standardized nomenclature to snake_case for seamless database integration.
   * Engineered new features: `age_group` (binned demographics) and `purchase_frequency_days` (numeric mapping).
   * Automated the data loading process into a PostgreSQL database using `SQLAlchemy`.
2. **Data Analysis & Querying (PostgreSQL):** * Designed 10 advanced SQL queries to extract business metrics, including revenue segmentation, shipping comparisons, and repeat buyer behaviors.
3. **Data Visualization (Power BI):** * Built an interactive dashboard to visualize key performance indicators (KPIs), demographic splits, and revenue distributions.

## 📊 Key Findings & Business Insights
* **Customer Base & Revenue:** The dataset features 3.9K customers with an average purchase amount of **$59.76** and an average review rating of **3.75**.
* **Subscription Impact:** Non-subscribers make up 73% of the customer base, yet subscribers present a highly consistent revenue stream that can be further optimized.
* **Discount Dependency:** Nearly 50% of purchases for top-selling items (like Hats, Sneakers, and Coats) are dependent on discounts, impacting overall profit margins.
* **Customer Segmentation:** The vast majority of customers fall into the "Loyal" segment (based on historic purchase counts), with distinct revenue concentrations in the "Young Adult" and "Middle-aged" demographics.

## 💡 Strategic Recommendations
1. **Boost Subscriptions:** Introduce exclusive perks (e.g., complimentary Express shipping) to incentivize the 73% of non-subscribers to upgrade.
2. **Refine Discount Policies:** Given the high discount dependency on specific product categories, reevaluate discount frequency to balance volume boosts with margin control.
3. **Enhance Loyalty Programs:** Implement tiered rewards to actively transition "Returning" buyers into the highly profitable "Loyal" segment.
4. **Targeted Marketing:** Focus marketing spend and premium product placements on the highest-revenue age groups (Young Adults and Middle-aged).

## 📁 Repository Structure
```text
├── Customer_Shopping_Behavior_Analysis.ipynb  # Primary Python notebook for EDA & DB Loading
├── Demo.ipynb                                 # Secondary notebook demonstrating ETL steps
├── customer_behavior_sql_queries.sql          # Advanced SQL queries for business analysis
├── customer_behavior_dashboard.pbix           # Interactive Power BI dashboard file
├── Customer Shopping Behavior Analysis.pdf    # Comprehensive project report
├── Business Problem Document.pdf              # Initial business case and requirements
└── README.md                                  # Project documentation

How to Run the Project:
Python ETL: Open Customer_Shopping_Behavior_Analysis.ipynb in Jupyter Notebook. Ensure you have your local PostgreSQL credentials configured. Run the cells to clean the data and push the table to your local database.

SQL Analysis: Open customer_behavior_sql_queries.sql in pgAdmin (or your preferred SQL IDE) and execute the queries against the newly created customer table.

Power BI Dashboard: Open customer_behavior_dashboard.pbix in Power BI Desktop to interact with the visualizations. (Note: Update the data source settings to point to your local PostgreSQL server if necessary).
