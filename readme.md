# Real-Time MBTA Data Pipeline  
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

A real-time data engineering project that ingests **live MBTA vehicle data**, runs it through an **ETL pipeline in SSIS**, and loads it into **SQL Server** to power **near real-time dashboards in Power BI**.

---

## 📚 Table of Contents  
- [What is this?](#what-is-this)  
- [Getting Started](#getting-started)  
  - [Requirements](#requirements)  
  - [Installation](#installation)  
- [Usage](#usage)  

## 🚌 What is this?

This project demonstrates how to build a production-style pipeline for **streaming public transit data**:

- Continuously pulls live vehicle data from the **MBTA API**  
- Cleans, transforms, and loads data into **SQL Server** using **SSIS**  
- Structures data for **OLTP-style writes** while preserving **historical tracking** for analytics  
- Exposes the data for **Power BI dashboards** (for real-time and historical insights)

It showcases skills in **API integration, ETL design, SQL performance, and real-time analytics**.

---
## ⚙️ Getting Started  

### Requirements
- SQL Server 2019+  
- SSIS (SQL Server Integration Services)  
- Power BI Desktop  
- Python 3.8+ (optional, for API testing / exploration)  
- MBTA API Key (free from [MBTA Developers Portal](https://api-v3.mbta.com))

### Installation
1. Clone this repo:  
   ```bash
   git clone https://github.com/Athul0491/mbta-data-pipeline.git
   cd mbta-data-pipeline
2. Open the SSIS project in Visual Studio and deploy the ETL package.

3. Set up SQL Server tables using the provided schema under `sql/schema.sql`.

4. Run the scheduled package or trigger it manually to start data ingestion.

5. Open the Power BI report under `dashboards/` (coming soon) to visualize live MBTA data.

## 🧪 Usage  
Once deployed, the pipeline will continuously **ingest, transform, and load** live Boston-area transit data.

Example insights:
- Active vehicle positions and routes
- Route-level delays and performance trends
- Historical vehicle tracks over time

You can adapt this pattern to other transit APIs or domains to practice **real-time analytics and data engineering**.

