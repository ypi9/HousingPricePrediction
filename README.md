# Interpretable Modeling of Housing Prices Across Regions 🏡

This project explores how housing prices are influenced by a combination of **property-level structural features** and **external risk-related attributes**, such as environmental hazards and regional demographics. Our objective is to build **interpretable machine learning models** that identify the key drivers of housing price variations and provide localized, data-driven insights.

---

## 🎯 Project Objective

We aim to answer:

> _What structural and environmental factors most strongly influence property prices at a local level?_

Through this project, we hope to inform:
- 🏠 Homebuyers — seeking fair pricing and risk-aware decisions  
- 📈 Real estate investors — identifying value and risk trade-offs  
- 🏛️ Policymakers — understanding how regional characteristics shape housing markets

---

## 🧰 Technologies and Libraries

- Python 3.x
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`, `xgboost`, `lightgbm`, `shap`
- `folium` and `geopandas` for spatial visualization

---

## 🏘️ Data Overview

We combined **property-level housing data** with:

- Structural features (square footage, number of bedrooms/bathrooms, lot size)
- Geographic context (ZIP code, region)
- External factors:
  - Natural hazard risk (e.g., floods, earthquakes, wildfires)
  - Demographics (e.g., income, population density)
  - Environmental indicators

---

## 🧠 Machine Learning Techniques

### 🔢 Classification Models
We created a binary classification task by labeling homes as **expensive** (top 50%) vs **not expensive** (bottom 50%). Multiple classifiers were tested:

#### ✅ Best Classification Models:
- **Random Forest Classifier**  
  - Accuracy: ~91%  
  - Excellent precision and recall, low misclassification rate.
  
- **Neural Network (MLPClassifier)**  
  - Two hidden layers: (64, 32), `ReLU` activation, `Adam` optimizer.  
  - Accuracy: **91%**, F1-score: **0.91**  
  - Balanced confusion matrix:  
    - True Negatives: 17,484  
    - True Positives: 16,668  

#### Other Classification Techniques:
- **Logistic Regression** with `class_weight='balanced'`
- **PCA for Dimensionality Reduction** (attempted but hurt performance)

---

### 📈 Regression Models

We modeled **actual housing prices** (continuous values) using several regression techniques. Features were standardized, and log transformation was applied to the target in some models.

#### 🥇 Top Performer: **Random Forest Regression**
- **R² Score**: 0.894  
- **MAE**: ~$49,330  
- **MSE**: ~5.15B  
- Great performance on capturing non-linear trends.

#### 🤖 Neural Network (MLPRegressor with SGD)
- Hidden layers: (64, 32), `ReLU`, `SGD` optimizer, early stopping  
- R² Score: 0.869  
- Slightly underperformed RF, but still strong

#### 🔍 Linear Models:
- **Linear Regression**  
  - R² Score: 0.741
- **Ridge Regression**  
  - R² Score: 0.741
- **Lasso Regression**  
  - R² Score: 0.741  
  - All performed similarly, unable to capture complex relationships

---

### 📊 Clustering

We applied **K-Means Clustering** on feature space to uncover latent housing market segments.

- **Optimal K (Elbow Method)**: 5 clusters
- Provides insight into regional price clusters, could be used for market segmentation.

---

## 🧹 Data Preprocessing

- **Outlier Removal**: Interquartile Range (IQR) method  
- **Feature Scaling**: StandardScaler from scikit-learn  
- **Target Transformation**: Log-transform for regression
- **PCA**: Tested but reduced regression performance

---

## ⚠️ Challenges

### 🔍 Data Sourcing
- Real estate data sourced from **Kaggle** (2022), while demographic data came from **public datasets (2020)**
- Free access limited real-time data availability

### ⚖️ Class Imbalance
- Originally, the top 25% house prices were used to define “expensive,” causing imbalance.
- Adjusted to **top 50% vs bottom 50%**, resulting in:
  - Class 0: 19,061 samples
  - Class 1: 18,509 samples  
- Also applied `class_weight="balanced"` in models

---

## 🚀 Future Work

1. **Multi-Class Classification**: Categorize houses into low, mid, high price tiers  
2. **Feature Expansion**: Include school quality, crime rates, proximity to amenities  
3. **Temporal Models**: Time series forecasting using LSTM or ARIMA  
4. **Geo-Aware Modeling**: Incorporate spatial data using geospatial techniques

---

## 👥 Team & Contributions

**Group Project — CS 545 Big Data Analysis Final Project**

- [ypi9] 
- [leyli16] 
- [jamieyuanmin]
- [jyan888] 

---

## 📬 Contact

For questions or collaboration inquiries, feel free to reach out via GitHub or email.

---

## 📄 License

This project is for academic purposes only. For usage or licensing inquiries, please contact the authors.
