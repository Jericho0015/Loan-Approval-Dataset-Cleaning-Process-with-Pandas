# Data Cleaning Pipeline using Pandas (Loan Approval Dataset)

This project demonstrates how to clean and preprocess a loan approval dataset using **Pandas**. The goal is to transform raw input data into a structured and reliable form ready for analysis or machine learning.

Data cleaning is a fundamental step in any data project. This pipeline handles:
- Missing values
- Categorical text inconsistencies
- Data type corrections
- Outlier treatment

---

## 📦 Dataset Overview
The dataset includes information about applicants and loan decisions.

| Feature Category | Examples |
|-----------------|----------|
| Applicant Details | Gender, Marital Status, Education, Income |
| Loan Information | Loan Amount, Term, Credit History |
| Target Variable | Loan Approval Status |

**Rows:** 614  
**Columns:** 13  

---

## 🧠 Cleaning Steps Performed

### 1. Data Exploration
- Inspected dataset structure (`df.info()`)
- Generated descriptive statistics (`df.describe()`)

### 2. Handling Missing Values
- **Categorical columns** → filled using the **mode** (most frequent category)
- **Numeric columns** → filled using the **median** to avoid influence from outliers

### 3. Standardizing Data Types
Converted all string-based categorical fields to **`category`** types for consistency and efficient memory usage.

### 4. Text Normalization
- Removed extra whitespace
- Converted categorical values to lowercase for uniformity  
  *(Example: "Male" → "male")*

### 5. Outlier Treatment
- Applied **capping** on columns such as *LoanAmount* and *ApplicantIncome*
- Ensured extreme values do not distort analysis

---

## ✅ Final Output
The cleaned dataset:
- Contains **no missing values**
- Has consistent categorical formatting
- Numeric distributions are smoothed for modeling
- Ready for **EDA**, **visualizations**, or building a **loan approval prediction model**

The cleaned dataset was exported as:
