# Crypto Market ETL & Analytics Pipeline

## Overview
This project is an end-to-end data pipeline for cryptocurrency market analysis. It extracts crypto price and market data from public APIs, transforms and cleans the data, loads it into PostgreSQL, and supports downstream analysis through SQL queries and Power BI dashboards.

The goal is to demonstrate production-style data thinking across ingestion, storage, transformation, analysis, and business-facing reporting.

## Business Problem
Crypto markets generate high-volume, fast-changing data that can be difficult to track consistently across assets and time periods. Analysts, traders, and decision-makers need a structured workflow to collect reliable market data, clean it, store it in a queryable database, and generate insights for monitoring trends, volatility, and asset performance.

This project addresses that need by building a repeatable ETL pipeline and analytics layer for cryptocurrency market data.

## Project Objectives
- Extract cryptocurrency market data from a public source
- Clean and standardize the data for analysis
- Load structured data into PostgreSQL
- Write SQL queries for market insights and KPI reporting
- Build a Power BI dashboard for visual exploration
- Demonstrate an end-to-end analytics workflow suitable for data engineering and analytics roles

## Tech Stack
- **Python**: data extraction, transformation, automation
- **PostgreSQL**: structured storage and querying
- **SQL**: exploratory and reporting queries
- **Power BI**: dashboarding and business intelligence
- **Pandas / Requests / SQLAlchemy / Psycopg2**: ETL components

## Pipeline Architecture
1. **Extract**  
   Pull cryptocurrency market data from a public API

2. **Transform**  
   Clean missing values, standardize columns, parse timestamps, and prepare structured tables

3. **Load**  
   Insert processed data into PostgreSQL tables

4. **Analyze**  
   Use SQL queries to generate insights such as top-performing assets, price volatility, and market cap trends

5. **Visualize**  
   Connect Power BI to PostgreSQL or exported query outputs to build dashboards

## Dataset / Data Source
This project uses publicly available cryptocurrency market data from an external API source.

Typical fields may include:
- coin name
- symbol
- current price
- market capitalization
- trading volume
- price change percentage
- timestamp / refresh time

## Repository Structure
```text
crypto-market-etl-analytics/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   ├── raw/
│   └── processed/
├── sql/
│   ├── schema.sql
│   ├── load_queries.sql
│   └── analysis_queries.sql
├── src/
│   ├── extract.py
│   ├── transform.py
│   ├── load.py
│   ├── pipeline.py
│   └── config.py
├── notebooks/
│   └── crypto_analysis.ipynb
├── dashboard/
│   └── powerbi_screenshots/
└── outputs/
    └── reports/
