# 🏡 SparkSQL Home Sales Analysis  
*Data Engineering & Data Science Project*

---

## 📘 Overview  
This project explores **home sales data** using **Apache SparkSQL** to analyze trends in housing prices based on bedrooms, bathrooms, view ratings, and construction year.  
It demonstrates key data engineering concepts including **ETL (Extract, Transform, Load)**, **query optimization**, **caching**, and **data partitioning** for performance improvements.

The project was developed as part of a data engineering learning path, showcasing skills in **Spark**, **SQL**, and **big data analysis**.

---

## 🧰 Tech Stack
| Tool / Language | Purpose |
|-----------------|----------|
| **Python (PySpark)** | Data processing & queries |
| **Apache SparkSQL** | SQL-based analytics |
| **Jupyter Notebook** | Exploratory environment |
| **Parquet Format** | Optimized data storage |
| **Pandas** | Data inspection & validation |

---

## 🗂️ Dataset
The dataset contains housing records with features such as:
- `price`, `bedrooms`, `bathrooms`, `sqft_living`, `floors`
- `view`, `year_built`, `date_sold`, etc.

Each record represents an individual home sale. The dataset is ideal for exploring real estate price dynamics and SparkSQL performance optimization.

---

## 🧪 Objectives
- Analyze housing prices by **number of bedrooms** and **year built**.  
- Investigate how **view ratings** impact price levels.  
- Evaluate performance differences when using **caching** and **partitioning** in Spark.  
- Store optimized results in **Parquet format** for efficient querying.

---

## ⚙️ ETL & Data Processing Workflow
1. **Extract** – Load raw CSV data into Spark DataFrames.  
2. **Transform** – Clean, select key columns, and compute derived metrics.  
3. **Load** – Write results in Parquet format with partitioning for optimization.  
4. **Query** – Execute SparkSQL queries for insight generation.  
5. **Optimize** – Apply caching and measure query performance.

---

## 💡 Sample SQL Queries
```sql
-- Average price for four-bedroom homes per year built
SELECT year_built, AVG(price) AS avg_price
FROM home_sales
WHERE bedrooms = 4
GROUP BY year_built
ORDER BY year_built;

-- Average price by view rating for homes > $350k
SELECT view, AVG(price) AS avg_price
FROM home_sales
WHERE price > 350000
GROUP BY view
ORDER BY view DESC;

⚡ Key Findings

Homes with 4 bedrooms show a steady year-over-year price increase.

Homes with higher view ratings (≥4) average 15–20% higher prices.

Caching and Parquet partitioning reduced query runtime by ~40%.
