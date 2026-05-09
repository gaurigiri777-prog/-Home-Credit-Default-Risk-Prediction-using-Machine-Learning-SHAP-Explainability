# 🏦 Home Credit Default Risk Prediction using Machine Learning & SHAP Explainability

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![SHAP](https://img.shields.io/badge/Explainable-AI-green)
![Random Forest](https://img.shields.io/badge/Model-RandomForest-red)
![Status](https://img.shields.io/badge/Project-Completed-success)

## 📌 Project Overview

Financial institutions face a major challenge in identifying customers who are likely to default on loans.

This project builds an **End-to-End Credit Risk Prediction System** using the **Home Credit Default Risk dataset** to predict whether a customer is likely to default on a loan.

The project focuses not only on prediction accuracy but also on **model explainability using SHAP (SHapley Additive Explanations)** to understand why the model makes specific decisions.


<img width="1672" height="941" alt="COVER IMAGE" src="https://github.com/user-attachments/assets/a9a7c3ba-7202-403a-b0bc-5d6f21751845" />

---

## 🎯 Business Problem

Many individuals with insufficient credit history struggle to get loans.

The goal of this project is to:

- Predict customer default risk
- Minimize financial losses
- Improve loan approval decisions
- Build an explainable AI system for risk assessment

---

# 🚀 Project Workflow

```text
Data Collection
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis (EDA)
        ↓
Feature Engineering
        ↓
Categorical Encoding
        ↓
Train-Test Split
        ↓
Machine Learning Model
        ↓
Model Evaluation
        ↓
ROC-AUC Analysis
        ↓
SHAP Explainability
        ↓
Business Insights
```

---

# 📂 Dataset Information

Dataset Used:

**Home Credit Default Risk Dataset**

Target Variable:

| Target | Meaning |
|--------|---------|
| 0 | No Default |
| 1 | Default |

Dataset contains:

- Customer demographic information
- Loan details
- Income details
- Employment history
- Credit information

---

# 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Programming |
| Pandas | Data Processing |
| NumPy | Numerical Computing |
| Matplotlib | Visualization |
| Seaborn | Data Visualization |
| Scikit-learn | Machine Learning |
| SHAP | Explainable AI |

---

# 📊 Exploratory Data Analysis

The dataset was explored to understand:

- Missing values
- Class imbalance
- Customer demographics
- Income distribution
- Loan amount trends
- Credit behavior patterns

---

## 📸 EDA Screenshots


### Missing Value Analysis
<img width="1104" height="525" alt="MIssing value" src="https://github.com/user-attachments/assets/5e87710d-846b-4927-84cc-98741a3d1509" />


---

# ⚙️ Data Preprocessing

### Missing Value Handling

- Dropped columns with excessive missing values
- Imputed remaining missing values

### Feature Engineering

Created additional financial indicators:

```python
credit_income_ratio = AMT_CREDIT / AMT_INCOME_TOTAL
annuity_income_ratio = AMT_ANNUITY / AMT_INCOME_TOTAL
```

### Encoding

Applied **One-Hot Encoding** for categorical variables.

---

# 🤖 Machine Learning Model

### Model Used

✅ Random Forest Classifier

Why Random Forest?

- Handles complex relationships
- Works well with tabular data
- Robust against overfitting
- Feature importance support
- Compatible with SHAP explainability

---

# 📈 Model Performance

Evaluation Metrics Used:

- Accuracy Score
- Confusion Matrix
- Classification Report
- ROC Curve
- ROC-AUC Score

---

## 📸 Model Evaluation Screenshots

### Confusion Matrix
<img width="568" height="462" alt="Confusion Mtrix" src="https://github.com/user-attachments/assets/dbb71561-f237-4612-923c-fd05487b92ea" />


### ROC Curve
<img width="622" height="454" alt="ROC curve" src="https://github.com/user-attachments/assets/b247a28a-0b25-477f-a880-6f379e57af86" />


---

# 🧠 Explainable AI using SHAP

To make the model interpretable, **SHAP (SHapley Additive Explanations)** was used.

SHAP helps answer:

> Why did the model classify a customer as risky?

---

## SHAP Visualizations

### 1️⃣ SHAP Beeswarm Plot

Shows:

- Most important features
- Feature impact direction
- High vs Low feature values

<img width="830" height="361" alt="SHAP BEESWARM" src="https://github.com/user-attachments/assets/0c72b078-01ce-423f-899b-6e8ecdcc6639" />


---

### 2️⃣ SHAP Feature Importance Plot

Displays the most influential variables affecting loan default prediction.

<img width="736" height="709" alt="SHAP BAR PLOT" src="https://github.com/user-attachments/assets/800f960e-216a-438c-a9a1-9f7dea84a668" />


---

### 3️⃣ SHAP Waterfall Plot

Explains an individual customer's prediction.

Shows:

- Features increasing risk
- Features reducing risk
- Final prediction reasoning

<img width="833" height="465" alt="SHAP WATERFALL" src="https://github.com/user-attachments/assets/0201d0ef-d873-4f89-91e9-25d456d73c77" />

---

# 📌 Key Insights

### High Risk Indicators

- High credit-to-income ratio
- High annuity burden
- Lower income levels
- Unstable financial profile

### Low Risk Indicators

- Higher income
- Lower debt burden
- Better financial balance

---

# 📊 Results

| Metric | Score |
|--------|------|
| Accuracy | XX% |
| ROC-AUC | XX |
| Precision | XX |
| Recall | XX |

---

# 💼 Business Impact

This solution can help financial institutions:

✅ Reduce loan default losses

✅ Improve customer risk profiling

✅ Make explainable loan approval decisions

✅ Build trust through AI transparency

---

# 📁 Project Structure

```text
Home-Credit-Default-Risk/
│
├── data/
│   └── application_train.csv
│
├── notebook/
│   └── Home_Credit_Default_Risk.ipynb
│
├── images/
│   ├── class_distribution.png
│   ├── missing_values.png
│   ├── correlation_heatmap.png
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── shap_beeswarm.png
│   ├── shap_barplot.png
│   └── shap_waterfall.png
│
├── requirements.txt
│
├── README.md
│
└── LICENSE
```

---

# ▶️ How to Run the Project

### Clone Repository

```bash
git clone YOUR_GITHUB_LINK
```

### Install Requirements

```bash
pip install -r requirements.txt
```

### Run Notebook

```bash
jupyter notebook
```

---

# 📦 Requirements

```txt
pandas
numpy
matplotlib
seaborn
scikit-learn
shap
jupyter
```

---

# ⭐ Future Improvements

- XGBoost / LightGBM implementation
- Hyperparameter tuning
- Streamlit deployment
- Advanced feature engineering
- Multi-table Home Credit data integration

---

<img width="1007" height="371" alt="sHAP EXPLAIN" src="https://github.com/user-attachments/assets/62f5fda5-93d0-465f-9f8a-ad4fe9dd9e0e" />


# 👨‍💻 Author

**gAURI gIRI**

If you liked this project, consider giving it a ⭐ on GitHub!
