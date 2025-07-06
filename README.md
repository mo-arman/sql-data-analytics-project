# 📊 Exploratory Data Analysis with SQL – Call Center Dataset

This project showcases a comprehensive **Exploratory Data Analysis (EDA)** using SQL, applied to a real-world **Call Center dataset**. The goal is to uncover hidden patterns, trends, and performance metrics by transforming raw data into actionable insights — all without using any BI tools or external programming languages.

---

## 🧠 Objective

To perform **EDA using pure SQL** by:
- Ingesting raw CSV data
- Cleaning, transforming, and standardizing datasets
- Exploring patterns in SLA compliance, call durations, and escalation rates
- Generating insights directly from SQL queries

---

## 🏗️ Project Structure

| Layer  | Description |
|--------|-------------|
| **Bronze** | Raw CSV data ingestion using `BULK INSERT` |
| **Silver** | Cleaning, standardizing, and formatting data |
| **Gold** | Final queries for analytics, KPIs, and insights |

---

## 📈 Key EDA Highlights

- Call volume trend analysis (daily/weekly)
- SLA-based performance breakdown
- Identification of longest/shortest calls
- Call escalation behavior
- Nulls, duplicates, and formatting issues resolved

---

## 📁 Folder Overview


---

## 🛠️ Tools & Tech

- SQL Server (or any RDBMS)
- SQL (DDL + DML)
- BULK INSERT
- Query tuning (joins, filters, case logic, window functions)

---

## 🚀 How to Run

1. Clone this repository  
   `git clone https://github.com/mo-arman/sql-data-analytics-project`

2. In your SQL tool (SSMS / DBeaver / Azure Data Studio):
   - Execute `bronze` scripts to ingest CSVs  
   - Apply cleaning using `silver` layer  
   - Run `gold` layer queries to explore insights

---

## 📌 Sample Insight Query

```sql
SELECT call_date,
       COUNT(*) AS total_calls,
       AVG(duration) AS avg_duration,
       SUM(CASE WHEN sla_met = 'No' THEN 1 ELSE 0 END) AS missed_sla
FROM gold.call_center_data
GROUP BY call_date
ORDER BY call_date;

👨‍💻 About Me
Mohammad Arman
Aspiring Data Analyst | SQL • Power BI • Python • Excel
This project reflects my passion for turning raw data into meaningful narratives using structured querying alone.

🔗 LinkedIn

🏷️ Tags
#SQL #EDA #DataAnalytics #CallCenterData #PortfolioProject #DataCleaning
