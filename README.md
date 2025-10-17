---

# 🧮 Credit Data Preprocessing & Analysis

## 📘 Overview

This Google Colab notebook focuses on **exploring, cleaning, and preprocessing** a credit-related dataset (`train 2.csv`).
The goal is to prepare the data for downstream **machine learning modeling** — handling missing values, encoding categorical features, and engineering new numerical variables such as credit history age in months.

---

## ⚙️ Features & Workflow

### 1. **Data Import & Exploration**

* Imports the dataset using **Pandas**.
* Displays dataset info, shape, summary statistics, and missing value counts.

### 2. **Missing Values & Data Inspection**

* Checks for missing (`NaN` and `null`) values across all features.
* Investigates specific columns such as:

  * `Payment_Behaviour`
  * `Type_of_Loan`
  * `Credit_History_Age`

### 3. **Feature Engineering**

* Uses **Regular Expressions (regex)** to convert the `"Credit_History_Age"` string (e.g., `"22 Years and 3 Months"`) into a **single numeric column (months)**.
* Drops unnecessary or redundant columns:

  ```
  ["Name", "SSN", "ID", "Customer_ID", "Credit_History_Age"]
  ```

### 4. **Feature Categorization**

* Separates **numerical** and **categorical** columns for later use in model training and encoding.

---

## 🧰 Dependencies

Make sure the following libraries are installed (already included in Google Colab):

```python
import pandas as pd
import numpy as np
import re
```

---

## 🚀 Usage Instructions

1. **Open in Google Colab**
   Click this link or upload the `.ipynb` file to Colab.

2. **Upload your dataset**
   Replace `"train 2.csv"` with your own dataset file or upload via Colab’s file manager.

3. **Run all cells**
   Go to `Runtime > Run all` to execute the preprocessing pipeline.

4. **Inspect the cleaned dataframe**
   The notebook prints summary stats and data samples for validation.

---

## 📊 Output

After running the notebook:

* You’ll get a **cleaned Pandas DataFrame** ready for model training.
* Categorical and numerical columns are clearly separated.
* Invalid or redundant columns are dropped.
* Credit history values are transformed into consistent numeric formats.

---

## 💡 Future Work

* Apply **Label Encoding** or **One-Hot Encoding** to categorical columns.
* Implement **outlier detection** and **scaling**.
* Integrate **ML models** for classification or regression on the processed data.

---

## 🧑‍💻 Author

**Armen-Aris Shahinyan**
Student & Software Engineer Intern — combining data science with philosophical precision ⚔️

---
