# 📰 News Analysis Pipeline using Microsoft Fabric  

### 🚀 Project Overview  
This project builds a **scalable, automated data pipeline** for ingesting, processing, and analyzing news articles using **Microsoft Fabric**. The pipeline extracts news from the **Bing Search API** and performs **sentiment analysis** to gain insights from text data.  

### 🛠️ Tools & Technologies  

####  Data Ingestion & Orchestration  
- *Azure Data Factory* → Ingests news data from the **Bing API** and orchestrates the pipeline.  
####  Data Storage & Management  
- *OneLake* → Stores raw and processed data for efficient access.  
- *Lake Database* → Structured data repository for optimized querying and transformation.  
####  Data Processing & Transformation  
- *Synapse Data Engineering* → Uses **Spark notebooks** to clean, process, and convert raw data into **Delta tables**.  
####  Data Analysis & Insights  
- *Synapse Data Science* → Performs **sentiment analysis** on news articles to classify sentiment as **positive, negative, or neutral**.  

### 📌 Key Features  
✅ **Automated ingestion** of real-time news data from Bing API.  
✅ **Scalable data transformation** using **Spark-based processing**.  
✅ **Structured storage** with **Delta tables** for optimized querying.  
✅ **Sentiment analysis** for actionable insights on news trends.  
✅ **End-to-end orchestration** using Microsoft Fabric services.

### ⚙️ Environment Setup 
- Navigate to **Azure Portal** and Create a resource group named **DE-BP-Project-02**
- Inside the resource group, add: (Resource: **Bing Search v7**,Purpose: Fetch news data from Bing API)
- Set Up Power BI Workspace.
- Create a Microsoft Fabric Lakehouse (Switch to Data Engineering in the newly created Power BI workspace. Navigate to Lakehouse → Create a new Lakehouse.Name the database and click Create.)
