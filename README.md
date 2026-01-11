![Status](https://img.shields.io/badge/Status-Completed-success)
![Type](https://img.shields.io/badge/Project-ML%20%7C%20Classification-blueviolet)
![Domain](https://img.shields.io/badge/Domain-Banking%20%26%20Finance-informational)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Accuracy](https://img.shields.io/badge/Model-XGBoost%20%7C%20SMOTE-brightgreen)

# PRODIGY_DS__-03
---

**Author:** Adeyeye Blessing Temidayo  
**CIN:** PIT/DEC25/10676  

## 🏦 Bank Marketing Campaign Predictive Analysis
This project implements a machine learning solution to predict whether a customer will subscribe to a term deposit based on a Portuguese bank's direct marketing campaigns.

## 📌 Project Overview
Telemarketing campaigns are resource-intensive. This project develops a predictive pipeline that identifies high-probability customers, allowing financial institutions to optimize their outreach, reduce operational costs, and improve conversion rates.

## 🎯 Key Objectives
- **Predictive Modeling:** Build a binary classifier to distinguish between "Yes" (subscriber) and "No" (non-subscriber).
- **Handle Class Imbalance:** Successfully address the significant 88/12 data skew using SMOTE.
- **Strategic Insights:** Identify key drivers of customer conversion to inform future marketing scripts.

## 🛠️ Technical Implementation

### Data Pipeline
- **Preprocessing:** Handled "unknown" values and utilized `ColumnTransformer` for categorical encoding and numerical scaling.
- **Class Balancing:** Implemented **SMOTE (Synthetic Minority Over-sampling Technique)** within an `ImbPipeline` to ensure balanced learning without data leakage.
- **Model Selection:** Compared Logistic Regression, Decision Trees, Random Forest, and **XGBoost**.



### Machine Learning Models
- **XGBoost (Champion Model):** Selected for its superior ROC-AUC performance and ability to handle non-linear relationships.
- **Optimization:** Hyperparameter tuning conducted via `GridSearchCV` to maximize Average Precision.

## 💻 Installation

```bash
# Clone the repository
git clone <https://github.com/Temidayo23/PRODIGY_DS__-03>
cd world-bank-population-analysis

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook world_bank_Data_Analysed.ipynb

```
----
📊 Evaluation & Results
Metric Focus: Prioritized ROC-AUC and F1-Score over accuracy due to the imbalanced nature of the dataset.

Performance: The XGBoost model effectively identifies potential subscribers, significantly reducing the "False Negative" rate.

Top Predictors: duration (call length), poutcome (previous success), and age emerged as the most influential features.

## 📂 Project Structure
```                
├── data/
│   ├── bank-full.csv
│   
├── figures                        # visualizations 
├── Bank_marketing-Analysed.ipynb  #  Main analysis notebook
├── LICENSE.md                     # Authorization to reproduce
├── README.md                      # Project Documentation
└──requirements.txt               # Python dependencies  
```

### 🧪 Methodology
1. Data Inspection
Validated 45,211 records with no duplicate rows.
Analysis of categorical distributions (Job, Education, Marital Status).

2. Exploratory Data Analysis (EDA)
Correlation analysis of numerical variables.

Visualizing the 7.55:1 imbalance ratio to justify resampling strategies.

3. Feature Engineering
One-Hot Encoding for categorical variables.

Standard Scaling for numerical features like balance and duration.

4. Model Building & Evaluation
 Train-Test Split (80/20).

Implementation of cross-validation within the pipeline.

Confusion Matrix and ROC Curve analysis.

### 📈 Future Scope
Duration Leakage Fix: Developing a version of the model that excludes the duration feature for true pre-call prediction.

Deployment: Wrapping the model in a FastAPI or Flask app for real-time lead scoring.

Economic Integration: Adding external macroeconomic indicators (e.g., monthly interest rates) to improve temporal accuracy.

### 📧 Contact
Adeyeye Blessing Temidayo Email: adeyeyeblessing2017@gmail.com

Feel free to reach out for collaborations or questions regarding this analysis!

### 📄 License
MIT License Copyright (c) 2026 Adeyeye Blessing Temidayo
Original Source - https://archive.ics.uci.edu/dataset/222/bank+marketing
Disclaimer: This project was developed as part of a Data Science internship with Prodigy InfoTech.
