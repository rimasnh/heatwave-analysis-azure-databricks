# heatwave-analysis-azure-databricks
Distributed heatwave analysis using PySpark and Azure Databricks on NASA climate data.

# 🌍 Heatwave Analysis Using Azure Databricks & PySpark

## 📌 Project Overview

This project analyzes large-scale climate projection data from NASA NEX-GDDP to detect temperature trends and extreme heat patterns using distributed processing in Azure Databricks.

The workflow demonstrates how to:

- Download NetCDF climate data from AWS S3
- Process multi-dimensional scientific data
- Convert raw climate data into Spark DataFrames
- Store optimized datasets in Parquet format
- Engineer features such as continent classification
- Perform distributed aggregations
- Identify hottest and coldest days by continent
- Visualize temperature trends

This project showcases cloud-based big data processing and climate analytics using PySpark.

---

## 🛠 Tech Stack

- Azure Databricks
- Apache Spark (PySpark)
- Python
- AWS S3 (Public Climate Dataset)
- NetCDF4
- Xarray
- Pandas
- Matplotlib
- Parquet

---

## 🌎 Dataset

Source: NASA NEX-GDDP Climate Projections  
Variable Used: `tasmax` (Daily Maximum Temperature)  
Scenario: RCP 8.5  
Format: NetCDF (.nc)

---

## 🔄 Project Pipeline

### 1️⃣ Data Ingestion
- Created folder in DBFS
- Downloaded NASA climate projections from AWS S3 using boto3
- Stored NetCDF files in Databricks File System

### 2️⃣ NetCDF Processing
- Loaded `.nc` file using xarray
- Extracted subset of time, latitude, longitude
- Flattened multi-dimensional data
- Converted to Spark DataFrame

### 3️⃣ Data Storage Optimization
- Saved dataset in Parquet format
- Enabled efficient distributed querying

### 4️⃣ Data Preprocessing
- Converted temperature from Kelvin → Celsius
- Removed null values
- Extracted year, month, day from timestamp
- Created custom UDF to map latitude/longitude to continents

### 5️⃣ Heat Analysis
- Calculated daily average temperature
- Aggregated by continent
- Identified hottest and coldest days using Window functions
- Visualized Antarctica daily temperature trend

---

## 🔥 Heatwave Analysis Logic

Although the dataset represents projected climate data, the analysis simulates heatwave detection by:

- Computing daily average maximum temperatures
- Aggregating temperatures by region
- Comparing extremes across continents
- Identifying extreme temperature days

---

## 📊 Sample Analysis Outputs

- Daily temperature trend for Antarctica
- Continent-level temperature comparison
- Hottest and coldest day detection per continent

---

## 📈 Why This Project Matters

This project demonstrates:

- Distributed computing with Spark
- Handling scientific NetCDF data
- Cloud-based big data pipelines
- Climate data analytics
- Feature engineering using geospatial logic
- Performance optimization using Parquet

---

## 🚀 How to Run

### Option 1: Azure Databricks (Recommended)

1. Upload notebook to Databricks
2. Install required libraries
3. Mount or upload dataset to DBFS
4. Run all cells


