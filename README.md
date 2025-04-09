# 📊 Analyze Data in a Data Lake with Apache Spark

This project demonstrates how to use **Apache Spark** in **Azure Synapse Analytics** to explore and analyze data stored in **Azure Data Lake Storage Gen2**.

---

## 🧰 Prerequisites

- Azure subscription
- Familiarity with PySpark and basic data engineering concepts

---

## 🚀 Setup Instructions

1. Clone the repository and run the setup script in Azure Cloud Shell (PowerShell):

   ```powershell
   git clone https://github.com/MicrosoftLearning/Dp-203-azure-data-engineer dp203
   cd dp203/Allfiles/labs/05
   ./setup.ps1
%%pyspark
df = spark.read.load('abfss://files@<your-datalake>.dfs.core.windows.net/sales/orders/*.csv', format='csv')
display(df.limit(100))
