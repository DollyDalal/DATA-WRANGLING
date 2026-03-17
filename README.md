# 🧹 Data Wrangling in Python 🐍

## 📌 Introduction

Data wrangling (also called data cleaning or data preprocessing) is the process of transforming raw data into a clean and usable format. It is an important step before performing analysis or building models.

---

## ⚙️ Requirements

Make sure you have the following installed:

```bash
pip install pandas numpy
```

---

## 📥 Import Libraries

```python
import pandas as pd
import numpy as np
```

---

## 📂 Load Dataset

```python
df = pd.read_csv("data.csv")
print(df.head())
```

---

## 🔍 Explore Data

```python
df.info()        # structure of data
df.describe()    # statistical summary
df.shape         # rows and columns
df.columns       # column names
```

---

## ❌ Handle Missing Values

```python
df.isnull().sum()        # check missing values

df.dropna()              # remove missing values
df.fillna(0)             # replace with 0
df.fillna(method='ffill')  # forward fill
```

---

## 🔁 Remove Duplicates

```python
df.duplicated().sum()    # check duplicates
df.drop_duplicates(inplace=True)
```

---

## 🏷️ Rename Columns

```python
df.rename(columns={'old_name':'new_name'}, inplace=True)
```

---

## 🔄 Change Data Types

```python
df['Age'] = df['Age'].astype(int)
df['Date'] = pd.to_datetime(df['Date'], errors='coerce')
```

---

## 🔎 Filter Data

```python
df[df['Age'] > 25]
df[df['City'] == 'Delhi']
```

---

## ➕ Add New Column

```python
df['Total'] = df['Price'] * df['Quantity']
```

---

## 🔗 Merge DataFrames

```python
df1.merge(df2, on='ID', how='inner')
```

---

## 🧮 Group By

```python
df.groupby('Category')['Sales'].sum()
```

---

## 🔃 Sort Data

```python
df.sort_values(by='Price', ascending=False)
```

---

## 💾 Save Cleaned Data

```python
df.to_csv("cleaned_data.csv", index=False)
```

---

## 🎯 Conclusion

Data wrangling helps:

* ✅ Improve data quality
* ✅ Make analysis easier
* ✅ Increase accuracy of results


✨ Happy Coding! ✨
