# Crypto Market Data Pipeline

## Overview
This project is an end-to-end crypto market data pipeline built with Python, PostgreSQL, SQL, and Power BI. It is designed to demonstrate how data from multiple public cryptocurrency sources can be ingested, structured, transformed, analyzed, and presented in a business-friendly dashboard format.

Python is used for data extraction and loading, PostgreSQL is used to store and combine datasets, SQL is used for transformation and analytical querying, and Power BI is used for dashboard reporting and visual storytelling.

## Project Goal
The goal of this project is to build a structured analytics workflow for cryptocurrency market monitoring by combining data engineering, SQL analysis, and business intelligence.

This project is intended to show:
- data ingestion from public sources
- database design and loading in PostgreSQL
- SQL-based transformation and analysis
- dashboard development in Power BI
- end-to-end pipeline thinking for analytics and data roles

## Business Problem
Cryptocurrency data changes rapidly and comes from multiple public sources. Analysts and decision-makers need a structured pipeline that can collect this data, store it reliably, combine it across sources, and generate useful insights for monitoring market movement, asset performance, and trading activity.

Without a proper pipeline, analysis becomes inconsistent, repetitive, and difficult to scale.

## Solution
This project builds a multi-stage pipeline:

1. Python extracts cryptocurrency data from public APIs or datasets  
2. Raw data is loaded into PostgreSQL staging tables  
3. SQL is used to combine, clean, and transform the data into analysis-ready tables  
4. Analytical SQL queries generate KPIs and insights  
5. Power BI is used to present interactive dashboards and visual summaries  

## Tech Stack
- **Python**: data extraction and database loading
- **PostgreSQL**: data storage and table modeling
- **SQL**: transformations, joins, aggregations, and analysis
- **Power BI**: dashboarding and reporting
- **Pandas / Requests / SQLAlchemy / Psycopg2**: pipeline support libraries

## Proposed Architecture
```text
Public Data Sources
        ↓
      Python
(extract + prepare + load)
        ↓
   PostgreSQL
(staging + integrated tables)
        ↓
       SQL
(transform + analyze + aggregate)
        ↓
    Power BI
(dashboards + reporting)

crypto-market-data-pipeline/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   ├── raw/
│   └── processed/
├── sql/
│   ├── schema.sql
│   ├── staging_queries.sql
│   └── analysis_queries.sql
├── src/
│   ├── extract.py
│   ├── load_to_postgres.py
│   ├── analyze.py
│   └── config.py
├── notebooks/
│   └── crypto_analysis.ipynb
├── dashboard/
│   └── powerbi_screenshots/
└── outputs/
    └── reports/
