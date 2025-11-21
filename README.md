# ECON 573 – Applied Problem Sets

This repository contains applied exercises from **ECON 573 (Machine Learning Econometrics)**. Each problem set involves multiple datasets and statistical learning techniques, moving from exploratory analysis to regression/classification, resampling, and finally unsupervised learning with applications in finance.

---

## **Problem Set 1 – Exploratory Analysis & Introductory Modeling**
- **Datasets**:  
  - `College.csv`  
  - `Auto`  
  - `Boston`  
  - `BenAndJerry.csv`
- **Problems & Models**:
  - *College*: Exploratory data analysis with summary statistics, scatterplots, and boxplots. Created “Elite” indicator variable; analyzed tuition and room/board differences between public vs. private and elite vs. non-elite institutions.  
  - *Auto*: Basic regression setup, exploring linear relationships between horsepower and mpg.  
  - *Boston*: Examined housing data for predictors of median home value; introductory multiple regression analysis.  
  - *Ben & Jerry’s*: Business-oriented exploratory data analysis on ice cream sales, investigating demand variation across stores.  
- **Techniques**: EDA, feature engineering, summary statistics, simple linear regression, group comparison.

---

## **Problem Set 2 – Regression & Model Assessment**
- **Datasets**:  
  - `Auto`  
  - Simulated dataset (`x ~ N(0,1)`, generated response `y`)  
  - `Boston`  
  - `/homes2004`
- **Problems & Models**:
  - *Auto*: Linear regression of `mpg ~ horsepower`, confidence intervals, prediction intervals, and regression diagnostics.  
  - *Simulated dataset*: Studied correlation and regression properties of generated data; visualized regression line behavior under noise.  
  - *Boston*: Multiple regression to identify key housing predictors; hypothesis testing on the significance of variables like crime rate, rooms per dwelling.  
  - *Homes2004*: Applied regression models to predict housing prices; discussed overfitting vs generalization.  
- **Techniques**: OLS regression, confidence intervals, simulated regression, multiple regression model building, inference on coefficients.

---

## **Problem Set 3 – Model Complexity & Regularization**
- **Datasets**:  
  - Simulated regression dataset (20 features, 1000 obs.)  
  - `Boston`  
  - `Weekly`
- **Problems & Models**:
  - *Simulated data*: Bias–variance tradeoff analysis; fitted increasingly complex linear models and evaluated training vs. test error.  
  - Applied **PCR (Principal Component Regression)**, **PLS (Partial Least Squares)**, **stepwise selection**, and **L0-regularization** to reduce dimensionality and avoid overfitting.  
  - *Boston*: Applied regression and selection methods to predict housing prices.  
  - *Weekly*: Modeled stock market returns with **logistic regression** and **classification models** (train/test split).  
- **Techniques**: Simulation-based validation, regularization (PCR, PLS, L0), logistic regression for classification, stock market return prediction.

---

## **Problem Set 4 – Classification & Resampling**
- **Datasets**:  
  - `Default`  
  - `Boston`  
  - `Hitters`
- **Problems & Models**:
  - *Default*: Logistic regression predicting probability of default from income and balance; validation set approach and K-fold cross-validation for test error estimation.  
  - *Boston*: Applied regression with cross-validation to evaluate predictive accuracy; compared different resampling strategies.  
  - *Hitters*: Explored **best subset selection**, **ridge regression**, **lasso regression**, and **cross-validation** to predict baseball salaries.  
- **Techniques**: Logistic regression, classification, resampling (validation set, K-fold CV), subset selection, shrinkage methods.

---

## **Problem Set 5 – PCA, Clustering & Financial Applications**
- **Datasets**:  
  - Simulated dataset (3 classes, 50 variables)  
  - `FXmonthly.csv`  
  - `sp500.csv`
- **Problems & Models**:
  - *Simulated data*: Applied **PCA** for dimensionality reduction; **K-Means clustering** and **hierarchical clustering**; compared cluster labels with true classes; tested different values of K.  
  - *FXmonthly*: Conducted correlation analysis of foreign exchange returns; applied PCA to extract latent factors.  
  - *sp500*: Regressed S&P 500 returns onto currency PCA factors using **GLM** and **Lasso**; compared with **PLS** regression.  
- **Findings**: PCA revealed strong correlations in FX data, with first PCs capturing USD-driven variation; SP500 returns positively associated with USD strength (PC1) but negatively influenced by specific currency movements (PC2).  
- **Techniques**: PCA, clustering (K-Means, hierarchical), regression on PCs, Lasso vs PCA vs PLS comparison.

---

👉 Across all five problem sets, the notebooks demonstrate progression from **basic regression & exploratory data analysis** → **resampling & model validation** → **regularization & classification** → **unsupervised learning and financial applications**.  

