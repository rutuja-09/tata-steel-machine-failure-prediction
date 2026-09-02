# 🚀 Tata Steel Machine Failure Prediction System

## 📌 Project Overview

Machine failure can lead to significant production downtime, increased maintenance costs, and operational inefficiencies in industrial environments. This project develops a Machine Learning-based Predictive Maintenance System capable of identifying potential machine failures using machine operating parameters and failure indicators.

The solution leverages Exploratory Data Analysis (EDA), Statistical Hypothesis Testing, Feature Engineering, Machine Learning Modeling, Hyperparameter Optimization, and Model Evaluation to build a reliable machine failure prediction framework.

---

## 🎯 Business Problem

Industrial organizations require proactive maintenance strategies to minimize unexpected equipment failures.

This project aims to:

- Predict machine failures before breakdowns occur.
- Reduce unplanned downtime.
- Improve equipment reliability.
- Optimize maintenance scheduling.
- Support data-driven operational decisions.

---

## 📊 Dataset Features

The dataset contains machine operational and environmental parameters, including:

- Product Type
- Air Temperature [K]
- Process Temperature [K]
- Rotational Speed [rpm]
- Torque [Nm]
- Tool Wear [min]
- TWF (Tool Wear Failure)
- HDF (Heat Dissipation Failure)
- PWF (Power Failure)
- OSF (Overstrain Failure)
- RNF (Random Failure)

**Target Variable:**

- Machine Failure (0 = No Failure, 1 = Failure)

---

## 🔍 Exploratory Data Analysis (EDA)

Comprehensive EDA was performed using:

- Histograms
- Box Plots
- Count Plots
- Violin Plots
- Scatter Plots
- Pair Plots
- Correlation Heatmaps

### Key Findings

- Torque and Rotational Speed show strong relationships with machine failure.
- Air Temperature and Process Temperature are highly correlated.
- Product Type impacts failure occurrence.
- Failure indicators significantly influence machine failure prediction.

---

## 📈 Statistical Hypothesis Testing

The following statistical tests were conducted:

| Hypothesis | Statistical Test |
|------------|------------------|
| Torque vs Machine Failure | Independent T-Test |
| Product Type vs Machine Failure | Chi-Square Test |
| Air Temperature vs Process Temperature | Pearson Correlation Test |

Results confirmed statistically significant relationships among the selected variables.

---

## ⚙️ Data Preprocessing

### Data Cleaning
- Missing Value Analysis
- Outlier Detection using IQR Method

### Feature Engineering
- Label Encoding for categorical variables
- Feature Selection using correlation analysis and domain knowledge
- Removal of non-informative identifier columns

### Data Splitting
- Train-Test Split (80:20)
- Stratified Sampling

---

## 🤖 Machine Learning Models

### Model 1: Random Forest Classifier

Performance:

| Metric | Score |
|----------|----------|
| Accuracy | 99.61% |
| Precision | 95.76% |
| Recall | 78.84% |
| F1-Score | 86.48% |

---

### Model 2: Decision Tree Classifier

Performance:

| Metric | Score |
|----------|----------|
| Accuracy | 99.25% |
| Precision | 74.24% |
| Recall | 79.77% |
| F1-Score | 76.91% |

---

## 🔧 Hyperparameter Tuning

RandomizedSearchCV was used for model optimization.

### Best Random Forest Parameters

```python
{
    'n_estimators': 150,
    'max_depth': 15,
    'min_samples_split': 2
}
```

### Best Decision Tree Parameters

```python
{
    'max_depth': 15,
    'min_samples_split': 10,
    'min_samples_leaf': 4
}
```

Hyperparameter tuning improved model generalization and predictive performance.

---

## 🏆 Final Model Selection

The **Random Forest Classifier** was selected as the final production model due to:

- Highest overall Accuracy
- Strong Precision
- Better F1-Score
- Robust handling of feature interactions
- Lower risk of overfitting compared to a single Decision Tree

---

## 📌 Feature Importance

The most influential features were:

- Torque [Nm]
- Rotational Speed [rpm]
- Tool Wear [min]
- Air Temperature [K]
- Process Temperature [K]
- HDF
- PWF
- OSF
- TWF

These features directly represent machine operating conditions and failure mechanisms.

---

## 💾 Model Deployment Readiness

The final model was:

✅ Serialized using Joblib

✅ Reloaded successfully

✅ Tested on unseen data

✅ Verified for deployment readiness

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Joblib
- Google Colab






---

## 📈 Business Impact

This solution can help organizations:

- Reduce machine downtime
- Improve predictive maintenance planning
- Lower maintenance costs
- Increase equipment lifespan
- Improve operational efficiency
- Enable data-driven maintenance decisions

---

## 🔮 Future Enhancements

- Deploy using Flask/FastAPI
- Build an interactive Streamlit dashboard
- Integrate real-time sensor data
- Implement advanced ensemble models
- Deploy on cloud platforms (AWS, Azure, GCP)

---

## 👨‍💻 Author

**Rutuja Waghmare**

Machine Learning | Data Analytics | Generative AI 
