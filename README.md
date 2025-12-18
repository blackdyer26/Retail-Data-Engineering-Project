# Retail Data Engineering Pipeline

[![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)
[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)](https://databricks.com/)
[![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)](https://spark.apache.org/)

## Project Overview

This project demonstrates an end-to-end enterprise-grade data engineering solution built on Microsoft Azure cloud platform. It implements a modern data lakehouse architecture using the **Medallion Architecture"" (Bronze-Silver-Gold layers) to process retail transaction data from multiple heterogeneous sources.

### Key Achievements

- ✅ Architected an end-to-end ETL solution using Azure Data Factory to ingest heterogeneous data from Azure SQL Database and REST APIs into ADLS Gen2 Storage.
- ✅ Implemented a robust Medallion Architecture (Bronze → Silver → Gold) for data quality and governance.
- ✅ Developed high-performance PySpark transformations in Azure Databricks to process and transform data across Delta Lake layers.
- ✅ Built interactive Power BI dashboards for real-time business intelligence and analytics.
- ✅ Ensured data quality, consistency, and reliability throughout the entire pipeline.

## 🏗️ Architecture Diagram

![Retail Data Pipeline Architecture](results/retail_data_pipeline-drawio.png)

### Architecture Components

The pipeline consists of the following key components:

1. **Data Sources (Left)**
   - **Azure SQL Database**: Three tables (Transaction, Product, Store)
   - **REST API**: Customer data in JSON format

2. **Ingestion Layer (Azure Data Factory)**
   - Orchestrates data movement from multiple sources
   - Handles incremental and full data loads
   - Implements error handling and retry logic

3. **Storage Layer (Azure Data Lake Storage Gen2)**
   - Centralized data lake for all raw and processed data
   - Hierarchical namespace for efficient data organization
   - Cost-effective storage with high throughput

4. **Processing Layer (Azure Databricks)**
   - Distributed PySpark processing engine
   - Implements business logic and transformations
   - Handles data quality checks and validations

5. **Data Lakehouse (Medallion Architecture)**
   - **Bronze Layer**: Raw data ingestion (as-is from source)
   - **Silver Layer**: Cleaned, validated, and deduplicated data
   - **Gold Layer**: Business-level aggregations and analytics-ready datasets

6. **Visualization Layer**
   - Interactive dashboards and reports
   - Real-time business metrics
   - Self-service analytics for stakeholders
