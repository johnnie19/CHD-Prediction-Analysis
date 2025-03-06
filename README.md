# ❤️ CHD Prediction Analysis

## 📌 Overview
Coronary Heart Disease (CHD) is a major global health concern, often leading to severe complications. This project focuses on predicting the **10-year risk** of CHD using **Machine Learning models** applied to a structured dataset with health-related variables.

The analysis covers:
- **Exploratory Data Analysis (EDA)**
- **Data Preprocessing & Feature Engineering**
- **Model Selection & Hyperparameter Tuning**
- **Performance Evaluation & Insights**

## 🎯 Project Goals
- Identify **key risk factors** contributing to CHD.
- Develop **predictive ML models** to assess CHD risk.
- Compare various **classification algorithms** to determine the best model.

---

## 📜 Dataset
- **Size**: 4000+ records
- **Features**: 16 attributes (both categorical & numerical)
- **Key Attributes**:
  - **Demographic**: Age, Gender, Education
  - **Behavioral**: Smoking, Physical Activity
  - **Medical History**: Blood Pressure, Diabetes, Heart Rate
  - **Target Variable**: **TenYearCHD (0 = No CHD, 1 = CHD Risk)**

---

## 🔍 Exploratory Data Analysis (EDA)
- **Correlation Matrix**: Identifies relationships between health factors.
- **Data Distribution**: Checks for imbalances in CHD risk classes.
- **Principal Component Analysis (PCA)**: Reduces dimensionality for improved model efficiency.

📊 **Key Findings**:
- **Smokers** have a higher likelihood of CHD.
- **Age & Blood Pressure** are strong predictors of CHD risk.
- **Diabetic individuals** show increased CHD susceptibility.

---

## 🛠 Data Preprocessing & Feature Engineering
- **Handling Missing Data**:
  - Removed features with excessive missing values (`education`, `BMI`).
  - Mean imputation for `glucose`, `totChol` based on risk levels.
- **Data Transformation**:
  - **Standardization** of numerical features (`BP`, `cholesterol`).
  - **One-Hot Encoding** for categorical variables (`Gender`, `Smoking`).
- **Feature Engineering**:
  - **Interaction terms** (`age * cigsPerDay`, `BMI * glucose`).
  - **Mean Arterial Pressure (MAP)** derived from BP values.

---

## 🤖 Machine Learning Models
| Model                 | Accuracy | Precision | Recall | ROC AUC |
|----------------------|-----------|-----------|-----------|-----------|
| **Logistic Regression**  | 66.5% | 25.7% | 65.0% | 69.8% |
| **CatBoost**           | 66.5% | 24.9% | 60.9% | 68.6% |
| **LogitBoost**         | 85.4% | 70.0% | 5.7%  | 66.8% |
| **Random Forest**      | 85.2% | 66.7% | 3.2%  | 68.0% |

📌 **Best Model**:  
- **Logistic Regression & CatBoost** performed best when considering recall.
- **Random Forest & LogitBoost** showed high accuracy but low recall, making them **less ideal for critical healthcare predictions**.

---
