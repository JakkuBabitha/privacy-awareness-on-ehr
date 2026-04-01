# 🛡️ Diabetes Data Privacy Pipeline

> A data processing and privacy-preserving pipeline for a diabetes dataset using techniques like data cleaning, k-anonymity, l-diversity, and differential privacy.

---

## 📌 Overview

This project focuses on:
- Cleaning and preprocessing a healthcare dataset
- Performing feature engineering
- Applying privacy-preserving techniques
- Generating a protected dataset for safe analysis

It simulates a real-world Electronic Health Records (EHR) privacy system.

---

## 🚀 Features

- Data Cleaning & Preprocessing  
- Exploratory Data Analysis (EDA)  
- Feature Engineering (Age groups, BMI categories)  
- Privacy Techniques:
  - k-Anonymity  
  - l-Diversity  
  - Differential Privacy  
- Visualization of privacy impact  
- Export of final protected dataset  

---

## 📂 Project Structure

```
.
├── dpd.ipynb
├── diabetes_prediction_dataset.csv
├── diabetes_final_protected.csv
└── README.md
```

---

## 🛠️ Technologies Used

- Python  
- pandas  
- numpy  
- matplotlib  

---

## ⚙️ Workflow

### 1. Data Loading
- Loads diabetes dataset
- Displays basic information

### 2. Data Cleaning
- Removes invalid rows (e.g., gender = "Other")
- Fixes impossible values (BMI, glucose levels)
- Handles missing values using mean imputation
- Removes duplicate records

### 3. Feature Engineering
- Age grouped into:
  - Young (<40)
  - Middle (40–60)
  - Senior (>60)
- BMI categorized:
  - Underweight, Normal, Overweight, Obese
- Risk scores calculated based on health conditions

### 4. Privacy Preservation

#### k-Anonymity
- Groups data based on quasi-identifiers:
  - Age group  
  - Gender  
  - Smoking history  
- Ensures each group has at least k=5 records

#### l-Diversity
- Ensures diversity in sensitive attribute (diabetes)
- l = 2 (minimum unique values per group)

#### Differential Privacy
- Adds Laplace noise to:
  - HbA1c levels  
  - Blood glucose levels  
- Uses epsilon = 1.0

---

## 📊 Visualization

The notebook generates plots showing:
- Dataset size across stages
- Effect of anonymization
- Privacy vs data utility comparison

---

## ▶️ How to Run

### 1. Install dependencies
```
pip install pandas numpy matplotlib
```

### 2. Run the notebook
```
jupyter notebook dpd.ipynb
```

---

## 📁 Output

- diabetes_final_protected.csv  
  → Fully processed and privacy-protected dataset

---

##  Example Pipeline Summary

- Original dataset loaded  
- Invalid and missing data handled  
- Features engineered  
- Privacy techniques applied  
- Final dataset exported  

---
## ⭐ Future Improvements

- Add machine learning models for prediction  
- Use advanced anonymization tools (e.g., ARX)  
- Build an interactive dashboard (Streamlit)  

---
