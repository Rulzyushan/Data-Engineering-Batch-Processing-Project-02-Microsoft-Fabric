# 📰 News Analysis Pipeline using Microsoft Fabric  

### 🚀 Project Overview  
This project builds a **scalable, automated data pipeline** for ingesting, processing, and analyzing news articles using **Microsoft Fabric**. The pipeline extracts news from the **Bing Search API** and performs **sentiment analysis** to gain insights from text data.  

### 🛠️ Tools & Technologies  

####  Data Ingestion & Orchestration  
- *Data Factory* → Ingests news data from the **Bing API** and orchestrates the pipeline.  
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

### 📥 Data Ingestion Process  

To ingest news data, a secure connection must be established between **Bing API** and **Microsoft Fabric Workspace**. Additionally, **authentication** is required to allow Fabric to access the data.  

#### 1️⃣ Create a New Data Pipeline  
- Navigate to **Microsoft Fabric → Data Factory**.  
- Click **Create Pipeline**, provide a meaningful name, and click **Create**.  

#### 2️⃣ Establish Connection Between Bing API and Fabric  
- Add a **Copy Data Activity** to the pipeline..  
- Under the **Source** tab of the **Copy Data Activity**:  
  - Set **Data Store Type** → **External**.  
  - Choose **REST** as the **Connection Type**.  
- Configure **Connection Settings**:  
  - Set the **Base URL** to:  
    ```plaintext
    https://api.bing.microsoft.com/v7.0/news/search
    ```
  - This API endpoint retrieves **news articles** based on user-defined search queries.  
#### 3️⃣ Steps for Authentication in Microsoft Fabric (Data Factory)
- Expand the "Advanced" Section in the Source tab of the Copy Data Activity.
- Provide Additional Headers:
  - Header Name → Subscription-Key
  - Header Value → API Key
  - Set the Relative URL
#### write these responses of the API in the data lakehouse 
- Go to the "Destination" Tab in Copy Data Activity.  
- Set Data Store Type → `Workspace`.  
- Select Workspace Data Store Type → `Lakehouse`.  
- Choose Lakehouse → `DE_BP_P_02_bing_lake_db`.  
- Set Root Folder → `Files`.  
- Specify File Path → `DE_BP_P_02_bing_Data`.  
- Select File Format → `JSON`.
### Data Transformation 

