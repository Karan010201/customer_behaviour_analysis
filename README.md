Customer Shopping Behavior Analysis
📌 Project Overview
This project provides an end-to-end data analytics solution analyzing 3,900 consumer transactions to uncover spending patterns, customer segments, and product preferences. By leveraging an integrated pipeline—from raw data cleaning to advanced database querying and interactive business intelligence dashboards—this project delivers actionable insights designed to optimize loyalty programs, maximize subscriber conversions, and refine marketing strategies.

📊 Dataset Summary
Source: customer_shopping_behavior.csv

Size: 3,900 rows × 18 columns

Key Features:

Demographics: Age, Gender, Location, Subscription Status

Purchase Details: Item Purchased, Category, Purchase Amount (USD), Size, Color, Season

Behavioral Metrics: Review Rating, Shipping Type, Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases

🛠️ Tech Stack & Tools
Data Processing & EDA: Python (pandas, numpy, seaborn, matplotlib)

Database Management: MySQL

Database Querying: SQL (Advanced Window Functions, CTEs, Aggregations)

Business Intelligence: Power BI (DAX, Interactive Dashboards)

Reporting & Presentation: PDF Report & Gamma AI / PowerPoint

🚀 Step-by-Step Implementation
Step 1: Exploratory Data Analysis & Data Cleaning (Python)
Handled 37 missing values in the Review Rating column using median imputation grouped by product category.

Standardized column headers into clean snake_case.

Feature Engineering: * Segmented ages into logical bins (Young Adult, Adult, Middle-aged, Senior).

Dropped highly redundant attributes (promo_code_used).

Transferred the fully processed dataset directly into a relational database using sqlalchemy.

Step 2: Advanced Data Querying (SQL)
Designed and executed structured queries to isolate high-value business metrics:

Revenue Contributions: Segmented cumulative revenue by gender and age group.

Customer Behavior: Identified high-value discount seekers (customers using discounts who still spent above the average purchase amount).

Cohort Segments: Utilized CTEs and conditional logic (CASE WHEN) to categorize customer loyalty profiles based on purchase histories.

Product Insights: Applied ROW_NUMBER() OVER (PARTITION BY ...) window functions to isolate the top 3 items purchased within every product category.

Step 3: Business Intelligence & Visualization (Power BI)
Engineered an interactive executive dashboard mapping historical consumer trends.

Formulated foundational Key Performance Indicators (KPIs) to track overall performance at a glance.

Enabled real-time cross-filtering across dynamic dimensions including Subscription Status, Gender, Category, and Shipping Type.

🖥️ Dashboard Features
The interactive Power BI dashboard provides immediate visibility into operational performance:

High-Level KPIs: Total Customer Base (3.9K) | Average Purchase Amount ($59.76) | Average Review Rating (3.75)

Demographic Distributions: Revenue & Sales count breakdowns split by Age Groups and Gender.

Category Metrics: Comprehensive visualizations highlighting performance across Clothing, Accessories, Footwear, and Outerwear.

Behavioral Splits: A clear breakdown showing that while subscribers boast high average spends, non-subscribers drive 73% of overall sales volume.

📈 Key Findings & Results
The Gender Gap: Male shoppers generated 2.1× more revenue than female shoppers ($157,890 vs. $75,191).

The Subscription Opportunity: Out of all high-frequency repeat buyers (>5 previous purchases), 2,518 are non-subscribers compared to only 958 who subscribe, revealing a prime target audience for conversion campaigns.

Product Dominance: Clothing remains the largest overall revenue-generating category, driven primarily by the Young Adult age bracket.

Margin Risks: Five major products (Hat, Sneakers, Coat, Sweater, Pants) showed heavy discount dependency, with roughly 50% of their total purchases involving a markdown.

💡 Strategic Business Recommendations
Targeted Subscriptions: Launch exclusive membership perks specifically targeting the 73% non-subscriber base to build stable recurring revenue.

Loyalty Optimization: Deploy targeted email marketing and tier-based loyalty perks to incentivize Returning shoppers to progress into the highly profitable Loyal tier.

Discount Policy Audit: Review pricing and margin health for the top 5 highly-discounted products to prevent brand dilution and unnecessary profit leakage.

📁 Repository Structure
Plaintext
├── customer_shopping_behavior.csv         # Raw transactional dataset
├── customer_behaviour_analysis.ipynb      # Python Notebook for EDA & DB upload
├── customer_behavior_sql_queries.sql       # Production-ready analytical SQL script
├── customer_behaviour_dashboard.pbix      # Power BI Dashboard file
├── customer_behaviour_dashboard.pdf       # Exported static view of dashboard
├── Customer Shopping Behavior report.pdf  # Comprehensive analytical text report
└── Customer-Shopping-Behavior-Analysis.pptx # Project presentation slide deck

🔧 How to Run This Project

1. Database & Python Environment Setup
Ensure you have Python 3.x installed along with the required libraries:

Bash
pip install pandas numpy matplotlib seaborn sqlalchemy pymysql
Configure your local database connection details inside the Jupyter Notebook cell and run customer_behaviour_analysis.ipynb to clean and load the data.

2. SQL Analytics
Open customer_behavior_sql_queries.sql inside your preferred SQL workbench (MySQL, PostgreSQL, or SQL Server) and run the scripts against the generated database to extract key behavioral metrics.

3. Power BI Interactive Dashboard
Double-click customer_behaviour_dashboard.pbix to launch the workspace inside Power BI Desktop.

Click Refresh to sync the visual layouts with your newly populated local SQL database or flat file.
