# Energy Market Data Pipeline (Airflow + Python + Azure)

A production-style data engineering project for ingesting, validating, transforming and storing hourly energy market pricing data.

1. Overview

This project demonstrates a full end-to-end data engineering pipeline designed for real-world energy & financial analytics use cases.

The pipeline ingests hourly energy market pricing data from a public API (or CSV datasets), stores the raw data in Azure Data Lake, performs validation & cleaning with Python, transforms the data into analytics-ready tables, and loads them into Azure SQL for BI reporting.

This architecture is similar to pipelines used in energy trading, finance, and market operations, where high-quality time-series data is mission-critical.

2. Architecture
flowchart LR
    A[Public Market Data API / CSV] --> B[Airflow Scheduler]
    B --> C[Raw Zone - Azure Data Lake]
    C --> D[Python Validation & Cleaning]
    D --> E[Clean Zone - ADLS]
    E --> F[Azure SQL - Curated Tables]
    F --> G[Power BI Dashboard]
