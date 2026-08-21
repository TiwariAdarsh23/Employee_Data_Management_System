# Employee Data Management System

This repository contains the architecture and codebase for a scalable employee data management system. It utilizes AWS, PySpark, Kafka, PostgreSQL, and Apache Airflow to handle both daily batch data processing and real-time communication monitoring.

## Features

* **Data Ingestion & Storage:** Batch ingestion of employee records with reliable storage in AWS S3.
* **ETL Pipelines:** Data extraction, transformation, and loading handled by PySpark and AWS Glue.
* **Real-Time Monitoring:** Apache Kafka integration to process employee communications as they occur.
* **Content Moderation:** Automated detection and flagging of toxic or inappropriate messages.
* **Policy Enforcement:** Tracking of employee strikes and automated salary deduction processing based on communication violations.
* **Orchestration:** Scheduled and automated pipeline execution managed by Apache Airflow.
* **Querying & Database:** PostgreSQL for structured data storage and AWS Athena for serverless analytics on the data lake.

## Architecture

### Batch Pipeline (Data Processing)
```text
Employee Data
      │
      ▼
   AWS S3
      │
      ▼
AWS Glue + PySpark
      │
      ▼
 PostgreSQL
      │
      ▼
AWS Athena

```
### Real-Time Pipeline
```text
Employee Messages
        │
        ▼
      Kafka
        │
        ▼
PySpark Streaming
        │
        ▼
Toxic Message Detection
        │
        ▼
Strike & Salary Processing
```
## Tech Stack

| Category | Technology |
|---|---|
| Cloud | AWS |
| Storage | Amazon S3 |
| ETL | AWS Glue |
| Processing | PySpark |
| Streaming | Apache Kafka |
| Orchestration | Apache Airflow |
| Database | PostgreSQL |
| Query Engine | Amazon Athena |
| Language | Python |
| Compute | AWS EC2 |

## Core Modules

### Employee Data Pipeline
Processes employee data using AWS S3, AWS Glue, and PySpark.

**Capabilities:**
* Data ingestion
* Data transformation
* Employee data processing
* PostgreSQL integration
* Athena-based querying

### Real-Time Communication Monitoring
Uses Kafka and PySpark to process employee communication data in real time.

**Capabilities:**
* Real-time message processing
* Toxic message detection
* Strike history management
* Salary deduction processing

## Project Structure

```text
Employee-Data-Management-System/
│
├── 7UTC.py
├── yearly.py
│
├── GlueJob.ipynb
├── kafka-ec2(4).ipynb
│
├── kafka_dag_daily.py
├── kafka_dag_morning.py
│
├── daily_employee_glue_jobs_grouped1
│
└── README.md
```
## AWS Services

* **Amazon S3** — Data storage
* **AWS Glue** — ETL processing
* **Amazon Athena** — Data querying
* **Amazon EC2** — Infrastructure for project components
