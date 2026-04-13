# 🛍️ Customer Purchase Propensity
## 📊 Data Cleaning and Feature Engineering Pipeline

Welcome to this practical data analysis project based on **Customer Purchase Propensity**.  
This project is designed to clean, preprocess, and transform raw customer data from multiple sources so it becomes ready for future machine learning use.

---

## 🎯 Objective

The main objective of this project is to prepare a dataset for a **binary classification problem**:

- 🟢 `purchased = 1` → Customer made a purchase
- 🔴 `purchased = 0` → Customer did not make a purchase

This project focuses only on:
- 🧹 Data Cleaning
- 🔧 Data Preprocessing
- 🏗️ Feature Engineering

It does **not** include model training.

---

## 📁 Project Files

Here are the files used in this project:

- 📄 `customers.csv` → Customer demographic details
- 📄 `transactions.json` → Transaction records
- 🗃️ `products.sql` → SQL script for product table
- 💾 `products.db` → SQLite database file
- 🌐 `api_users.json` → API data from DummyJSON users endpoint
- 📘 `Customer Purchase Propensity.ipynb` → Main Jupyter Notebook
- 📤 `processed_customer_data.csv` → Final processed dataset
- 📝 `summary_report.md` → Summary of project observations

---

## 🌍 API Used

This project also uses external API data from:

🔗 `https://dummyjson.com/users`

The API is used as an additional data source for user information.

---

## 🪜 Project Workflow

### 1. 📝 Project Planning and Problem Framing
- Understood what data analysis means
- Reviewed the steps in a data science project
- Framed the problem as a binary classification task

### 2. 📥 Data Import and Understanding
- Imported data from:
  - CSV
  - JSON
  - SQL
  - API
- Merged datasets using relevant keys like:
  - `customer_id`
  - `product_id`
- Explored data using:
  - `head()`
  - `info()`
  - `describe()`

### 3. 📊 Exploratory Data Analysis (EDA)
- Performed univariate analysis
- Performed bivariate analysis
- Performed multivariate analysis
- Used:
  - Histograms 📉
  - Scatter plots 🔵
  - Heatmaps 🌡️

### 4. 🧩 Handling Missing Data
Applied different missing value handling techniques:
- Simple Imputer
- Most Frequent Imputation
- Missing Indicator
- Random Sample Imputation
- KNN Imputer
- MICE Imputer
- Complete Case Analysis

### 5. 🚨 Outlier Detection and Handling
Used multiple outlier handling techniques:
- Z-score Method
- IQR Method
- Percentile Method
- Winsorization

### 6. 📅 Handling Date and Mixed Variables
- Converted columns into datetime format
- Created:
  - `days_since_signup`
  - `days_since_last_purchase`
- Handled mixed columns like customer code values

### 7. 🔤 Encoding Categorical Data
Applied:
- Label Encoding
- One Hot Encoding
- Ordinal Encoding
- Numerical binning for income groups

### 8. 📏 Feature Scaling
Applied:
- StandardScaler
- MinMaxScaler
- MaxAbsScaler
- RobustScaler
- Normalizer
- ColumnTransformer

### 9. 🏗️ Feature Construction and Transformation
Created and transformed features such as:
- `purchase_per_day`
- Log transformation
- Square root transformation
- Reciprocal transformation
- Power transformation
- Income binning
- Frequent buyer flag

### 10. 📤 Final Output
Exported the final transformed dataset as:

- ✅ `processed_customer_data.csv`

---

## 🧰 Technologies and Libraries Used

This project was completed using Python and the following libraries:

- 🐼 `pandas`
- 🔢 `numpy`
- 🗃️ `sqlite3`
- 📦 `json`
- 🌐 `urllib`
- 📉 `matplotlib`
- 🤖 `scikit-learn`

---

## 📌 Final Deliverables

The final deliverables of this project are:

- 📘 Jupyter Notebook
- 📤 Processed CSV Output
- 📝 Summary Report
- 📄 README File

---

## ▶️ How to Run the Project

Follow these simple steps:

1. Open the notebook file  
   📘 `Customer Purchase Propensity.ipynb`

2. Run all cells step by step

3. After execution, the final output file will be created:  
   📤 `processed_customer_data.csv`

---

## 📈 Outcome

At the end of this project, the raw data was successfully:
- cleaned ✅
- analyzed ✅
- transformed ✅
- feature engineered ✅
- exported for future machine learning use ✅

This project shows a complete preprocessing workflow for customer purchase prediction.

---

## 🙌 Author Details

- 👤 **Name:** Patel
- 🎓 **Role:** Junior Data Analyst Practical Exam
- 💼 **Project Domain:** Data Preprocessing and Feature Engineering

---

## ⭐ Thank You

Thank you for reviewing this project.  
This notebook demonstrates the essential steps needed before building a machine learning model on customer purchase data.
