# 📊 Zomato Data Analytics Project  

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

## 🗄️ Database Schema & ERD  
Relational schema was built in **PostgreSQL** with proper constraints.  

![ERD](https://github.com/ShaikhBorhanUddin/Zomato-Data-Analysis/blob/main/Images/zomato_erd.png?raw=true)  

---

## 🔎 Workflow  
1. **Schema Design** → PostgreSQL schema & data upload  
2. **Data Cleaning** → SQL scripts & Pandas transformations  
3. **Analytics** → SQL queries for KPIs & patterns  
4. **Visualization** → Dashboards in Tableau & Python charts  
5. **Insights** → Business-driven conclusions  

---

## 💡 Key Questions Solved  
- Which restaurants generate the most **revenue & orders**?  
- Which **cuisines** are most popular?  
- How do **income & demographics** affect ordering behavior?  
- What are the **peak days, times, and months** for orders?  
- Who are the **top-spending customers**?  
- Which restaurants have the **most diverse menus**?  

---

## 🧑‍💻 Sample SQL Queries  

**Top 10 Restaurants by Menu Diversity**  
```sql
SELECT r.name, COUNT(DISTINCT m.f_id) AS item_count
FROM restaurant r
JOIN menu m ON r.id = m.r_id
GROUP BY r.name
ORDER BY item_count DESC
LIMIT 10;
```  

**Order Trends by Weekday**  
```sql
SELECT TRIM(TO_CHAR(order_date, 'Day')) AS weekday,
       COUNT(*) AS total_orders,
       SUM(sales_amount) AS total_sales
FROM orders
GROUP BY weekday, EXTRACT(DOW FROM order_date)
ORDER BY EXTRACT(DOW FROM order_date);
```  

---

## 📊 Tableau Dashboards  
Dashboards were created using **Orders, Menu, Restaurant, and Users tables**.  

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Zomato-Data-Analysis/blob/main/Images/Viz_1.png?raw=true" width="49%" />
  <img src="https://github.com/ShaikhBorhanUddin/Zomato-Data-Analysis/blob/main/Images/Viz_3.png?raw=true" width="49%" />
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

## 📬 Contact  

👩‍💻 **Tamsa Sandeep Karwa**  
📧 [Email](mailto:tamsakarwa@gmail.com) | 🔗 [LinkedIn](https://www.linkedin.com) | 🌐 [Portfolio](https://github.com/tamsakarwa)  

---

✨ Explore, fork, and enhance this project to unlock deeper insights into food-tech analytics!  


