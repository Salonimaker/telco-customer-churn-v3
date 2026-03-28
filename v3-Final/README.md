# 📡 Telco Customer Churn: Strategic Retention Engine (v3.0)

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Ensemble-orange.svg)
![Status](https://img.shields.io/badge/Project-v3.0--Optimized-green.svg)

## 📌 Project Overview
This repository contains the **v3 (Optimized)** iteration of a Telco Customer Churn prediction model. Moving beyond baseline classification, this version implements a **Soft-Voting Ensemble** and **Custom Threshold Tuning** to hit a business-critical **72% Recall target**.

### 🚀 The Evolution (The Quest for Balance)
* **v1 (Baseline):** Simple Logistic Regression (Recall ~52%). 
* **v2 (High-Sensitivity):** Random Forest (Recall ~82%). *Note: High recall but likely suffered from low precision/high false-alarm rate.*
* **v3 (Optimized Ensemble):** Soft-Voting (XGBoost + RF) + Threshold Calibration (**Recall 71.9%**). 
  * *Strategic Choice: v3 was selected for production because it offers the most stable 'Profit-to-Retention' ratio, reducing false positives while maintaining a high 70%+ capture rate.*

---

## 🛠 Key Technical Features
* **Consensus Ensemble:** Combines **XGBoost** and **Random Forest** via a Soft-Voting Classifier.
* **Class Imbalance Handling:** Implements **SMOTE-Tomek** to clean the decision boundary.
* **Precision-Recall Calibration:** Optimized the decision boundary to a **0.35 "Golden Threshold"**.

## 📊 Performance Metrics (v3)
| Metric | Score | Note |
| :--- | :--- | :--- |
| **Accuracy** | **77.9%** | High generalizability |
| **Recall (Churn)** | **71.9%** | Successfully capturing 7/10 churners |
| **Precision** | **56.5%** | Efficient marketing spend allocation |

---

## 💡 Business Recommendations
1.  **The "Bridge" Offer:** Target Month-to-Month users at the 6-month mark.
2.  **Technical Safety Net:** Bundle security features for high-risk Fiber Optic users.
3.  **The "72% Catch" Workflow:** Use the 0.35 threshold to prioritize weekly CRM outreach.

---

## 📁 Repository Structure
* `Telco_Churn_v3_Ensemble_Optimization.ipynb`: Full analytical pipeline.
* `requirements.txt`: Necessary libraries for reproducibility.
* `telco_churn_expert_model.pkl`: Serialized production-ready model package.
