# NYC-TAXI-End-To-End-Azure-Data-Engineering-Project

# 🚖 Azure End-to-End Data Engineering Project

This project demonstrates an end-to-end data engineering pipeline using Azure Data Services and Databricks for **Data Ingestion**, **Transformation**, and **Serving**. It uses Azure Data Factory, Azure Data Lake Gen2, and Delta Lake to build a robust and scalable solution for processing data.

---

## 📊 **Project Overview**

The project involves ingesting **Taxi Trip** data via APIs into Azure Data Lake Gen2. Using **Databricks**, the raw data is transformed and optimized in multiple stages to enable analytics-ready data serving.

---

## ⚙️ **Architecture**

### Key Components:

1. **Ingestion**:
   - Source: Taxi Trip Data (via API).
   - Tool: Azure Data Factory.
   - Destination: **Raw Data Store** in Azure Data Lake Gen2 (stored as Parquet).

2. **Transformation**:
   - Tool: Azure Databricks.
   - Stages:
     - Raw data → Transformed data (Parquet format).
     - Optimized for analytics.

3. **Serving**:
   - Optimized data stored in **Delta Lake** for query serving.
   - Tool: Azure Data Lake Gen2.

4. **Security**:
   - Azure Active Directory for authentication.
   - Managed access keys for securing resources.

---

## 🚀 **Technologies Used**

- **Azure Data Factory**: Orchestrates data ingestion workflows.
- **Azure Data Lake Storage Gen2**: Cloud storage for raw and processed data.
- **Azure Databricks**: Data transformation, ETL, and Delta Lake implementation.
- **Delta Lake**: Ensures ACID transactions, data reliability, and time travel.
- **Parquet**: Storage format for raw and transformed data.
- **Azure Active Directory**: Secures the pipeline.

---

## 🔧 **Steps to Run the Project**

### Prerequisites:
1. Azure subscription with access to:
   - Azure Data Factory
   - Azure Data Lake Gen2
   - Azure Databricks
2. Python and Spark skills.
3. Access to the Taxi Trip Data API.

---

### Step-by-Step Process:

1. **Data Ingestion**:
   - Use Azure Data Factory to connect to the API.
   - Load raw data into Azure Data Lake Gen2.

2. **Data Transformation**:
   - Set up a Databricks notebook.
   - Load raw Parquet data.
   - Transform the data using Spark (PySpark).
   - Save intermediate transformed data as Parquet.

3. **Serving Layer**:
   - Convert transformed data into a Delta table.
   - Save it in Azure Data Lake Gen2.

4. **Security**:
   - Integrate Azure Active Directory for resource protection.

---

## 📂 **Directory Structure**

```plaintext
.
├── notebooks/            # Databricks Notebooks
│   ├── 01_data_ingestion.ipynb
│   ├── 02_data_transformation.ipynb
│   └── 03_delta_serving.ipynb
├── data/                 # Sample Raw Data (if any)
├── pipeline/             # Data Factory pipeline JSON exports
├── images/               # Architecture diagrams or screenshots
├── README.md             # Project documentation
└── LICENSE               # License information

