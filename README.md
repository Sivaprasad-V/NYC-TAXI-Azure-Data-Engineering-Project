# NYC TAXI🚖Azure End-to-End Data Engineering Project🚀

Welcome to my **Azure End-to-End Data Engineering Project**! In this project, I used various Azure tools and technologies to **ingest, transform, and serve data** efficiently. Let’s dive into what I’ve built step by step. 🛠️

---

## 📋 **Project Overview**

This project handles data in three major steps:

1. **Ingestion**: Collect raw data and store it.
2. **Transformation**: Clean, process, and transform the data.
3. **Serving**: Save the transformed data in a serving layer for further analysis.

I used **Azure Data Factory**, **Azure Data Lake Storage (Gen2)**, **Databricks**, and **Delta Lake** for this project.

---

## 📊 **Architecture**

Here’s the overall architecture of the project:

1. **Source Data** 🚵

   - I collected data (in this case, Taxi data) from an **API**.
   - **API LINK** https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
   - **File Link** https://d37ci6vzurychx.cloudfront.net/trip-data/green_tripdata_2023-01.parquet
     
2. **Ingestion Layer** 🌐

   - I ingested the raw data into **Azure Data Lake Gen2**.
   - I stored the data in **Parquet format** for efficient storage and processing.

3. **Transformation Layer** 🧹

   - I used **Azure Databricks** to clean and transform the data.
   - I converted the raw data into a meaningful format using Spark and saved it back to **Azure Data Lake Gen2**.

4. **Serving Layer** 🎯

   - The cleaned, transformed data was saved as a **Delta Table** in the serving layer for analytics and reporting.

5. **Security** 🔒

   - I ensured secure access to all Azure services using **Azure Active Directory** and role-based access control (RBAC).

---

## 🛠️ **Steps of the Project**

### 1. **Data Ingestion**

- I used **Azure Data Factory** to extract data from an external API.
- The data was stored as raw **Parquet files** in the **Raw Data Store** folder of **Data Lake Gen2**.

### 2. **Data Transformation**

- I used **Databricks** for data processing and transformation.
- The tasks included:
  - Reading the raw data.
  - Performing **cleaning** and **transformation**.
  - Writing the transformed data back to **Data Lake Gen2** in Parquet format.

### 3. **Serving Data with Delta Lake**

- I converted the transformed data into **Delta Tables** for optimized storage and performance.
- The data was stored in the **Serving folder** of **Data Lake Gen2**.
- Delta Tables make it easy to query and perform analytics on the data.

### 4. **Security**

- I applied **Azure Security** features to protect the data.
- Tools used:
  - **Azure Active Directory** for authentication.
  - **Role-Based Access Control (RBAC)** for authorization.

---

## 📂 **Technologies Used**

| **Tool/Service**           | **Purpose**                                       |
| -------------------------- | ------------------------------------------------- |
| **Azure Data Factory**     | Ingesting data from APIs.                         |
| **Azure Data Lake Gen2**   | Storage for raw, transformed, and served data.    |
| **Databricks**             | Processing and transforming the data using Spark. |
| **Parquet**                | Storage format for raw and transformed data.      |
| **Delta Lake**             | Optimized format for serving clean data.          |
| **Azure Active Directory** | Security and access management.                   |

---

## 📂 **Folder Structure**

Here’s how I organized my data in **Azure Data Lake Gen2**:

```
DataLakeGen2/
│
├── bronze/          <- Raw data in Parquet format
│
├── silver/          <- Cleaned and transformed data
│
└── gold/            <- Final Delta Tables for analytics
```

---

## 🎉 **Key Highlights**

1. **Dynamic Pipeline in Data Factory**\
   I created a dynamic pipeline to handle data ingestion dynamically, based on certain conditions. For example:

   - **Copy Data 1** for small numbers.
   - **Copy Data 2** for large numbers.

2. **Efficient Transformation**\
   Using **Databricks**, I transformed raw data into meaningful, clean data quickly and efficiently.

3. **Serving Layer with Delta Tables**\
   The final output is stored as **Delta Tables**, which provide fast query performance and are perfect for analytics.

4. **Security First**\
   All data movement and storage are secured using Azure’s built-in security features.

---

## 📊 **How to Run the Project**

Follow these steps to run the project:

1. **Set up Azure Resources**:

   - Create Azure Data Lake Gen2, Azure Databricks, and Azure Data Factory.

2. **Ingest Data**:

   - Use **Azure Data Factory** to collect data and store it in **Data Lake Gen2**.

3. **Transform Data**:

   - Use Databricks to clean and transform the data.

4. **Store Data**:

   - Write the transformed data as Delta Tables to the serving layer.

5. **Analyze the Data**:

   - Query the Delta Tables for reporting and insights.

---

## 📈 **Conclusion**

This project shows how you can build an end-to-end data engineering solution using **Azure tools**. It covers everything from **ingesting data** to **transforming** it and saving it securely for analysis.

Feel free to clone this project and try it on your own. Let me know if you have any questions or suggestions! 😃

---

## 🧺 **Next Steps**

- Add more transformations in Databricks.
- Use **Power BI** or **Synapse Analytics** to visualize the data.
- Automate pipelines further using triggers.

---

I hope this makes it crystal clear! Let me know if you want any changes or additions. 😊






