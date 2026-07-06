### 📈 Real-Time Stock Market Analytics using Microsoft Fabric
###📖 Overview

This project demonstrates an end-to-end real-time stock market analytics platform built using Microsoft Fabric Real-Time Intelligence. Live stock market data is collected using the Yahoo Finance (yfinance) API, processed through a Fabric Notebook, streamed into Eventstream, stored in a KQL Database (Eventhouse), and visualized through an interactive Real-Time Dashboard.

The entire ingestion process is fully automated using a Fabric Data Pipeline with an hourly schedule trigger, enabling near real-time monitoring of stock prices and market trends.

### 🎯 Business Objective

Financial analysts and investors require continuously updated stock market information to monitor price movements and make informed decisions. Traditional batch-based reporting introduces delays that reduce responsiveness.

This project addresses this challenge by building a streaming analytics pipeline capable of:

Automatically collecting live stock market data
Streaming data into Microsoft Fabric
Storing historical stock events
Delivering live dashboards with minimal latency
### 🏗️ Solution Architecture
                    Yahoo Finance API
                          │
                          ▼
                 Fabric Notebook (Python)
                          │
                          ▼
              Fabric Data Pipeline (Hourly Trigger)
                          │
                          ▼
                  Fabric Eventstream
                          │
                          ▼
               Eventhouse / KQL Database
                          │
                          ▼
              Real-Time Intelligence Dashboard
⚙️ Project Workflow
Step 1 – Stock Data Extraction

A Microsoft Fabric Notebook uses the yfinance Python library to retrieve live stock information for selected companies.

Monitored Stocks
Apple (AAPL)
Microsoft (MSFT)
NVIDIA (NVDA)
Tesla (TSLA)
Amazon (AMZN)
Collected Metrics
Symbol
Timestamp
Current Price
Open Price
Previous Close
Day High
Day Low
Volume
Change Percentage
Step 2 – Automated Pipeline Execution

The notebook is executed automatically using a Microsoft Fabric Data Pipeline.

Pipeline Features:

Notebook Activity
Schedule Trigger
Hourly execution
No manual intervention

This ensures fresh stock data is collected throughout the trading day.

Step 3 – Real-Time Streaming

After fetching stock prices, the notebook sends each record into a Fabric Eventstream.

The Eventstream acts as the real-time ingestion layer by:

Receiving streaming events
Validating incoming records
Forwarding data directly to Eventhouse
Step 4 – Data Storage

Incoming events are stored inside a KQL Database (Eventhouse).

The KQL database maintains historical stock records, enabling:

Time-series analysis
Historical trend analysis
Streaming queries
Low-latency data retrieval
Step 5 – Dashboard Visualization

A Microsoft Fabric Real-Time Dashboard is built on top of the KQL Database.

The dashboard refreshes automatically whenever new events arrive.

Dashboard includes:

📈 Highest Price Reached
📊 Latest Stock Prices
📉 Price Trend
📦 Volume Trend
📊 Top Gainers
⏱ Live Refresh Timestamp
🛠️ Technology Stack
Component	Technology
Programming Language	Python
Data Source	Yahoo Finance (yfinance API)
Compute	Microsoft Fabric Notebook
Orchestration	Fabric Data Pipeline
Scheduling	Hourly Schedule Trigger
Streaming	Microsoft Fabric Eventstream
Storage	Eventhouse (KQL Database)
Query Language	Kusto Query Language (KQL)
Visualization	Fabric Real-Time Dashboard

### 📊 Data Flow
Yahoo Finance API
        │
        ▼
Fabric Notebook
        │
        ▼
Hourly Pipeline Trigger
        │
        ▼
Fabric Eventstream
        │
        ▼
Eventhouse (KQL Database)
        │
        ▼
Real-Time Dashboard
### 📸 Project Screenshots
1️⃣ Workspace Lineage

Shows the complete Microsoft Fabric architecture connecting the Notebook, Pipeline, Eventstream, Eventhouse, and Dashboard.

(Insert your first screenshot here)

2️⃣ Eventstream

Demonstrates real-time streaming of stock market events into the KQL Database.

(Insert your second screenshot here)

3️⃣ Real-Time Dashboard

Displays live stock market insights including:

Highest Price
Latest Prices
Price Trends
Volume Trends
Top Gainers

(Insert your third screenshot here)

### ✨ Features
End-to-end Microsoft Fabric implementation
Automated hourly stock price collection
Real-time event ingestion
Historical data storage in Eventhouse
Interactive real-time dashboard
Low-latency analytics
Scalable streaming architecture
### 📚 Key Learnings

This project provided hands-on experience with:

Microsoft Fabric Real-Time Intelligence
Fabric Notebooks
Data Pipelines
Schedule Triggers
Eventstream
Eventhouse
KQL Database
Kusto Query Language (KQL)
Python Integration
Real-Time Dashboard Development
### 🚀 Future Enhancements
Add support for additional stock exchanges
Implement real-time alerts using Fabric Activator
Calculate technical indicators (SMA, EMA, RSI, MACD)
Integrate financial news sentiment analysis
Build predictive models using Microsoft Fabric ML
Publish dashboards to Power BI
