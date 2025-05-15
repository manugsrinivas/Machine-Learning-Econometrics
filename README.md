This repository contains a series of applied econometric and statistical learning problem sets completed as part of ECON 573. Each notebook uses real-world or simulated datasets to explore predictive modeling, classification, dimensionality reduction, and unsupervised learning techniques using Python. The work extensively utilizes libraries such as `statsmodels`, `scikit-learn`, `ISLP`, and `matplotlib`.

The first notebook, ECON_573_PS1_Applied.ipynb, focuses on logistic regression using the `Default` dataset, which contains information on individuals' income, credit card balance, student status, and whether they defaulted on a loan. A logistic regression model was built to predict default status using income and balance as predictors. The validation set approach was used to evaluate test error, with results showing that increasing the training set size improved performance. The problem set also introduced a student dummy variable to assess its impact on prediction accuracy, but its inclusion did not meaningfully reduce test error. Lastly, the notebook used bootstrapping to estimate standard errors of model coefficients, which were compared to standard GLM-based estimates and found to be quite similar, validating both methods.

In ECON_573_PS2_Applied.ipynb, the focus shifted to polynomial regression, regression splines, and boosting. Using the `Boston` housing dataset, the relationship between nitrogen oxide concentration (nox) and the distance to employment centers (dis) was modeled using cubic polynomials and regression splines. Model complexity was varied, and cross-validation identified the optimal degree of the spline to balance fit and overfitting. In a separate analysis, the `Hitters` dataset was used to predict log-transformed baseball player salaries using boosting. Training and test sets were used to evaluate mean squared error (MSE), and boosting outperformed best subset selection and linear regression. The most important features in the boosted model were also identified, highlighting the interpretability of ensemble methods.

The third notebook, ECON_573_PS3_Applied.ipynb, emphasized model selection and regularization techniques. Simulated data and datasets like `College` and `Hitters` were used to compare best subset selection, forward and backward stepwise regression, ridge regression, and LASSO. Regularization paths and coefficient shrinkage were explored, and LASSO was shown to effectively reduce dimensionality while retaining key predictors. Model performance was assessed using cross-validation, and findings illustrated that LASSO provided better prediction accuracy than traditional selection methods, especially when the number of predictors was large.

ECON_573_PS4_Applied.ipynb introduced tree-based methods, including decision trees, random forests, and boosting. Using the `Carseats` dataset, a regression tree was built to predict sales, with tree pruning applied to avoid overfitting. Random forests and boosting were then implemented, significantly improving predictive accuracy. The `OJ` dataset was used to predict brand purchases in a classification task. Ensemble methods again demonstrated superior accuracy and robustness compared to single-tree models. The notebooks also examined variable importance rankings, highlighting which factors most influenced purchasing decisions.

The final notebook, ECON\_573\_PS5\_Applied.ipynb, focused on unsupervised learning and principal component analysis (PCA). In Part I, a simulated dataset with 60 observations (20 per class) and 50 features was generated, with mean shifts to create three distinct classes. PCA was used to reduce dimensionality, and the first two principal components successfully separated the classes. K-means clustering was then applied for different values of K (2, 3, 4), both on the original and PCA-reduced data. Results showed that clustering on PCA scores improved class separation, and scaling the data further enhanced clustering performance. In Part II, monthly currency exchange rates were translated into returns and analyzed using PCA. The first principal component captured broad USD movement, while the second and third reflected more nuanced currency dynamics. Principal component regression (PCR), LASSO, and partial least squares (PLS) were used to model S&P 500 returns based on currency factors. Findings indicated that PC1 had a positive relationship with S&P 500 returns, and PLS outperformed PCR in predictive power, highlighting the benefits of supervised dimensionality reduction.

Collectively, these problem sets demonstrate a comprehensive application of statistical learning techniques to both simulated and real-world economic data, showcasing how modern modeling tools can enhance prediction, interpretation, and data-driven decision-making.

Libraries Used

Each problem set leveraged a combination of statistical modeling and machine learning libraries to conduct analysis. Below is a breakdown of the important libraries used in each notebook:

PS1: Logistic Regression & Bootstrap

* `pandas`, `numpy` – data manipulation and numerical operations
* `matplotlib.pyplot`, `seaborn` – data visualization
* `math` – basic mathematical operations

PS2: Polynomial Regression, Splines, Boosting

* Same libraries from PS1, plus:
* `statsmodels.api`, `statsmodels.formula.api` – regression models and statistical analysis
* `ISLP` – for loading datasets and polynomial feature transformations
* `statsmodels.stats.anova`, `variance_inflation_factor` – model diagnostics and multicollinearity checking

PS3: Model Selection & Regularization

* Same libraries from PS2, plus:
* `scikit-learn` modules:
  * `Pipeline`, `StandardScaler`, `LinearRegression`, `PCA`, `PLSRegression`
  * `train_test_split`, `mean_squared_error`, `r2_score`, `mean_absolute_error`
* `l0bnb` – best subset regression via branch-and-bound
* `functools.partial`, `itertools`, `time` – utility and performance handling

PS4: Tree-Based Methods

* Same libraries from PS3, plus:
* `KFold`, `PolynomialFeatures` – cross-validation and polynomial feature engineering

PS5: PCA & Clustering

* Same libraries from PS4, plus:
* `random`, `datetime` – for simulation and time management
* `statsmodels.datasets` – dataset access
* `scipy.cluster.hierarchy`, `sklearn.cluster` – hierarchical and k-means clustering
* `ISLP.cluster` – helper functions for clustering analysis
