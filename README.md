# Data Warehouse and Analytics Project 

Welcome to the **Data Warehouse and Analytics Project** repository! 
This project demonstrates a comprehensive data warehousing and analytics solution, from building a data warehouse to generating actionable insights. Designed as a portfolio project highlights industry best practices in data engineering and analytics. 

----

## Data Architecture

The data architecture for this project follows the **Medallion Architecture**, consisting of **Bronze**, **Silver**, and **Gold** layers:

<img width="1544" height="912" alt="image" src="https://github.com/user-attachments/assets/73d3d1bb-f5d4-4143-9346-3bac44a6168b" />

1. **Bronze Layer**: Stores raw data as-is from source systems. Data is ingested from CSV files into a SQL Server database.
2. **Silver Layer**: Performs data cleansing, standardization, and normalization to prepare the data for analysis.
3. **Gold Layer**: Contains business-ready data modeled using a **Star Schema** for reporting and analytics.

----

## 📌 Project Overview

This project focuses on designing and implementing a **Modern Data Warehouse** using the **Medallion Architecture**, along with developing ETL pipelines, analytical data models, and reporting solutions.

### 🔹 Project Components

#### 1. Data Architecture
Design and implement a modern data warehouse using the **Medallion Architecture**, consisting of three layers:

- **🥉 Bronze Layer** – Stores raw data extracted from source systems.
- **🥈 Silver Layer** – Contains cleaned, transformed, and standardized data.
- **🥇 Gold Layer** – Contains business-ready data optimized for analytics and reporting.

#### 2. ETL Pipelines
Develop **Extract, Transform, and Load (ETL)** pipelines to:

- Extract data from source systems.
- Clean and transform the data.
- Load processed data into the appropriate warehouse layers.

#### 3. Data Modeling
Develop analytical data models consisting of:

- **Fact Tables** – Store measurable business events and metrics.
- **Dimension Tables** – Store descriptive attributes used for analysis and filtering.
- Optimized relationships to support efficient analytical queries.

#### 4. Analytics & Reporting
Create **SQL-based analytical reports and dashboards** to:

- Analyze business performance.
- Identify trends and patterns.
- Generate actionable business insights.
- Support data-driven decision-making.

----

## Project Requirements 

## Building a Data Warehouse (Data Engineering)

### Objective 
Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

### Specifications 
- **Data Sources**: Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality**: Cleanse and resolve data quality issues prior to analysis.
- **Integration**: Combine both sources into single, user friendly data model designed for analytical queries.
- **Scope**: Focus on the latest dataset only; historization of dataset is not required.
- **Documentation**: Provided clear documentation of the data model to support both business stakeholders and analytical team.

  -----

  ### BI Analytics & Reporting (Data Analytics)

   ### Objective
  Develop SQL-based analytics to deliver detailed insights info:
  **Customer Behavior**
  **Product Performance**
  **Sales Trends**

  These insights empower stakeholders with key business metrics, enabling strategic decision-making.

  -----

 ## 📁 Project Structure
 
- **`datasets/`** – Raw ERP and CRM datasets.

- **`docs/`** – Project documentation and architecture.
  - **`etl.drawio`** – ETL techniques and methods.
  - **`data_architecture.drawio`** – Project architecture.
  - **`data_catalog.md`** – Dataset fields and metadata.
  - **`data_flow.drawio`** – Data flow diagram.
  - **`data_models.drawio`** – Data models and star schema.
  - **`naming-conventions.md`** – Naming guidelines.

- **`scripts/`** – SQL scripts for ETL and data transformations.
  - **`bronze/`** – Raw data extraction and loading.
  - **`silver/`** – Data cleaning and transformation.
  - **`gold/`** – Analytical data models.

- **`tests/`** – Data quality and testing scripts.

- **`README.md`** – Project overview and instructions.
