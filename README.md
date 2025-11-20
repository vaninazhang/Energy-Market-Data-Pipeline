# Energy Market Data Pipeline (Airflow + Azure + Python)

A production-style **data engineering pipeline** for ingesting, validating, transforming, and loading hourly **energy market pricing data** into a cloud analytics environment.  
This project reflects the types of pipelines used in **energy trading, finance, and market operations**, where reliable time-series data is critical.

---

## 📌 1. Overview

This repository demonstrates an end-to-end data engineering workflow:

- Automated pipeline orchestration with **Apache Airflow**
- Data ingestion from public **energy market APIs** or CSV
- Schema & quality validation using **Pandera**
- Time-series cleaning and transformation
- Raw → Clean → Curated cloud storage architecture in **Azure Data Lake**
- Analytics-ready dimensional model in **Azure SQL**
- Final visualization using **Power BI**

---

## 📌 2. Architecture Diagram

```mermaid
flowchart LR
    A[Market Data API / CSV Files] --> B[Airflow Scheduler]
    B --> C[Raw Zone - Azure Data Lake]
    C --> D[Python Validation & Cleaning]
    D --> E[Clean Zone - ADLS]
    E --> F[Azure SQL - Curated Tables]
    F --> G[Power BI Dashboard]

