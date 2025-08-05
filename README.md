# PANDAS
# 📊 Pandas in Python - A Detailed Guide

## 🐼 What is Pandas?

**Pandas** is an open-source Python library used for **data manipulation**, **analysis**, and **cleaning**. It provides two primary data structures:

- `Series`: One-dimensional labeled arrays.
- `DataFrame`: Two-dimensional labeled data structures (like a table or spreadsheet).

Pandas is built on top of NumPy and integrates well with many other data science libraries like Matplotlib, Scikit-learn, and Seaborn.

---

## 🚀 Installation

```bash
pip install pandas

# 📚 Core Data Structures

## 1. Series  
A one-dimensional array-like object with labels (called **index**).

```python
import pandas as pd

data = pd.Series([10, 20, 30, 40])
print(data)
2. DataFrame
A two-dimensional table with rows and columns.

python
Copy
Edit
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35]
}

df = pd.DataFrame(data)
print(df)
📥 Reading and Writing Data
Reading from CSV:
python
Copy
Edit
df = pd.read_csv('filename.csv')
Writing to CSV:
python
Copy
Edit
df.to_csv('filename.csv', index=False)
Reading from Excel:
python
Copy
Edit
df = pd.read_excel('filename.xlsx')
🔍 Data Exploration
View top rows:
python
Copy
Edit
df.head()       # First 5 rows
df.head(10)     # First 10 rows
View bottom rows:
python
Copy
Edit
df.tail()
Get summary info:
python
Copy
Edit
df.info()
Get descriptive statistics:
python
Copy
Edit
df.describe()
🛠️ Data Manipulation
Selecting Columns:
python
Copy
Edit
df['Name']        # Single column
df[['Name', 'Age']]  # Multiple columns
Filtering Rows:
python
Copy
Edit
df[df['Age'] > 30]
Adding a Column:
python
Copy
Edit
df['Salary'] = [50000, 60000, 70000]
Dropping Columns/Rows:
python
Copy
Edit
df.drop('Age', axis=1)             # Drop column
df.drop([0, 1], axis=0)            # Drop rows by index
🔄 Data Cleaning
Handling Missing Values:
python
Copy
Edit
df.isnull()                       # Check for nulls
df.dropna()                       # Drop rows with missing values
df.fillna(0)                      # Replace nulls with 0
Renaming Columns:
python
Copy
Edit
df.rename(columns={'Name': 'FullName'}, inplace=True)
📊 Grouping and Aggregation
python
Copy
Edit
df.groupby('Department')['Salary'].mean()
📏 Sorting
python
Copy
Edit
df.sort_values(by='Age', ascending=False)
🔄 Merging & Joining
Concatenation:
python
Copy
Edit
pd.concat([df1, df2])
Merging:
python
Copy
Edit
pd.merge(df1, df2, on='id')
📈 Visualization (with Pandas + Matplotlib)
python
Copy
Edit
import matplotlib.pyplot as plt

df['Age'].plot(kind='hist')
plt.show()
📌 Common Use Cases
Data cleaning and preprocessing

Exploratory data analysis (EDA)

Time series analysis

Input/output operations with CSV/Excel/SQL

Feature engineering for machine learning

🔗 Resources
Pandas Documentation

Pandas GitHub

10 Minutes to Pandas

🧠 Summary
Pandas is a cornerstone of data science in Python. With its intuitive syntax and powerful features, it's a must-learn tool for:

Data analysts

Data scientists

Machine learning engineers

Anyone working with structured data

💬 License
Pandas is licensed under the BSD License. Feel free to use and contribute!

yaml
Copy
Edit

---

Would you like me to generate and give you this content as a downloadable `README.md` file?
