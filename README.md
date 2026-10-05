# Pandas in Python: Your Data's Best Friend 🐼

## 📌 Overview

Pandas is one of the most widely used Python libraries for data manipulation and analysis. It provides powerful and convenient tools for working with structured data such as CSV files, Excel files, and datasets used in data science.

This repository accompanies the article **"Pandas in Python: Your Data's Best Friend"** and demonstrates practical Pandas concepts for working with data.

## 📚 Topics Covered

* Introduction to Pandas
* Installing and importing Pandas
* Creating DataFrames
* Reading and writing files
* Handling missing values
* Removing duplicate records
* Selecting columns
* Filtering rows
* Creating new columns
* Grouping and aggregation
* Exploratory Data Analysis (EDA)
* Merging datasets
* Data visualization
* Vectorized operations
* Method chaining
* Using `.apply()`

## 🛠️ Technologies

* Python
* Pandas
* Matplotlib
* Jupyter Notebook

## 📦 Installation

Install Pandas using pip:

```bash
pip install pandas
```

For visualization with Matplotlib:

```bash
pip install matplotlib
```

Import Pandas:

```python
import pandas as pd
```

## 📊 Creating a DataFrame

A Pandas DataFrame is a tabular data structure with labeled rows and columns.

```python
data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35],
    "City": ["New York", "Los Angeles", "Chicago"]
}

df = pd.DataFrame(data)

print(df)
```

## 📂 Reading and Writing Data

### Reading a CSV file

```python
df = pd.read_csv("data.csv")
```

### Writing to Excel

```python
df.to_excel("output.xlsx", index=False)
```

## 🧹 Data Cleaning

Real-world datasets often contain missing values and duplicate records.

### Handling Missing Values

```python
df.fillna("Unknown", inplace=True)
```

or:

```python
df.dropna(inplace=True)
```

### Removing Duplicates

```python
df.drop_duplicates(inplace=True)
```

## 🔎 Data Manipulation

### Selecting a Column

```python
ages = df["Age"]
print(ages)
```

### Filtering Rows

```python
adults = df[df["Age"] > 18]
print(adults)
```

### Adding a New Column

```python
df["Age in 10 Years"] = df["Age"] + 10
```

### Grouping and Aggregation

```python
city_counts = df.groupby("City").size()
print(city_counts)
```

## 📈 Exploratory Data Analysis

Pandas provides useful methods for quickly understanding a dataset.

```python
print(df.describe())
```

To inspect data types and non-null values:

```python
print(df.info())
```

## 🔗 Merging Datasets

Pandas can combine datasets using merge operations.

```python
df1 = pd.DataFrame({
    "ID": [1, 2],
    "Score": [85, 90]
})

df2 = pd.DataFrame({
    "ID": [1, 2],
    "Grade": ["A", "B"]
})

merged = pd.merge(df1, df2, on="ID")

print(merged)
```

## 📊 Data Visualization

Pandas integrates with visualization libraries such as Matplotlib.

```python
df["Age"].plot(kind="hist")
```

## ⚡ Useful Pandas Techniques

### Vectorized Operations

Operations can be performed directly on entire columns.

```python
df["Double Age"] = df["Age"] * 2
```

### Method Chaining

Multiple operations can be combined into a concise expression.

```python
result = df.dropna().sort_values("Age").head(3)
```

### Using `.apply()`

Custom functions can be applied to a column.

```python
df["Age Category"] = df["Age"].apply(
    lambda x: "Young" if x < 30 else "Old"
)
```

## 🎯 Learning Objective

The goal of this repository is to provide a practical introduction to Pandas and demonstrate how it can be used to:

* Work with structured datasets
* Clean messy data
* Manipulate and transform data
* Explore datasets
* Combine multiple datasets
* Create basic visualizations
* Prepare data for further data science and machine learning tasks

## 📝 Article

This repository is based on the Medium article:

**Pandas in Python: Your Data's Best Friend**

## 👩‍💻 Author

**Marishetty Ramyakrishna**

---

⭐ If this repository helped you learn Pandas, consider giving it a star!
