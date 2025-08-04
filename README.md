# Interpretable Modeling of Housing Prices Across Regions 🏡📉

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

## 🧠 Methodology

### Part 1: Data Preparation

- Exploratory Data Analysis (EDA)
- Merging multiple datasets (property + risk + demographics)
- Handling missing data, encoding categorical variables
- Feature normalization and spatial alignment

### Part 2: Modeling and Interpretation

- Model comparison:
  - Linear Regression, Ridge, Lasso (interpretable baselines)
  - Tree-based models: Random Forest, XGBoost, LightGBM
- Model evaluation using:
  - MAE, RMSE, R²
- Feature importance and SHAP-based model explainability
- Mapping price predictions and risk profiles geographically

---

## 📊 Results & Insights

- Structural features like **house size**, **bedroom count**, and **lot area** were strong predictors of price.
- External features such as **wildfire risk**, **income levels**, and **population density** added substantial explanatory power.
- SHAP analysis helped uncover how specific factors influence price differently across regions.

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
