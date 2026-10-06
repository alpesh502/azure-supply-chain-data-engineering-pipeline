# End-to-End Supply Chain Data Pipeline

An end-to-end supply chain analytics project that turns raw transactional data into business-ready insights using the Medallion Architecture. The pipeline is organized into Bronze, Silver, and Gold layers to support reliable ingestion, clean transformation, data quality, and dashboard-ready aggregations.

## Project Overview

This project demonstrates how to build a scalable analytics workflow for supply chain data using Azure Databricks, PySpark, Spark SQL, Delta Lake, and Power BI. It takes raw source files, processes them through layered transformations, and delivers curated datasets for executive reporting and operational decision-making.

The project follows a structured data engineering approach where raw operational data is first ingested into the Bronze layer, then cleaned and transformed in the Silver layer, and finally aggregated into business-ready datasets in the Gold layer.

The repository includes three notebooks that map directly to the Medallion flow:

- `01_bronze_ingestion.ipynb` for raw data ingestion and landing.
- `02_silver_transformation.ipynb` for cleansing, validation, standardization, and enrichment.
- `03_gold_analytics.ipynb` for business-level aggregations and analytics.

The overall objective is to create a reliable and maintainable data pipeline that can transform raw supply chain information into meaningful insights for inventory management, sales analysis, product movement, supplier performance, and operational reporting.

## Business Problem

Supply chain organizations generate data from multiple operational areas such as inventory, products, suppliers, warehouses, shipments, and transactions. When this information is stored in separate raw files, it can be difficult to analyze consistently and efficiently.

Raw datasets may contain duplicate records, inconsistent values, missing information, different data formats, and operational-level details that are not directly suitable for business reporting.

This project addresses these challenges by creating a layered data processing pipeline.

The pipeline:

- Ingests raw supply chain data.
- Stores the original data in the Bronze layer.
- Cleans and validates the data in the Silver layer.
- Standardizes datasets for downstream analysis.
- Creates business-level datasets in the Gold layer.
- Provides curated outputs for Power BI reporting.
- Supports analysis of sales, inventory, products, suppliers, shipments, and warehouses.
- Provides a structured foundation for future analytics and data engineering enhancements.

## Project Objectives

The major objectives of this project are:

- Build an end-to-end supply chain data pipeline.
- Implement Medallion Architecture using Bronze, Silver, and Gold layers.
- Process raw CSV files using Azure Databricks and PySpark.
- Perform data cleaning and validation.
- Standardize datasets for analytical use.
- Transform operational data into business-ready datasets.
- Apply data modeling concepts such as Slowly Changing Dimension Type 2.
- Create analytical aggregations for reporting.
- Connect curated datasets with Power BI.
- Provide meaningful supply chain and inventory insights.
- Maintain a clear and organized data processing workflow.

## Architecture

The solution follows the Medallion design pattern:

- **Bronze Layer:** Stores raw, unprocessed data as the source of truth.
- **Silver Layer:** Applies cleaning, validation, standardization, and transformation for analysis.
- **Gold Layer:** Produces aggregated and business-ready tables optimized for reporting and dashboarding.

The high-level flow of the project is:

```text
Raw CSV Files
      |
      v
Bronze Layer
Raw / Unprocessed Data
      |
      v
Silver Layer
Cleaning + Validation + Standardization
      |
      v
Gold Layer
Business Aggregations + Analytics
      |
      v
Power BI
Dashboards + Business Insights
