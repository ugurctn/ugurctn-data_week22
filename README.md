# ugurctn-data_week22

## 🏠 Home Sales Analysis with PySpark

This project performs big data analysis on a real estate dataset using Apache Spark and PySpark in a Google Colab environment. The dataset includes home sales data that is loaded from an AWS S3 bucket and processed using Spark SQL.

### 📁 Project Structure

- **Jupyter Notebook**: `2025APR02_Home_Sales_starter_code_colab.ipynb`
- **Data Source**: CSV file hosted on AWS S3
- **Frameworks Used**:
  - Apache Spark (v3.5.5)
  - PySpark
  - Google Colab

### ⚙️ Setup Instructions

This notebook installs Spark and Java on Google Colab automatically. No local setup is needed. However, for reference:

1. **Install Spark and Java**:
    ```bash
    apt-get update
    apt-get install openjdk-17-jdk-headless
    wget http://www.apache.org/dist/spark/spark-3.5.5/spark-3.5.5-bin-hadoop3.tgz
    tar xf spark-3.5.5-bin-hadoop3.tgz
    pip install findspark
    ```

2. **Configure Environment Variables**:
    ```python
    os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-17-openjdk-amd64"
    os.environ["SPARK_HOME"] = "/content/spark-3.5.5-bin-hadoop3"
    ```

3. **Start Spark Session**:
    ```python
    from pyspark.sql import SparkSession
    spark = SparkSession.builder.appName("SparkSQL").getOrCreate()
    ```

### 📊 Features

- Loads home sales data using PySpark
- Displays schema and data preview
- Computes basic statistics (e.g., total row count)
- Prepares for further SQL-based querying and transformations

### 🔗 Dataset Source

[Home Sales CSV - AWS S3](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv)

### 📌 Notes

- This notebook is designed to be used in Google Colab.
- Intended for educational use as part of a Data Analytics Boot Camp.
