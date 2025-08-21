# 📊 Regression Experiments

This repository explores regression techniques including **Ridge Regression**, **Lasso Regression**, and **Polynomial Regression**, applied to different datasets.  
The goal is to evaluate model performance, feature selection, and prediction accuracy.

---

## 📂 Project Overview
- Perform **regularized regression** (Ridge, Lasso) and compare results.
- Explore **high-dimensional sparse data** and **correlated feature groups** with Lasso.
- Compare **linear vs polynomial (quadratic) regression** on synthetic data.
- Evaluate models using **R² score** and **Root Mean Squared Error (RMSE)**.
- Analyze **selected features** from Lasso regression.

---

## ⚡ Implemented Models

### 1. Ridge Regression
- Dataset: `ridge_10feat_150.csv`  
- Uses **RidgeCV** with cross-validation to select the best alpha.  
- Reports:
  - Best α (regularization strength)
  - Coefficients & intercept
  - R² score and RMSE

---

### 2. Lasso Regression (Sparse Data)
- Dataset: `lasso_sparse_150.csv`  
- Uses **LassoCV** with 5-fold cross-validation.  
- Reports:
  - Best α
  - Selected features (non-zero coefficients)
  - R² score and RMSE

---

### 3. Lasso Regression (Correlated Groups)
- Dataset: `lasso_groups_150.csv`  
- Goal: Check how Lasso handles correlated feature pairs (xA/xB, xC/xD).  
- Reports:
  - Best α
  - Coefficients & intercept
  - Which feature in each correlated pair is **kept** or **dropped**
  - R² score and RMSE

---

### 4. Polynomial (Quadratic) vs Linear Regression
- Dataset: `poly_quadratic_150.csv`  
- Models:
  - Linear Regression (y ~ x)
  - Polynomial Regression (y ~ x + x²)
- Reports:
  - Intercept and coefficients
  - R² score and RMSE
  - Prediction at **x = 1.5** using the quadratic model

---

## 📈 Evaluation Metrics
- **R² Score**: Measures goodness of fit (higher is better).  
- **RMSE**: Measures prediction error (lower is better).  

---

## 🎯 Key Insights
- **Ridge** helps stabilize coefficients by penalizing large weights.  
- **Lasso** performs feature selection by shrinking some coefficients to zero.  
- In **correlated groups**, Lasso tends to keep one feature and drop the other.  
- **Quadratic models** can capture non-linear trends better than linear baselines.  

---

## 🛠️ Tools & Libraries
- Python 3  
- NumPy, Pandas  
- Scikit-learn (LinearRegression, RidgeCV, LassoCV, PolynomialFeatures)  
- Matplotlib / Seaborn (optional for visualization)

---