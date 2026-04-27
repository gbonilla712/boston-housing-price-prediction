# Boston House Price Prediction Elective Project

## 📋 Project Overview

This project builds an **OLS multiple linear regression model** to predict median home values across Boston suburbs and towns using the Boston Housing dataset (506 observations, 13 variables) collected in 1970 from the Boston Standard Metropolitan Statistical Area (SMSA). The analysis applies exploratory data analysis, feature engineering, and multicollinearity diagnostics to deliver a statistically robust, interpretable model that explains approximately **70%** of the variation in housing prices. This elective project was completed as part of the **MIT Applied AI & Data Science Program**. 

## 🎯 Key Objectives

- Identify the key socioeconomic and spatial factors that drive housing prices in Boston suburbs and towns
- Build a reliable OLS multiple linear regression model with validated assumptions
- Deliver actionable, data-driven insights for real estate stakeholders, including home buyers, property investors, and housebuilders

## 📊 Highlights & Findings

- **Seven statistically significant predictors** retained in the final model: CRIM, CHAS, NOX, RM, DIS, PTRATIO, and LSTAT
- **RM (rooms per dwelling)** and **LSTAT (lower-status population %)** showed the strongest linear relationships with home values (Pearson r = 0.70 and −0.74, respectively)
- **Log transformation** of the target variable (MEDV) improved residual normality and stabilized variance
- **Iterative VIF analysis** removed RAD_24 (VIF = 15.63) and TAX (VIF = 6.06), ensuring all remaining features had VIF < 5
- **All four OLS assumptions verified:** residual mean ≈ 0, homoscedasticity confirmed (Goldfeld-Quandt p = 0.279), linearity satisfied, and normality confirmed via Q-Q plot and histogram
- **10-fold cross-validation** confirmed model stability with R² = 0.729 (±0.239) and MSE = 0.040 (±0.023)
- **No overfitting detected** — training and test RMSE, MAE, and MAPE remain small and stable

## 💡 Recommendations

1. **Housing Quality:** Prioritize renovations and construction of larger, multi-room homes to increase property values
2. **Environmental Initiatives:** Target high-NOX neighborhoods with pollution-reduction measures such as eco-friendly buffers and traffic rerouting
3. **Transit Connectivity:** Enhance public transit access to employment centers for suburban and distant neighborhoods
4. **Education Investment:** Lower pupil-teacher ratios in underperforming schools to positively impact surrounding home values
5. **Community Programs:** Support socioeconomic uplift initiatives to reduce LSTAT concentrations across neighborhoods
6. **Public Safety:** Implement crime-reduction strategies, including hotspot identification, improved street lighting, and community safety programs
7. **Waterfront Development:** Construct recreational areas near bodies of water to leverage the Charles River adjacency premium

## 📁 Project Structure
```plaintext
boston-house-price-prediction/
│
├── GBonilla Boston House Price Prediction Elective Methodology and Workflow.pdf   # Detailed methodology + workflow document
├── GBonilla Boston House Price Prediction Elective Low Code Report.pdf     # Full project report
├── GBonilla_Boston_House_Price_Prediction_Elective_Low_Code.ipynb   # Solution deliverable
│
└── README.md                                # Project overview and documentation
```

## 🛠️ Tools & Technologies

- **Language:** Python
- **Libraries:** NumPy, Pandas, Matplotlib, Seaborn, Statsmodels, Scikit-learn
- **Modeling:** OLS Multiple Linear Regression (Statsmodels)
- **Diagnostics:** Variance Inflation Factor (VIF), Goldfeld-Quandt Test, Q-Q Plot, 10-Fold Cross-Validation
- **Environment:** Google Colab Notebook

## 📑 Project Report

The full project report (`GBonilla Boston House Price Prediction Elective Low Code Report.pdf`) covers the following sections:

1. **Executive Summary** — Dataset overview, modeling approach, key findings, and stakeholder applications
2. **Business Problem Overview and Solution Approach** — Problem framing, stakeholder needs, and end-to-end methodology
3. **Data Overview** — Variable definitions, data types, quality assessment, and descriptive statistics
4. **Exploratory Data Analysis (EDA)** — Univariate distributions, bivariate correlations, and scatterplot analysis
5. **Data Preprocessing** — Outlier retention, log transformation, one-hot encoding, and VIF-based feature selection
6. **Linear Regression Analysis and its Assumptions** — Model comparison (model1 vs. model2), coefficient interpretation, and four-assumption verification
7. **Conclusions and Recommendations** — Actionable insights, strategic proposals, and key takeaways
8. **Appendix** — Supporting code snippets
