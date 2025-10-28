# 📊 E-Commerce Sales Analytics | Python + SQL
This project analyzes retail sales performance to uncover revenue drivers, customer value insights, and operational inefficiencies.
Using real Superstore sales data, the goal is to support business decision-making with data-driven insights.


## 🔍 Project Objectives
1. Identify top-performing product categories and regions
2. Analyze how discounting impacts profitability
3. Evaluate shipping performance and delays
4. Discover high-value customers for retention strategies


| Skill Category    | Highlights                                  |
| ----------------- | ------------------------------------------- |
| Programming       | Python (Pandas, Seaborn, Matplotlib)        |
| Data Manipulation | Data cleaning, feature engineering          |
| Database          | MySQL integration (upcoming)                |
| Business Insights | Profitability, demand & operations analysis |
| Version Control   | GitHub repository management                |
| Notebooks         | Google Colab for analysis                   |


## 📁 Project Structure
ecommerce-sales-analytics
├── data_raw/           # original dataset
├── data_cleaned/       # cleaned dataset
├── notebooks/          # Jupyter notebooks
│   ├── 01_data_cleaning.ipynb
│   └── 02_EDA_and_Insights.ipynb
└── README.md


## ✅ Work Completed So Far
✔ Data imported & cleaned
✔ Enhanced dataset with:
• Shipping delay metric
• Profit margin percentage
✔ Exploratory Data Analysis completed
✔ Business insights derived from visualizations


## 🔮 Upcoming Work
• Monthly trend dashboards
• Top customer profitability analysis
• SQL querying for deeper metrics
• Final business recommendation report
• Streamlit dashboard 


## 📈 Key Insights
• Technology category delivers best revenue + profit combo
• Discounts have a negative impact on profit
• Standard shipping shows more delays than Express modes
• Central & West regions lead performance; South has opportunity for growth


## 📦 Dataset Source
Superstore Sales Dataset (Kaggle)
🔗 https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

## 👩‍💻 Author
Sri Gayatri Nandikanti

[LinkedIn] (https://www.linkedin.com/in/sri-gayatri-nandikanti-8a1128242/)


## 💡 Hire Me
Actively seeking Data Analyst / Python Developer opportunities.


## 📊 Visual Insights Preview

| Profit by Category | Profit by Region |
|------------------|-----------------|
| ![Profit Category](images/profit_by_category.png) | ![Profit Region](images/profit_by_region.png) |

| Shipping Delay vs Profit |
|------------------------|
| ![Shipping Delay](images/shipping_delay_vs_profit.png) |


## 🧠 Business Insights & Decisions

Here are key insights that can drive strategic decisions:

1️⃣ **Technology category generates the highest profit**  
• Prioritize marketing + inventory investment here  

2️⃣ **Central and West regions are more profitable than South**  
• Expand logistics + target customer campaigns in high-performing regions

3️⃣ **Large discounts often lead to losses**  
• Implement smarter discounting rules  
• Focus on profitability, not sales volume only

4️⃣ **Shipping delays reduce profit**  
• Review carrier performance  
• Faster fulfillment = better customer satisfaction and earnings


## 🗂️ SQL Analysis

SQL was used to validate insights extracted from Python EDA.
A SQLite database was created from the cleaned dataset and queries were executed to analyze sales and profit performance.
✅ Queries Executed
-- 1️⃣ Total Sales and Profit by Category
SELECT Category,
       ROUND(SUM(Sales), 2) AS Total_Sales,
       ROUND(SUM(Profit), 2) AS Total_Profit
FROM Orders
GROUP BY Category
ORDER BY Total_Profit DESC;
-- 2️⃣ Profit by Region
SELECT Region,
       ROUND(SUM(Profit), 2) AS Total_Profit
FROM Orders
GROUP BY Region
ORDER BY Total_Profit DESC;
-- 3️⃣ Impact of Shipping Delays on Profit
SELECT CASE
         WHEN "Ship Delay (Days)" > 3 THEN 'Delayed'
         ELSE 'On-Time'
       END AS Shipping_Status,
       ROUND(AVG(Profit), 2) AS Avg_Profit
FROM Orders
GROUP BY Shipping_Status;

## 📌 Results
✅ SQL results exported as CSVs for reference:
📁 SQL_outputs/category_profit_sql.csv
📁 SQL_outputs/region_profit_sql.csv
📁 SQL_outputs/shipdelay_profit_sql.csv


## 🧠 Conclusion
✔ Technology category drives highest profit
✔ Central & West regions outperform others
✔ High discounting reduces profitability
✔ Shipping delays have a negative business impact

These findings help guide pricing strategy, regional planning, and logistics improvements.
