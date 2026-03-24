# 🏥 Healthcare Claims Analytics Pipeline (Snowflake)

## 📌 Overview

This project implements an end-to-end **data pipeline in Snowflake** to process and analyze healthcare claims data. It transforms raw claim records into validated, analytics-ready datasets with support for **incremental data processing**.

---

## 🏗️ Architecture

The pipeline follows a layered architecture:

* **RAW Layer** → Ingests data directly from source files
* **CURATED Layer** → Cleans, standardizes, and enriches data
* **ANALYTICS Layer** → Generates business insights
* **STREAMS** → Tracks incremental changes
* **VALIDATION & TESTING** → Ensures data quality and correctness

---

## ⚙️ Tech Stack

* Snowflake (Cloud Data Warehouse)
* SQL
* Snowflake Streams (CDC)
* Internal Stages (Data Ingestion)

---

## 📂 Project Structure

```bash
healthcare-claims-analytics/
│
├── sql/
│   ├── raw.sql
│   ├── curated.sql
│   ├── streams.sql
│   ├── analytics.sql
│   ├── validation.sql
│   └── testing.sql
│
└── README.md
```

---

## 🚀 Execution Steps

### 1️⃣ Setup Database & Schemas

Run:

* `RAW.sql`

### 2️⃣ Load Data into Stage

Upload CSV files into Snowflake:

```sql
PUT file://<your_file>.csv @healthcare_stage;
```

### 3️⃣ Transform Data

Execute in order:

1. `CURATED.sql`
2. `STREAMS.sql`
3. `ANALYTICS.sql`

### 4️⃣ Validate & Test

Run:

* `VALIDATION.sql`
* `TESTING.sql`

---

## 🔄 Incremental Processing

* Implemented using **Snowflake Streams**
* Captures **new and updated records only**
* Enables efficient and scalable data pipelines

---

## 📊 Key Highlights

* End-to-end ETL pipeline in Snowflake
* Modular SQL-based architecture
* Incremental data loading (CDC)
* Built-in data validation framework

---

## 💡 Business Use Cases

* Fraud detection in claims
* Cost and utilization analysis
* Provider performance evaluation

---

## 🚀 Future Enhancements

* Automate pipeline using Snowflake Tasks
* Add dashboard layer (Power BI / Tableau)
* Implement alerting for data anomalies
