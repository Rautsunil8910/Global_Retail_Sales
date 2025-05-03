# 🛠️ Medallion Architecture Data Pipeline with Azure Databricks and Power BI

## 📌 Project Overview

This project demonstrates a complete end-to-end data pipeline using the **Medallion Architecture** (Bronze, Silver, Gold) implemented in **Azure Databricks**. The pipeline ingests raw data in multiple file formats, transforms and refines the data, and finally aggregates it for analytics and visualization using **Power BI**.

---

## 🗂️ Data Sources

Three different raw data files were used and ingested into the **Bronze Layer**:

- `transactions.parquet` — Transaction-level sales data  
- `products.json` — Product catalog information  
- `customers.csv` — Customer demographic and identity data  

---

## 🏗️ Architecture Layers

### 🥉 Bronze Layer: Raw Ingestion

- Loaded raw data into Delta Lake format using Databricks.
- Applied minimal transformations (schema enforcement, metadata tracking).
- File formats:
  - Parquet for transaction data
  - JSON for product data
  - CSV for customer data

### 🥈 Silver Layer: Data Refinement

- Cleaned and transformed raw data:
  - Type conversions
  - Handling nulls and duplicates
  - Filtering invalid or corrupt records
  - Joining datasets (e.g., customers with transactions)
- Stored as Delta Tables for efficient querying and version control.

### 🥇 Gold Layer: Aggregated Business Data

- Performed business-level aggregations:
  - Total revenue per product/category
  - Top customers by spending
  - Monthly transaction volume
- Optimized tables for BI reporting (e.g., denormalization).
- Stored curated and aggregated results in Delta format.

---

## 🔗 Tools and Technologies

| Tool/Service        | Purpose                                |
|---------------------|----------------------------------------|
| Azure Databricks    | Data engineering and Delta Lake ETL    |
| Delta Lake          | Reliable storage and versioning        |
| Apache Spark (PySpark) | Data processing and transformation |
| Power BI Desktop    | Business Intelligence and Visualization|
| Azure Blob/ADLS     | Storage for source files (optional)    |

---

## 📊 Visualizations in Power BI

After the Gold layer was created:

- **Connected Power BI Desktop to Azure Databricks cluster**
- Imported aggregated Delta tables using the built-in connector
- Built dashboards and reports, including:
  - Sales trends over time
  - Daily Sales

---

## ✅ Outcomes

- Demonstrated scalable data lakehouse architecture using Medallion pattern
- Enabled real-time or batch processing with Delta Lake
- Built business-ready dashboards with direct connectivity to Databricks
- Ensured data quality, lineage, and performance across all pipeline stages

---

## 📌 Future Improvements

- Integrate with Azure Data Factory for orchestration  
- Implement CI/CD with Databricks Repos  
- Add unit tests and data quality validation layers (e.g., with Great Expectations)

---

## 👨‍💻 Author

**Sunil Raut**  
Data Engineer | Big Data & AI Enthusiast  


---

