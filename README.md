# Data Warehouse & Business Intelligence Dashboard

## Project Overview

This project focuses on building an end-to-end data warehouse using Microsoft SQL Server and the Medallion Architecture. It transforms raw CRM and ERP source data into structured, business-ready analytical datasets and presents insights through an interactive Power BI dashboard.

The project was developed as part of the Business Intelligence and Data Analytics course at the German International University.

## Project Objectives

- Build a structured data warehouse following Bronze, Silver, and Gold layers.
- Clean, standardize, and enrich raw source data using SQL.
- Design dimensional data models based on Kimball's star schema principles.
- Integrate multiple analytical schemas using shared dimensions.
- Develop a Power BI dashboard to answer business questions and support data-driven decision-making.

## Architecture

The data pipeline follows the Medallion Architecture:

```text
CRM / ERP CSV Files
        |
        v
Bronze Layer
Raw data ingestion
        |
        v
Silver Layer
Data cleaning and transformation
        |
        v
Gold Layer
Star schemas and business logic
        |
        v
Power BI Dashboard
KPIs, analytics and business insights
```

### Bronze Layer

- Loaded source CSV files into SQL Server tables.
- Preserved the original source structure.
- Used stored procedures for repeatable data loading.
- Implemented logging and row-count validation.

### Silver Layer

- Cleaned and standardized source data.
- Handled missing values, duplicates, whitespace, and inconsistent entries.
- Applied data type conversions and derived business attributes.
- Implemented stored procedures and data-quality validation.

### Gold Layer

- Designed dimensional models around business processes.
- Implemented fact and dimension tables.
- Used surrogate keys to establish relationships between facts and dimensions.
- Integrated at least two star schemas using a fact constellation (Galaxy schema) design.

### Power BI Dashboard

- Defined dashboard user personas and business questions.
- Developed KPIs, DAX measures, filters, and interactive visualizations.
- Used cross-schema analysis to connect insights across business processes.
- Designed dashboard pages to support business monitoring and decision-making.

## Technologies Used

- **Database:** Microsoft SQL Server
- **Query Language:** SQL / T-SQL
- **Data Engineering:** Stored Procedures, ETL, Data Quality Checks
- **Data Modeling:** Medallion Architecture, Star Schema, Fact Constellation
- **Business Intelligence:** Microsoft Power BI, DAX
- **Data Visualization:** Interactive dashboards, KPIs, filters, and slicers

## Repository Structure

```text
data-warehouse-business-intelligence/
├── README.md
├── sql/
│   ├── bronze/
│   ├── silver/
│   └── gold/
├── dashboard/
│   ├── dashboard_screenshots/
│   └── dashboard.pbix
└── docs/
    ├── report.pdf
    └── data_model.png
```

The structure above is a suggested organization. Include only folders and files that are actually available and approved for publication.

## Key Learning Outcomes

- Implementing a layered data warehouse architecture.
- Building repeatable SQL-based data ingestion and transformation processes.
- Applying dimensional modeling and integrating analytical schemas.
- Validating data quality and maintaining reliable data pipelines.
- Translating business requirements into Power BI dashboards and actionable insights.

## Academic Project

Developed as part of the Business Intelligence and Data Analytics course at the German International University.
