# 📈 Real-Time Stock Market Analytics using Microsoft Fabric

![Microsoft Fabric](https://img.shields.io/badge/Microsoft-Fabric-blue?logo=microsoft)
![Python](https://img.shields.io/badge/Python-3.11-yellow?logo=python)
![KQL](https://img.shields.io/badge/KQL-Database-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📖 Overview

This project demonstrates an **end-to-end real-time stock market analytics platform** built using **Microsoft Fabric Real-Time Intelligence**.

Live stock market data is collected using the **Yahoo Finance (yfinance) API**, processed through a **Microsoft Fabric Notebook**, streamed into **Fabric Eventstream**, stored in an **Eventhouse (KQL Database)**, and visualized through an interactive **Real-Time Dashboard**.

The entire ingestion process is fully automated using a **Microsoft Fabric Data Pipeline** with an hourly schedule trigger, enabling near real-time monitoring of stock prices and market trends.

---

# 🎯 Business Objective

Financial analysts and investors require continuously updated stock market information to monitor price movements and make informed decisions. Traditional batch-based reporting introduces delays that reduce responsiveness.

This project addresses these challenges by:

- ✅ Automatically collecting live stock market data
- ✅ Streaming data into Microsoft Fabric
- ✅ Storing historical stock events
- ✅ Delivering live dashboards with minimal latency

---

# 🏗️ Solution Architecture

```text
                    Yahoo Finance API
                          │
                          ▼
                 Fabric Notebook (Python)
                          │
                          ▼
              Fabric Data Pipeline
              (Hourly Schedule Trigger)
                          │
                          ▼
                  Fabric Eventstream
                          │
                          ▼
             Eventhouse (KQL Database)
                          │
                          ▼
          Real-Time Intelligence Dashboard
```

---

# ⚙️ Project Workflow

## 📥 Step 1 – Stock Data Extraction

A **Microsoft Fabric Notebook** uses the **yfinance** Python library to retrieve live stock information for selected companies.

### 📌 Monitored Stocks

| Symbol | Company |
|---------|----------|
| AAPL | Apple |
| MSFT | Microsoft |
| NVDA | NVIDIA |
| TSLA | Tesla |
| AMZN | Amazon |

### 📊 Collected Metrics

- Symbol
- Timestamp
- Current Price
- Open Price
- Previous Close
- Day High
- Day Low
- Volume
- Change Percentage

---

## ⏰ Step 2 – Automated Pipeline Execution

The notebook is executed automatically using a **Microsoft Fabric Data Pipeline**.

### Pipeline Features

- 📒 Notebook Activity
- ⏰ Hourly Schedule Trigger
- 🔄 Automated Execution
- 🚫 No Manual Intervention

This ensures fresh stock market data is collected every hour.

---

## 📡 Step 3 – Real-Time Streaming

After fetching stock prices, the notebook sends each record into **Microsoft Fabric Eventstream**.

### Eventstream Responsibilities

- Receives streaming events
- Processes incoming stock data
- Streams data into Eventhouse
- Enables low-latency ingestion

---

## 💾 Step 4 – Data Storage

Incoming events are stored inside an **Eventhouse (KQL Database)**.

### KQL Database Capabilities

- Time-series analysis
- Historical trend analysis
- Fast streaming queries
- Low-latency data retrieval

---

## 📊 Step 5 – Dashboard Visualization

A **Microsoft Fabric Real-Time Dashboard** is built on top of the KQL Database.

The dashboard refreshes automatically whenever new events arrive.

### Dashboard Insights

- 📈 Highest Price Reached
- 💲 Latest Stock Prices
- 📉 Price Trend
- 📦 Volume Trend
- 🚀 Top Gainers
- ⏱ Live Refresh Timestamp

---

# 🛠 Technology Stack

| Component | Technology |
|------------|------------|
| **Programming Language** | Python |
| **Data Source** | Yahoo Finance (yfinance API) |
| **Compute Engine** | Microsoft Fabric Notebook |
| **Orchestration** | Microsoft Fabric Data Pipeline |
| **Scheduling** | Hourly Schedule Trigger |
| **Streaming** | Microsoft Fabric Eventstream |
| **Storage** | Eventhouse (KQL Database) |
| **Query Language** | Kusto Query Language (KQL) |
| **Visualization** | Microsoft Fabric Real-Time Dashboard |

---

# 📊 Data Flow

```text
Yahoo Finance API
        │
        ▼
Fabric Notebook
        │
        ▼
Fabric Data Pipeline
(Hourly Trigger)
        │
        ▼
Fabric Eventstream
        │
        ▼
Eventhouse (KQL Database)
        │
        ▼
Real-Time Dashboard
```

---

# 📸 Project Screenshots

## 🖥️ 1. Workspace Lineage

Shows the complete Microsoft Fabric architecture connecting the Notebook, Pipeline, Eventstream, Eventhouse, and Dashboard.

<img width="1535" height="717" alt="Workspace Lineage" src="https://github.com/user-attachments/assets/86868ed3-5a46-4c84-a45e-7637a8022456" />

---

## 📡 2. Eventstream

Demonstrates real-time streaming of stock market events into the KQL Database.

<img width="1528" height="714" alt="Eventstream" src="https://github.com/user-attachments/assets/7d3dc090-bfcb-477d-afc3-9fc0410086aa" />

---

## 📊 3. Real-Time Dashboard

Displays live stock market insights including:

- Highest Price
- Latest Prices
- Price Trends
- Volume Trends
- Top Gainers

<img width="1503" height="715" alt="Dashboard" src="https://github.com/user-attachments/assets/620abc95-0a22-4d27-b53b-ea8a7ca94cef" />

---

# ✨ Features

- 🚀 End-to-End Microsoft Fabric Implementation
- ⏰ Automated Hourly Stock Price Collection
- 📡 Real-Time Event Streaming
- 💾 Historical Data Storage in Eventhouse
- 📊 Interactive Real-Time Dashboard
- ⚡ Low-Latency Analytics
- 📈 Live Market Monitoring
- 🔄 Fully Automated Data Pipeline

---

# 📚 Key Learnings

Through this project, I gained practical experience with:

- Microsoft Fabric Real-Time Intelligence
- Microsoft Fabric Notebooks
- Data Pipelines
- Schedule Triggers
- Eventstream
- Eventhouse
- KQL Database
- Kusto Query Language (KQL)
- Python Integration
- Real-Time Dashboard Development

---

# 🚀 Future Enhancements

- 📈 Support additional stock exchanges
- 🔔 Implement real-time alerts using Fabric Activator
- 📊 Calculate technical indicators (SMA, EMA, RSI, MACD)
- 📰 Integrate financial news sentiment analysis
- 🤖 Build predictive models using Microsoft Fabric Machine Learning
- 📉 Publish dashboards to Power BI

---

# 🎓 Skills Demonstrated

- Microsoft Fabric
- Real-Time Intelligence
- Python
- KQL
- Eventstream
- Eventhouse
- Data Engineering
- Data Pipelines
- Streaming Analytics
- Dashboard Development

---

# 👩‍💻 Author

**Indumathi Panchireddi**

**Software Trainee | Data & Advanced Analytics**

📌 Passionate about **Microsoft Fabric**, **Azure Data Engineering**, **Power BI**, and **Real-Time Analytics**.

---

⭐ **If you found this project interesting, consider giving it a star!**
