# PowerBI - E-commerce Data Transformation and Data Modeling
<img width="556" height="249" alt="image" src="https://github.com/user-attachments/assets/e64f2310-16e3-4891-bbef-d903fb68f88c" />

# 📊 E-Commerce Analysis Using Power BI
Analyze product order distributions, category profit margins, and sub-category sales performance to identify key growth drivers and optimize the store's product portfolio.

## 📑 Table of Contents
* [Project Overview](#-project-overview)
* [Data Sources & Architecture](#-data-sources--architecture)
* [Data Transformation ETL](#-data-transformation-etl)
* [Data Model DAX](#-data-model-dax)
* [Key Insights](#-key-insights)
* [How To Use](#-how-to-use)

---

## 🎯 Project Overview

* **Business Problem:** Analyze product order distributions, category profit margins, and sub-category sales performance to identify key growth drivers and optimize the store's product portfolio.
  
* **Objective:** This project focuses on organizing, analyzing, from a different type of datasets. The data sets are Sales Target, List of Order, Order Details. Using Power BI tool, the workflow transforms raw datasets into a structured summary.
  
* **Target Audience:** To increase the sales perfomance and the primary user as customer.

## 🗃️ Data Sources & Architecture

* **Source Systems:** Local CSV files.
  
* **Storage Mode:** Specify if using Import, Direct Query, or Composite mode.

## ⚙️ Data Transformation (ETL)

* **Tool Used:** Power Query Editor.
  
* **Key Cleanups:** Standard transformations applied to raw data as,

   * Clean, Trim, Data type change, Remove duplicate, Group by aggregation, Manage relationship.

## 🧠 Data Model & DAX

* **Model Type:** Snowflake schema design
  
* **Fact Tables:** Sales Target table as primary transactional tables.
  
* **Dimension Tables:** List of order and Order details are dimension table.

* **Aggergation Table:** Group by category order details, Group By Sub-category Order details tables are aggergation table.

* **Key Measures:**
  ```dax
  Count of order Id = COUNTA('Dupicate Order Details'[Order ID])
  ```
  ```dax
  Profit Mergin % = DIVIDE('Order Details'[Profit],'Order Details'[Amount])
  ```
  ```dax
  Profit Status = IF('Order Details'[Profit]>0,"Profit",IF('Order Details'[Profit]<0,"Loss","Break-Even"))
  ```
  ```dax
  Profit Mergin % = DIVIDE('Order Details'[Profit],'Order Details'[Amount])
  ```
  ```dax
  Location = 'List of Orders'[City]& " - "&'List of Orders'[State]
  ```
  ## 💡 Key Insights
  
* **Trend A:** First major business finding or behavior pattern identified.
* **Trend B:** Actionable performance anomaly noted in the data.
* **Recommendation:** Direct business action suggested based on the metrics.

  ## 🚀 How To Use
1. **Prerequisites:** Ensure you have the latest Power BI Desktop installed.
2. **File Formats:** Clone the repository to access the `.pbix` or `.pbit` file.
3. **Data Refresh:** Change the source path under **Data Source Settings** to point to your data files.

## Author

**Abirami Ganesan**


  

