# 🌐 End-to-End Data Engineering Project on Azure

AdventureWorks Data Pipeline - Complete Project
# Project Overview

This project implements a complete end-to-end data pipeline for AdventureWorks data using Azure cloud services. The pipeline follows a medallion architecture (Bronze → Silver → Gold) with automated data ingestion, transformation, and reporting capabilities.

# Architecture Overview

GitHub Repository → ADF Dynamic Pipeline → Bronze Layer → Databricks Silver Layer → Synapse Analytics (Gold Layer) → Reporting(Power BI)

Azure Data Factory (ADF): Data ingestion and orchestration
Azure Data Lake Storage Gen2: Data storage (Bronze, Silver, Gold layers)
Azure Databricks: Data transformation and processing
Azure Synapse Analytics: Data warehousing and analytics
Power BI/SQL: Reporting and visualization
JSON Configuration: Dynamic pipeline parameters


# Phase 1: Dynamic Data Ingestion (ADF)
Overview
Azure Data Factory dynamically ingests data from GitHub repositories using JSON configuration files to define source parameters.
Key Components
1. JSON Configuration File (added in Data folder)

2. Dynamic Pipeline Activities

Lookup Activity: Reads JSON configuration file
ForEach Activity: Iterates through each data source
Copy Activity: Downloads data from GitHub and stores in Bronze layer

# Phase 2: Data Transformation (Databricks Silver Layer)
Overview
Databricks processes raw Bronze layer data, applying transformations, cleansing, and standardization to create the Silver layer.

# Phase 3: Data Warehousing (Synapse Analytics)
Overview
Synapse Analytics creates the Gold layer with optimized schemas, views, and stored procedures for analytical workloads.
