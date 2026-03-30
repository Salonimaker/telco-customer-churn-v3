# 📉 Telco Customer Churn: v2 Optimization Phase

## 🎯 Project Goal
The objective of **v2** was to move beyond a simple baseline by implementing a high-sensitivity ensemble model. This phase focused on robust data engineering, exploratory data analysis (EDA), and strategic threshold tuning to prioritize customer retention.

## 🚀 Key v2 Achievements
* **Ensemble Transition:** Upgraded from a linear baseline to a **Random Forest Classifier** to capture complex, non-linear customer behaviors.
* **Strategic Threshold Tuning:** Shifted from an "Accuracy-Focused" to a **"Recall-Focused"** model by implementing a custom **0.22 decision threshold**.
* **High-Sensitivity Result:** Achieved a **83.6% Recall rate**, successfully identifying **312 out of 373** potential churners.

---

## 🛠️ Technical Implementation

### 1. Data Architecture (OOP)
Implemented a `TelcoChurnProject` Python class to manage the entire data lifecycle.
* **Robust Cleaning:** Handled hidden empty strings in `TotalCharges` using `errors='coerce'`.
* **Domain-Driven Imputation:** Filled missing values for new customers (`tenure=0`) with `0` instead of dropping data.
* **Feature Selection:** Dropped `customerID` to prevent model overfitting on unique strings.

### 2. Feature Engineering & Encoding
* **Binary Mapping:** Converted Yes/No features (Partner, Dependents, Churn) to 1/0.
* **Label Encoding:** Transformed multi-categorical features like `InternetService` and `Contract` for model compatibility.
* **Scaling:** Applied `StandardScaler` to numerical features (`tenure`, `MonthlyCharges`) to ensure balanced feature weight.

### 3. High-Sensitivity Model Performance
By applying a **0.22 threshold** and **Balanced Class Weights**, the model reached the following metrics:

| Metric | Score |
| :--- | :--- |
| **Recall (Churners)** | **83.6%** |
| **Accuracy** | 73.0% |
| **Precision** | 49.0% |

> **Note:** The trade-off for high recall in this version is a higher "False Alarm" rate (325 False Positives), which serves as the primary motivation for the optimization in v3.

---

## 📊 Key Insights
* **Top Churn Drivers:** The Random Forest identified `TotalCharges`, `MonthlyCharges`, and `tenure` as the top three predictors of churn.
* **Contract Risk:** Visual EDA confirmed that **Month-to-Month** contracts and **Fiber Optic** internet services are the highest indicators of customer turnover.



## 🛠️ Requirements
* `pandas`, `numpy`
* `matplotlib`, `seaborn`
* `scikit-learn`
