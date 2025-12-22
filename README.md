# 🫀 Heart Disease Detection: A Multi-Tiered Analytical Approach

A comprehensive **data science project** integrating **Diagnostic, Predictive, and Prescriptive Analytics** to improve heart disease detection and clinical decision-making.

---

## 📌 Project Overview

Cardiovascular diseases (CVDs) are the leading cause of global mortality, responsible for approximately **17.9 million deaths annually**.  
This project addresses the limitations of manual diagnosis by implementing a **data-driven analytical framework**:

### 🔍 Diagnostic Analytics
- Investigates historical correlations
- Identifies key clinical indicators using statistical hypothesis testing

### 🤖 Predictive Analytics
- Develops machine learning models to predict patient risk
- Prioritizes **minimizing False Negatives** by maximizing **Recall**

### 🧭 Prescriptive Analytics
- Translates model outputs into **actionable clinical strategies**
- Supports early intervention and decision-making

**Primary Outcome:**  
A robust detection system achieving **91.15% Recall** using the **Support Vector Machine (SVM)** model.

---

## 📊 Dataset Description

The analysis uses a heart disease dataset consisting of **900+ patient records** with **11 independent features** and **1 target variable**.

| Feature           | Type         | Description |
|------------------|--------------|-------------|
| Age              | Numerical    | Age of the patient |
| Sex              | Categorical  | Gender (M/F) |
| ChestPainType    | Categorical  | TA, ATA, NAP, ASY |
| RestingBP        | Numerical    | Resting blood pressure (mm Hg) |
| Cholesterol      | Numerical    | Serum cholesterol (mm/dl) |
| FastingBS        | Binary       | Fasting blood sugar > 120 mg/dl (1: True, 0: False) |
| RestingECG       | Categorical  | Normal, ST, LVH |
| MaxHR            | Numerical    | Maximum heart rate achieved |
| ExerciseAngina   | Binary       | Exercise-induced angina (Y/N) |
| Oldpeak          | Numerical    | ST depression induced by exercise |
| ST_Slope         | Categorical  | Slope of peak exercise ST segment (Up, Flat, Down) |
| **HeartDisease** | Target       | Output class (1: Disease, 0: Normal) |

---

## 🧪 Methodology

### 1️⃣ Data Cleansing
- Handled missing/invalid values (`0` values in **RestingBP** and **Cholesterol**)
- Applied **Median Imputation** to preserve distribution robustness

### 2️⃣ Diagnostic Statistical Testing
- **Chi-Square Test** for categorical features  
- **Independent T-Test** for numerical features  
- Statistical significance threshold: **p < 0.05**

### 3️⃣ Data Preprocessing
- **One-Hot Encoding** for categorical variables
- **StandardScaler** for numerical feature normalization

### 4️⃣ Modeling & Evaluation
- Models evaluated using **5-Fold Cross Validation**
- Algorithms tested:
  - Logistic Regression
  - Support Vector Machine (SVM)
  - Random Forest
  - K-Nearest Neighbors (KNN)
  - XGBoost
- Primary optimization metric: **Recall**

---

## 📈 Results & Model Performance

Model performance comparison with emphasis on **Recall** to reduce missed diagnoses.

| Model               | Accuracy | Precision | Recall | ROC AUC |
|--------------------|----------|-----------|--------|---------|
| **SVM**            | 0.870 ± 0.02 | 0.864 ± 0.04 | **0.912 ± 0.02** | 0.918 ± 0.02 |
| Logistic Regression| 0.861 ± 0.02 | 0.863 ± 0.03 | 0.892 ± 0.04 | **0.921 ± 0.02** |
| Random Forest      | 0.859 ± 0.03 | 0.863 ± 0.04 | 0.890 ± 0.02 | 0.919 ± 0.03 |
| KNN                | 0.850 ± 0.01 | 0.849 ± 0.03 | 0.888 ± 0.02 | 0.894 ± 0.03 |
| XGBoost            | 0.841 ± 0.02 | 0.848 ± 0.04 | 0.872 ± 0.03 | 0.916 ± 0.02 |

📌 **Selected Model:** Support Vector Machine (SVM)

---

## 🔑 Key Insights

### 🫀 Dominant Clinical Factors
- **ST_Slope**, **ChestPainType**, and **ExerciseAngina** show strong statistical significance
- **Flat** or **Down ST Slope** is a critical risk indicator

### 📉 Physiological Indicators
- Patients with heart disease tend to have:
  - **Lower MaxHR**
  - **Higher Oldpeak values**

### 🧬 Metabolic Correlation
- **Fasting Blood Sugar (Hyperglycemia)** significantly contributes to cardiovascular risk

---

## 🧠 Prescriptive Recommendations

Based on the analytical findings, the following strategies are proposed:

### 🚨 Priority Triage Protocol
- Patients with:
  - **Asymptomatic (ASY) chest pain**
  - **Flat or Down ST_Slope**
- Classified as **“Red Zone”** (Highest Priority)

### 🖥️ Clinical Decision Support System (CDSS)
- Integrate the **SVM model** into hospital systems
- Estimated **20% improvement** in diagnostic efficiency

### 🛡️ Preventive Intervention
- Automatic clinical alert for patients with:
  - **Predicted risk probability > 0.7**
- Enables early preventive and therapeutic actions

---

## 🛠️ Technologies Used

### Programming Language
- **Python**

### Libraries
- `pandas`, `numpy` – Data processing
- `scikit-learn` – Machine learning & evaluation
- `matplotlib`, `seaborn` – Data visualization
- `xgboost` – Advanced modeling

### Platform
- Google Colab / Jupyter Notebook

---

## 📜 License & Contributor

**Developer:** Elvin Aurelio  
**License:** No License
---

⭐ *If you find this project useful, consider giving it a star!*
