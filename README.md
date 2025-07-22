#  Customer Churn Prediction Using Machine Learning

##  Project Overview

This project applies supervised machine learning techniques to predict **customer churn** for SyriaTel, a telecommunications company. Churn prediction is a critical problem in the telecom industry, where companies lose revenue due to customers leaving. Identifying customers likely to churn can help target interventions that improve retention.

The project includes:
- Business and data understanding
- Data preparation and visualization
- Modeling using Logistic Regression and Decision Tree
- Model evaluation with classification metrics and visualizations
- Actionable recommendations for the business

---

##  Dataset

**Source:** [Churn in Telecoms Dataset on Kaggle](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)

**File:** `SyriaTel Customer Churn.csv`

This dataset contains 3,333 customer records with the following key features:
- `account length`
- `international plan`
- `voice mail plan`
- `number vmail messages`
- `total day/evening/night/international minutes/calls/charges`
- `number customer service calls`
- `churn` (target variable)

---

##  Business Understanding

The objective is to **build a classification model** that can predict whether a customer will churn (`1`) or stay (`0`). This can help SyriaTel:
- Identify at-risk customers
- Take proactive steps to retain them (e.g., offer better plans or service)

---

##  Data Understanding

- The dataset is clean with no missing values.
- Churned customers represent ~14.5% of the total, indicating a **class imbalance**.
- Features like `international plan`, `voice mail plan`, and `number customer service calls` show strong relationships with churn.

**Visualizations included:**
- Correlation heatmap
- Count plots for categorical variables

---

##  Data Preparation

Steps taken:
- Converted `yes`/`no` values to binary.
- One-hot encoded categorical variables.
- Standardized numeric features for Logistic Regression.
- Split the data into train and test sets (80/20 split).
- Checked for class imbalance.

---

##  Models and Evaluation

### 1. Logistic Regression
- **Accuracy:** 84.8%
- **Precision:** 50%
- **Recall:** 23.8%
- **F1 Score:** 32.2%
- **Confusion Matrix:**  
  - TP = 21, FP = 15, TN = 551, FN = 80

### 2. Decision Tree Classifier
- **Accuracy:** 94.8%
- **Precision:** 89.3%
- **Recall:** 74.3%
- **F1 Score:** 81.1%
- **Confusion Matrix:**  
  - TP = 74, FP = 20, TN = 546, FN = 27

**Visuals included:**
- Confusion matrix for both models
- Feature importance bar chart (Decision Tree)
- ROC Curve (Decision Tree)

---

##  Key Insights

- **Decision Tree outperformed Logistic Regression** across all metrics, especially in detecting churned customers (recall ↑).
- **Top predictive features** included:
  - `number customer service calls`
  - `international plan`
  - `total day charge`
  - `voice mail plan`
  - `account length`

---

##  Recommendations

Based on the model outputs and data analysis, SyriaTel can take the following actions:

1. **Target customers with frequent support calls:** They are highly likely to churn. Improve resolution quality or assign them to a retention team.
2. **Monitor international plan users:** This group has a higher churn rate and might need better international calling packages or service bundles.
3. **Use the model to score current customers:** Continuously evaluate churn probability and trigger marketing or customer success workflows for high-risk individuals.

---

##  Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn & Matplotlib
- Jupyter Notebook

---

##  Files Included

- `phase 3 ML project.ipynb`: Full notebook with code, analysis, visualizations, and evaluation
- `SyriaTel Customer Churn.csv`: Original dataset
- `README.md`: Project documentation
- `phase 3 ML presentation.ppt`

---


