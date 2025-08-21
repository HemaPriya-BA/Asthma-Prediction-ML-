# Asthma Prevalence Prediction with Machine Learning

## 📌 Overview
This project predicts county-level prevalence of current asthma (CASTHMA) in the United States using machine learning. Built on the CDC PLACES dataset, it blends behavioral, preventive, and spatial features to train models that are both accurate and interpretable for small-area health estimation.

## 🧠 Objective
- Produce CASTHMA predictions at the county scale.
- Compare the performance of multiple regression models.
- Add spatial context and quantify model uncertainty with Gaussian Process Regression (GPR).

## 🗂️ Data Source
- **CDC PLACES**: <https://www.cdc.gov/places/>
- Example features: smoking prevalence, preventive health behaviors, and geographic coordinates (latitude/longitude), among others.

## 🛠️ Methods Used
- **Data preprocessing**: cleaning, feature selection, MinMax scaling  
- **Feature engineering**: cyclical encodings for spatial variables  
- **Models trained**:
  - Linear Regression
  - Ridge Regression
  - Support Vector Regression (SVR)
  - Gradient Boosting (with hyperparameter tuning)
  - Neural Network (MLP)
  - Gaussian Process Regression (GPR)
- **Tuning**: `RandomizedSearchCV`  
- **Evaluation**: R² and Mean Squared Error (MSE)

## 📊 Key Findings
- **SVR** and **tuned Gradient Boosting** performed best, each reaching **R² ≈ 0.79**.
- **Gradient Boosting** achieved the **lowest test MSE (~0.0012)**, indicating strong predictive accuracy.
- **GPR** delivered **95% confidence intervals**, enabling uncertainty-aware interpretation.
- **MLP (neural network)** underperformed, likely due to dataset size and complexity.

## 📈 Visualization
- Scatter plots of actual vs. predicted CASTHMA.
- GPR-based confidence interval visualizations.
- Feature importance summaries from tree-based models.

## ✅ Requirements
- Python 3.8+
- scikit-learn
- pandas
- numpy
- matplotlib / seaborn
- scipy

Install dependencies:
```bash
pip install -r requirements.txt
