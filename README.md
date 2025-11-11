# PySpark

---

# ⚡ PySpark Basics for Beginners

A **beginner-friendly PySpark repository** containing essential functions, transformations, and actions to help you quickly learn and apply **Apache Spark** for big data processing and distributed computing.

This repo is designed as a **hands-on guide** to start learning PySpark from scratch — covering DataFrames, RDDs, SQL, and commonly used operations.

---

## 📌 What You’ll Learn here

* 🔹 Setting up PySpark environment
* 🔹 Creating RDDs & DataFrames
* 🔹 Basic operations: `select`, `filter`, `withColumn`, `groupBy`, `agg`, etc.
* 🔹 Handling missing values & data cleaning
* 🔹 Joins & SQL queries with SparkSQL
* 🔹 Common transformations & actions
* 🔹 Saving and loading data (CSV, Parquet, JSON)

---

## 📁 Repository Structure

```bash
pyspark-basics/
│
├── notebooks/                # Jupyter notebooks for practice
│   ├── 01_intro.ipynb
│   ├── 02_dataframes.ipynb
│   ├── 03_transformations.ipynb
│   └── 04_spark_sql.ipynb
│
├── examples/                 # Python scripts with basic functions
│   ├── dataframe_examples.py
│   ├── rdd_examples.py
│   └── spark_sql_examples.py
│
├── requirements.txt          # Dependencies
└── README.md                 # You are here 🚀
```

---

## ⚙️ Installation & Setup

1️⃣ **Install PySpark** (locally):

```bash
pip install pyspark
```

2️⃣ **Verify Installation**:

```bash
python -c "import pyspark; print(pyspark.__version__)"
```

3️⃣ **Start Jupyter Notebook** to practice:

```bash
jupyter notebook
```

---

## 🚀 Quick Start Example

```python
from pyspark.sql import SparkSession

# Create Spark session
spark = SparkSession.builder.appName("BeginnerApp").getOrCreate()

# Create DataFrame
data = [("Alice", 25), ("Bob", 30), ("Charlie", 35)]
df = spark.createDataFrame(data, ["Name", "Age"])

# Show data
df.show()

# Basic operations
df.select("Name").show()
df.filter(df.Age > 28).show()
```

Output:

```
+-------+---+
|   Name|Age|
+-------+---+
|  Alice| 25|
|    Bob| 30|
|Charlie| 35|
+-------+---+
```

---

## 📊 Topics Covered

* ✅ DataFrames & RDDs
* ✅ Transformations & Actions
* ✅ Joins & Aggregations
* ✅ SparkSQL queries
* ✅ File I/O (CSV, JSON, Parquet)
* ✅ Beginner-friendly examples

---

## 🧑‍💻 Who is this for?

* 🔹 Students learning **Big Data & Spark**
* 🔹 Data engineers starting with **ETL pipelines**
* 🔹 Beginners who want to practice **PySpark functions** hands-on

---

## 📌 Future Enhancements

* Add MLlib (Spark Machine Learning) basics
* Add streaming examples (Spark Streaming)
* Add optimization tips for large datasets

---

## 🪪 License

This project is licensed under the **MIT License** – feel free to use and contribute.

---

✨ **Happy Learning PySpark!** ✨
