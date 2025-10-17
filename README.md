# 🌦️ Weather ETL Pipeline (PostgreSQL + Python)

A beginner-friendly **Data Engineering project** that extracts daily weather data from a public API, transforms it with Python, and loads it into a PostgreSQL database.

---

## 🚀 Project Overview

This project demonstrates a simple **ETL (Extract, Transform, Load)** pipeline:
1. **Extract**: Fetch daily weather data from the Open-Meteo API  
2. **Transform**: Clean and structure the data using Pandas  
3. **Load**: Store the processed data into a PostgreSQL table for analysis  

Ideal for learning data pipelines, API handling, and SQL integration.

---

## 🧰 Tech Stack

| Component | Tool |
|------------|------|
| Language | Python 3.x |
| Data Processing | Pandas |
| API | Open-Meteo (no API key needed) |
| Database | PostgreSQL |
| ORM / DB Connection | SQLAlchemy + psycopg2 |
| Visualization (optional) | Matplotlib or Plotly |

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/weather-etl-postgres.git
cd weather-etl-postgres
```

### 2️⃣ Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # for macOS/Linux
venv\Scripts\activate     # for Windows
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Configure Database Connection
```python
DB_URL = "postgresql+psycopg2://<username>:<password>@localhost:5432/weather_data"
```
_(Or use your Neon.tech connection string)_

### 5️⃣ Run the ETL Script
```bash
python main.py
```

## 🗃️ Database Schema

| Column     | Type      | Description            |
| ---------- | --------- | ---------------------- |
| date       | DATE      | Forecast date          |
| temp_max   | FLOAT     | Max temperature        |
| temp_min   | FLOAT     | Min temperature        |
| created_at | TIMESTAMP | Time data was inserted |

## 📊 Sample Output
```sql
SELECT * FROM daily_weather ORDER BY date DESC LIMIT 5;
```

## 🌍 API Reference

Open-Meteo API: https://open-meteo.com

Example endpoint:
```bash
https://api.open-meteo.com/v1/forecast?latitude=14.6&longitude=120.98&daily=temperature_2m_max,temperature_2m_min&timezone=Asia/Manila
```
### 🧩 Future Enhancements

- Add data visualization dashboard
- Schedule daily runs using CRON or Airflow
- Store raw data in AWS S3 (free tier)

## 🧑‍💻 Author

Jay — Software Developer & Aspiring Data Engineer 🚀

## 🪴 License

This project is open-source under the MIT License
```yaml
Would you like me to help generate a `requirements.txt` and starter code (`main.py` + `config.py`) next so you can push the first commit right after creating the repo?

```
