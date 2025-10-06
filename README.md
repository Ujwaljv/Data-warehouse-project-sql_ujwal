# Data-warehouse-project-sql_ujwal
# Building a Modern Data Warehouse with Medallion Architecture

In today's data-driven world, businesses rely on clean, consistent, and well-modeled data to make informed decisions.  
As part of my portfolio, I built a **Data Warehouse project** that demonstrates the complete journey — from raw source data to actionable insights — following industry best practices in **data engineering and analytics**.  

This project simulates a real-world enterprise scenario with multiple source systems, data integration, and analytics-ready modeling.  

---

## 🚀 Project Overview  

The source data came from two systems:  

**CRM System (Customer Relationship Management)**  
- `cust_info.csv`  
- `prd_info.csv`  
- `sales_details.csv`  

**ERP System (Enterprise Resource Planning)**  
- `cust_az.csv`  
- `loc_a101.csv`  
- `px_cat_g1v1.csv`  

**Goal:**  
To design a modern data warehouse using the **Medallion Architecture** (Bronze → Silver → Gold layers), build ETL pipelines, and prepare data models for analytics.  

---

## 🏗️ Data Architecture: Medallion Approach  
<img width="1544" height="912" alt="image" src="https://github.com/user-attachments/assets/97cc96ec-c202-4eeb-b3e4-07d7e98fd589" />

### 🔹 Bronze Layer – Raw Data Ingestion  
- Created staging tables for each CSV file.  
- Loaded data using **bulk insert** methods.  
- Data remained in its **raw, unprocessed form** to preserve source integrity.  

### 🔹 Silver Layer – Data Cleaning & Transformation  
- Applied transformations on each table, including:  
  - Trimming strings  
  - Handling missing values (replacing blanks with `"N/A"`)  
  - Standardizing date formats (converted `varchar → date`, extracted `year` & `month`)  
- Produced **cleaned and standardized tables**, ready for integration.  

### 🔹 Gold Layer – Business-Ready Data Models  
- Integrated and modeled data into **analytical views**:  
  - **Customer View** → Combined data from `cust_info`, `cust_az`, and `loc_a101`.  
  - **Product View** → Merged details from `prd_info` and `px_cat_g1v1`.  
  - **Sales View** → Standardized and cleaned transactional data from `sales_details`.  
- Ensured **data consistency**, removed duplicates, and validated relationships across entities.  

---

## 📊 Data Modeling  
<img width="1522" height="861" alt="image" src="https://github.com/user-attachments/assets/dc162aa8-e5b7-4ca7-a0d7-170da0c7efa1" />

The **Gold Layer** was structured into **fact and dimension tables** following a **star schema** approach:  

- **Dimension Tables**: Customers, Products, Locations  
- **Fact Table**: Sales Transactions  

This design supports **fast analytical queries** and reporting.  

---

## 📈 Analytics & Reporting  

With the Gold layer in place, I created **SQL-based reports and dashboards** to answer key business questions such as:  

- Customer demographics and location insights  
- Product performance analysis  
- Sales trends by time period  

The warehouse now serves as a **single source of truth**, ensuring reliable insights for decision-making.  

---

## 🔑 Key Takeaways  

- **End-to-End Pipeline**: From raw CSVs to a production-ready data warehouse.  
- **Medallion Architecture**: Clean separation of raw, curated, and business-ready data.  
- **Data Quality First**: Handling missing values, standardizing formats, and ensuring consistency.  
- **Scalable Design**: Fact and dimension modeling for efficient analytics.  

This project highlights the **core principles of modern data engineering** and demonstrates how raw operational data can be transformed into actionable insights.  

---

## 💡 Closing Thoughts  

Building this project gave me hands-on experience with the **complete data warehousing lifecycle** — from ingestion to analytics.  
It showcases my ability to design data pipelines, model data effectively, and deliver insights, which are critical skills for **data engineering and analytics roles**.  

---

