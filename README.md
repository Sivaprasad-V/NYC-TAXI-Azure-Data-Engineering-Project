# 🚖 Azure End-to-End Data Engineering Project

# Azure End-to-End Data Engineering Project

This README provides a detailed explanation of my Azure-based end-to-end data engineering project. The project demonstrates the ingestion, transformation, and serving of data using Azure services, including Data Factory, Databricks, and Data Lake.

---
## **1. Project Overview**
The project processes taxi trip data and implements the following stages:

1. **Ingestion** - Raw data is ingested from the source using Azure Data Factory.
2. **Transformation** - Data is transformed and stored in Parquet format using Databricks.
3. **Serving** - Final data is stored in Delta Lake format with advanced features like *Versioning* and *Time Travel*.
4. **Security** - Data is secured with Azure Active Directory and Key Vault.

---
## **2. Data Flow Architecture**
Here is the step-by-step data flow:

### **Step 1: Ingestion**
- **Tool**: Azure Data Factory
- **Process**:
   - The raw data is fetched from a REST API (Taxi trip data).
   - Data is stored in the **Raw Data Store** within **Azure Data Lake Gen2**.

### **Step 2: Transformation**
- **Tool**: Azure Databricks
- **Process**:
   - The raw data is loaded into Databricks.
   - Data cleaning and transformation are performed using PySpark.
   - Transformed data is stored back in **Azure Data Lake Gen2** in **Parquet format**.

### **Step 3: Serving Data with Delta Lake**
- **Tool**: Azure Databricks
- **Process**:
   - Final data is stored in **Delta Lake**.
   - Implemented **Versioning** and **Time Travel** for advanced data management.
     - *Versioning*: Tracks changes made to the data.
     - *Time Travel*: Allows querying previous versions of the data.

   - This ensures data reliability, consistency, and flexibility for analytical workloads.

---
## **3. Security**
To ensure the project is secure:
- **Azure Active Directory (AAD)** is used for authentication.
- **Azure Key Vault** is used to securely store secrets and keys.

---
## **4. Tools & Technologies Used**
- **Azure Data Factory**: For data ingestion.
- **Azure Databricks**: For data transformation and serving.
- **Azure Data Lake Gen2**: Data storage at every stage.
- **Delta Lake**: For serving data with versioning and time travel.
- **Azure Active Directory**: For authentication and security.
- **Azure Key Vault**: For secrets management.

---
## **5. Pipeline Explanation**

### Dynamic Pipeline in Azure Data Factory
- I have created a **DynamicPipeline** in Azure Data Factory.
- The pipeline includes a **ForEach** activity and an **If Condition**.
   - The condition checks: `@greater(item(), 9)`.
   - **True Case**: Runs *Copy data2* activity.
   - **False Case**: Runs *Copy data1* activity.

---
## **6. Project Diagram**
Below is a high-level diagram of the project:

![Project Diagram](image.png)

---
## **7. How to Run the Project**
1. **Set up Azure Resources**:
   - Azure Data Factory
   - Azure Databricks
   - Azure Data Lake Gen2
2. **Load Data**:
   - Configure the REST API source for taxi trip data.
3. **Execute the Pipeline**:
   - Run the Azure Data Factory pipeline for ingestion.
   - Use Databricks for transformation and serving the data.
4. **Verify Data**:
   - Check the raw, transformed, and served data in Azure Data Lake Gen2.
   - Use Delta Lake's versioning and time travel to query historical data.

---
## **8. Conclusion**
This project demonstrates a robust data pipeline using Azure services to ingest, transform, and serve data. The use of Delta Lake ensures advanced features like versioning and time travel, making the solution reliable and future-proof.

Thank you for checking out this project! 🚀

---
## **9. Contact Information**
Feel free to reach out to me for any queries or collaboration opportunities!

**Name**: [Your Name]  
**Email**: [Your Email]  
**GitHub**: [Your GitHub Profile Link]



