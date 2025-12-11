# UrbanPulse: Real-Time Smart City Data Platform

## Project Overview

UrbanPulse is a full-fledged data engineering project simulating a **real-time smart city data platform**. It ingests, processes, stores, and visualizes data from various urban sources, including traffic sensors, energy meters, and IoT devices. This project demonstrates end-to-end **data engineering skills**: ETL pipelines, streaming data, orchestration, and dashboards.

## Objectives

* Build scalable **batch and streaming data pipelines** using Python, PostgreSQL, Kafka, and Airflow.
* Implement a **data lake** using MinIO for raw, processed, and curated datasets.
* Demonstrate **real-time data processing** with Kafka producers and consumers.
* Orchestrate pipelines with **Airflow DAGs**.
* Create **interactive dashboards** using Metabase or Streamlit.
* Provide a **polished portfolio-ready project** demonstrating real-world DE skills.

## Features

* Batch ETL pipelines: Extract, Transform, Load into PostgreSQL.
* Streaming pipeline: Kafka producer/consumer for real-time ingestion.
* Data lake layers: raw, processed, curated.
* Workflow orchestration via Airflow DAGs.
* Interactive dashboards for smart city metrics.

## Tech Stack

| Component        | Technology             | Purpose                       |
| ---------------- | ---------------------- | ----------------------------- |
| Programming      | Python 3.11+           | ETL & data pipeline logic     |
| Database         | PostgreSQL             | Data warehouse                |
| Object Storage   | MinIO                  | Data lake storage             |
| Streaming        | Kafka                  | Real-time data ingestion      |
| Orchestration    | Apache Airflow         | Schedule/manage pipelines     |
| Dashboard        | Metabase / Streamlit   | Visualization                 |
| Batch Processing | Pandas / PySpark       | Data transformations          |
| Containerization | Docker, Docker Compose | Local development environment |

## Project Structure

```
UrbanPulse/
├─ airflow/                # DAGs, plugins, configs
│  └─ dags/urbanpulse_etl.py
├─ kafka/
│  ├─ producer.py
│  └─ consumer.py
├─ etl/
│  ├─ api_ingest.py
│  ├─ transform.py
│  └─ load_postgresql.py
├─ datalake/
│  ├─ upload_raw.py
│  └─ curate_data.py
├─ warehouse/
│  └─ schema.sql
├─ dashboards/
│  └─ streamlit_app.py
├─ docker-compose.yml
├─ requirements.txt
└─ README.md
```

## Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/UrbanPulse.git
cd UrbanPulse
```

### 2. Python Environment

```bash
python -m venv venv
# Activate venv
# Windows: venv\Scripts\activate
# Mac/Linux: source venv/bin/activate
pip install -r requirements.txt
```

### 3. Docker Services

```bash
docker compose up -d
```

This starts PostgreSQL, MinIO, Kafka, Zookeeper, and Metabase.

### 4. Run ETL Pipelines

* Batch ETL: `python etl/api_ingest.py`
* Streaming: `python kafka/producer.py` & `python kafka/consumer.py`
* Airflow DAGs: Access at `http://localhost:8080`

### 5. Dashboard

* Metabase: `http://localhost:3000`
* Streamlit: `streamlit run dashboards/streamlit_app.py`

## Learning Outcomes

* Hands-on experience with **batch & streaming pipelines**.
* Practical knowledge of **workflow orchestration** with Airflow.
* Building a **data lake architecture**.
* Developing **interactive dashboards**.
* Portfolio-ready demonstration of **real-world DE skills**.

## Future Enhancements

* Deploy pipelines on **AWS/GCP**.
* Integrate **Spark** for large-scale data.
* Implement **data quality validation** (Great Expectations).
* Add **monitoring & alerting** (Prometheus/Grafana).

## License

MIT License
