# Azure Lakehouse Data Engineering Project

### AdventureWorks Pipeline

---

## 🚀 Why This Project?

Modern analytics platforms must be **scalable, secure, and cost-efficient**.
This project simulates a **real-world enterprise data platform** built on Microsoft Azure, transforming raw operational data into **business-ready analytics** using a **Lakehouse approach**.

The solution follows **Medallion Architecture** to ensure clean separation between raw, refined, and curated data layers.

---

## 🧩 Business Use Case

AdventureWorks data from multiple domains is published as CSV files on GitHub.
The goal is to:

- Ingest this data automatically
- Standardize and optimize it for analytics
- Serve trusted datasets for reporting without exposing raw storage

---

## 🏗️ Solution Overview

The platform is built using **Azure-native services only**, avoiding secrets and long-running compute.

**Core idea:**

> _Ingest once → Transform logically → Serve securely_

---

## 🔁 End-to-End Flow

1. **Source**

   - CSV files hosted on GitHub

2. **Ingestion**

   - Azure Data Factory performs metadata-driven ingestion
   - Pipelines dynamically ingest multiple domains

3. **Storage**

   - Azure Data Lake Storage Gen2
   - Organized into Bronze, Silver, and Gold containers

4. **Analytics Layer**

   - Azure Synapse Analytics (Serverless SQL)
   - SQL-based querying directly on data lake files

5. **Visualization**

   - Power BI connects only to curated Gold datasets

---

## 🥉🥈🥇 Data Layer Strategy

### Bronze Layer

- Raw CSV files
- No transformations
- Full data traceability

### Silver Layer

- Cleaned and standardized datasets
- Converted to Parquet
- Optimized for performance

### Gold Layer

- Business-ready datasets
- External tables created using CETAS
- Used directly by Power BI

---

## 🏠 Lakehouse Design Principles

- Single source of truth (ADLS)
- SQL-first analytics
- No data duplication
- Storage and compute fully decoupled
- Serverless and pay-as-you-go

---

## 🛠️ Technology Stack

- **Azure Data Factory** – Orchestration and ingestion
- **Azure Data Lake Storage Gen2** – Central data storage
- **Azure Synapse Serverless SQL** – Analytics engine
- **Microsoft Entra ID** – Authentication and access control
- **Power BI** – Reporting and dashboards
- **GitHub** – Source control

---

## 🔐 Security Model

- System-assigned Managed Identity
- Entra ID authentication only
- RBAC-based access to storage
- No credentials stored in pipelines or code
- Power BI isolated from raw storage

<!-- Thanks for visiting
LALIT SINGH -->
