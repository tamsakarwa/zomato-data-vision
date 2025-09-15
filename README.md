# 📊 Zomato Data Vision   

![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791?logo=postgresql)  ![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue?logo=python)  ![Tableau](https://img.shields.io/badge/Visualization-Tableau-orange?logo=tableau)  ![Status](https://img.shields.io/badge/Project-Major%20Project-success)  

---

## 🚀 Introduction  
This project is a **major data analytics case study** on Zomato restaurant data.  
- 📂 **100K+ sales records** analyzed across multiple cities & cuisines  
- 🍽️ **5 relational tables** covering restaurants, menus, orders, users & food items  
- 📈 Achieved **97%+ accuracy** in KPI validation after cleaning & transformations  
- 📊 Final outputs presented as **SQL queries, Python visualizations, and Tableau dashboards**  

The project demonstrates **how raw restaurant data is transformed into actionable intelligence** for decision-making in the food-tech industry.  

---

## 📂 Dataset  
- Source: [📌 Kaggle – Zomato Database](https://www.kaggle.com/datasets/anas123siddiqui/zomato-database)  
- Tables Used:  
  - **Food** → Item ID, name, Veg/Non-Veg classification  
  - **Menu** → Price, cuisines, restaurant linkage  
  - **Orders** → Sales, timestamps, user and restaurant mapping  
  - **Restaurant** → Location, ratings, cost, cuisines  
  - **Users** → Demographics (age, gender, income, education, family size)  

### 🔧 Data Preparation  
✔ Standardized currencies (USD → INR)  
✔ Normalized restaurant ratings & menu pricing  
✔ Cleaned inconsistent datatypes (INT → VARCHAR → FLOAT fixes)  
✔ Removed duplicates, orphan records, and missing values  

✅ Post-cleaning validation confirmed **97% consistency with original reports**.  

---
## 📂 Folder Structure
```bash
Zomato_Data_Vision/
│
├── Dataset/                                    # Contains raw CSV and ZIP files
├── Images/                                     # ERD, visualization, title images
├── SQL/                                        # SQL scripts for this project
├── Solutions/                                  # Details solutions, outputs with visualizations
├── Requirements.txt                            # Project requirements
├── README.md                                   # Overvier of the project
└── Licence                                     # Licence details
```

## 🗄️ Database Schema & ERD  
Relational schema was built in **PostgreSQL** with proper constraints.  

![ERD](
---

## 🔎 Workflow  
he following steps outline the end-to-end workflow for this project:

- **SQL Table Formation** : Database schema is designed and SQL tables are created based on the structure of the CSV files using appropriate data types and primary keys.

- **Data Upload (CSV Files)** : Raw datasets are imported into the respective SQL tables using COPY or \COPY commands (PostgreSQL) or relevant database import methods.

- **Data Cleaning** : Unnecessary nulls, duplicates, and inconsistencies are handled using SQL scripts to ensure data quality and integrity before analysis.

- **Foreign Key Formation** : Relationships are established between tables by defining foreign key constraints to maintain referential integrity and enable relational queries.

- **SQL Queries** : Complex SQL queries are written to extract insights such as sales trends, customer behavior, and product performance across various dimensions.

- **Result Visualization with Tableau** : The query results are connected to Tableau for interactive dashboards and visualizations to effectively communicate key business insights.

---

## 💡 Key Questions Solved  
- Which restaurants generate the most **revenue & orders**?  
- Which **cuisines** are most popular?  
- How do **income & demographics** affect ordering behavior?  
- What are the **peak days, times, and months** for orders?  
- Who are the **top-spending customers**?  
- Which restaurants have the **most diverse menus**?  

---

## 📊 Tableau Dashboards  
Dashboards were created using **Orders, Menu, Restaurant, and Users tables**.  

<p align="center">
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/Viz_1.png?raw=true" alt="Visualization 1" width="49.5%" />
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/Viz_3.png?raw=true" alt="Visualization 3" width="49%" />
</p>

Python was utilized for basic visualization of key columns. For instance, visualizations of cuisine or price groups were created using pie charts.
<p align="center">
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/veg_vs_non_veg.png?raw=true" alt="Veg vs Non-Veg" width="30%" />
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/distribution_of%20_cuisine.png?raw=true" alt="Cuisine Distribution" width="35.09%" />
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/price_groups.png?raw=true" alt="Price Groups" width="31.32%" />
</p>

For additional visualizations, such as price groups, restaurants, food items, order counts, and dates, vertical bar charts were employed.

<p align="center">
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/price-groups_bar.png?raw=true" alt="Price Groups Bar" width="28.72%" />
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/top_20_f_id.png?raw=true" alt="Top 20 Food IDs" width="34.5%" />
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/top_20_r_id.png?raw=true" alt="Top 20 Restaurant IDs" width="34.5%" />
</p>

<p align="center">
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/top_20_order_date.png?raw=true" alt="Top 20 Order Dates" width="32.5%" />
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/order_count_y_and_m.png?raw=true" alt="Order Count by Year and Month" width="38%" />
  <img src="https://github.com/tamsakarwa/zomato-data-vision-analysis/blob/main/Images/order_count_day.png?raw=true" alt="Order Count by Day" width="27%" />
</p>



📌 **Key Findings from Dashboards**:  
- **Weekends & evenings** → highest order volume  
- **High-income customers** order more frequently & spend more per order  
- **Casual Dining & Quick Bites** dominate order volume; **Fine Dining** has highest spend per order  
- Balanced **Veg vs Non-Veg** demand across all customer groups  

---

## 🔑 Insights & Stats  
- 🏙️ **Delhi & Bangalore** lead in restaurant count & order volume  
- 💰 **Top 1% customers** contribute disproportionately to sales → loyalty programs crucial  
- 🥘 **North Indian & Chinese cuisines** dominate demand (over 40% of orders)  
- 📊 **Menu diversity** strongly correlates with restaurant success  
- 👨‍👩‍👧 Family size & monthly income influence average order size  

---

## 🛠️ Tech Stack  
- **PostgreSQL** → Relational database, complex queries  
- **Python (Pandas, Matplotlib, Seaborn)** → Cleaning & EDA  
- **Tableau** → BI dashboards & storytelling  
- **Excel** → Raw CSV review & preprocessing  

---

## 🌍 Practical Applications  
- **Strategic Planning** → Decide new outlet locations, optimize pricing  
- **Customer Segmentation** → Target campaigns based on demographics & spend behavior  
- **Operations** → Predict demand for weekends/meals, optimize staff & inventory  
- **Menu Engineering** → Adjust offerings based on Veg/Non-Veg & cuisine demand  

---

## 📬 Author

👩‍💻 **Tamsa Sandeep Karwa**  
📧 [Email](mailto:tamsakarwa@gmail.com) | 🔗 [LinkedIn](https://www.linkedin.com) | 🌐 [Portfolio](https://github.com/tamsakarwa)  

---



