# Credit Scoring Model 🏦

## 📌 Project Overview
This project predicts an individual's creditworthiness using past financial data.
Built as part of the **CodeAlpha Machine Learning Internship - Task 1**.

## 🎯 Objective
Classify individuals as credit-worthy or not using supervised machine learning algorithms.

## 📂 Dataset
- **Name:** German Credit Data
- **Rows:** 1000
- **Columns:** 21
- **Target Column:** `kredit` (1 = Good Credit, 2 = Bad Credit)
- **Features include:** loan duration, loan amount, employment status,
  marital status, age, existing credits, job type, and more.

## 🛠️ Technologies Used
- Python 3
- Google Colab
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

## ⚙️ Methodology

### 1. Data Preprocessing
- Loaded CSV from zip file
- Handled missing values using median imputation
- Encoded categorical columns using LabelEncoder

### 2. Feature Engineering
- Created new feature: `duration_amount_ratio = laufzeit / (hoehe + 1)`
- Scaled all features using StandardScaler

### 3. Models Trained
| Model | Description |
|---|---|
| Logistic Regression | Linear baseline classifier |
| Decision Tree | Rule-based tree (max_depth=5) |
| Random Forest | Ensemble of 100 trees |

## 📊 Evaluation Metrics
- Precision
- Recall
- F1-Score
- ROC-AUC Score

## 📈 Results

| Model | Precision | Recall | F1-Score | ROC-AUC | Accuracy |
| Logistic Regression | 0.82 | 0.88 | 0.85 | 0.8195 | 78% |
| Decision Tree | 0.82 | 0.85 | 0.83 | 0.7595 | 76% |
| Random Forest | 0.82 | 0.91 | 0.86 | 0.8296 | 80% |

## Best Model
**Random Forest** achieved the best overall performance with:
- Highest ROC-AUC: **0.8296**
- Highest Accuracy: **80%**
- Best Recall: **0.91** (catches most bad credit cases)

