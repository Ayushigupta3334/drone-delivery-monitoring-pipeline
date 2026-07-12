# Drone Delivery Monitoring & Failure Analytics Pipeline

## Project Overview

This project implements an end-to-end data engineering pipeline using Databricks, PySpark, Delta Lake, and SQL to monitor drone deliveries and analyze operational failures.

The solution follows the Medallion Architecture (Bronze, Silver, Gold) and generates business insights such as delivery success rates, failure causes, average delivery time, and high-risk delivery zones.

---

# Project Structure

```text
drone-delivery-monitoring-pipeline/

│
├── README.md
├── architecture.png
├── requirements.txt
│
├── notebooks/
│   ├── 01_generate_data.ipynb
│   ├── 02_bronze_layer.ipynb
│   ├── 03_silver_layer.ipynb
│   └── 04_gold_layer.ipynb
|
│├── dashboard/
│   ├── drone performance.png
│   ├── success_rate.png
│   ├── high_risk failure.png
│   ├── Average delivery time.png
│  
├── screenshots/
│   ├── bronze_layer.png
│   ├── silver_layer.png
│   ├── gold_layer.png
│   ├── data generation.png
│   └── gold_kpis.png
│
├── Drone_Delivery_Monitoring_Report.pdf
│
└── data_sample/
    ├── drones_sample.csv
    ├── deliveries_sample.csv
    └── flight_logs_sample.csv
```

---

# Problem Statement

Drone delivery systems face challenges such as:

- Battery limitations
- Weather disruptions
- GPS signal instability
- Delivery failures
- Lack of centralized monitoring

This project builds a scalable data pipeline to monitor and optimize drone operations.

---

# Architecture

```text
Raw CSV Files
       ↓
Bronze Layer
       ↓
Silver Layer
       ↓
Gold Layer
       ↓
SQL Dashboard
```

---

# Technologies Used

- Databricks
- PySpark
- Delta Lake
- SQL
- Pandas
- GitHub

---

# Medallion Architecture

## Bronze Layer

Stores raw datasets and ingestion metadata.

Tables:

- bronze_drones
- bronze_deliveries
- bronze_logs

---

## Silver Layer

Performs cleaning and transformation.

Derived columns:

- delivery_duration
- failure_flag
- processed_time

Tables:

- silver_deliveries
- silver_logs

---

## Gold Layer

Generates business KPIs.

Tables:

- gold_kpis
- gold_high_risk_zones
- gold_drone_performance

---

# KPIs Generated

- Delivery Success Rate
- Failure Rate
- Average Delivery Time
- High-Risk Zones
- Drone Performance

---

# SQL Analytics

The project includes SQL queries and dashboard visualizations for:

- Delivery analysis
- Failure analysis
- Zone analysis
- Drone performance analysis

---

# Future Enhancements

- Apache Kafka integration
- Apache Airflow scheduling
- Machine learning models
- Real-time dashboards

---

# Author

Ayushi Gupta
