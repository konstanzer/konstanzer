# Title

<img src="img/name.png" width="200"/>

---
- [Summary](#introduction)
- [Data](#data)
- [Planning ipeline](#planning-pipeline)
- [Hypotheses](#hypotheses)
- [Results](#results)

## Summary



## Data

| Feature                        | Description                                                                                                            |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------|
| 'X'                            |                                               |
| 'X'                            |                                               |
| 'y'                            | The target variable.                          |

## Planning pipeline

Step 1: Acquire

* If data is in a SQL database, run select * from zillow.2017 via SQL IDE.
* If data is a csv file, use pandas, e.g. pandas.read_csv().

These steps are covered in acquire.py.

Step 3: Prepare Data

* Drop columns
* Impute
* Convert categorical variables using one-hot encoding.
* Drop outliers 
* Split 

These steps are covered in prepare.py.

Step 4: Explore & Preprocess

* Visualize attributes & interactions (Python: seaborn and matplotlib).
* Plot correlation matrix of features.
* Drop multicollinear features

Analyze: statistically and more generally (Python: statsmodels, numpy, scipy, scikit-learn).

Step 5: Model

* Constant (mean of training target error) baseline
* Linear regression

Models used:

* KMeans
* LinearRegression (OLS)
* TweedieRegressor (GLM)

## Hypotheses

* Location (county and/or zip code) is driving log error.
* Finished square feet is driving log error.

## Results

| model | RMSE | R^2
| --- | --- | --- |
| Constant (mean) | .08 | 0 |
| Generalized linear regression | .08 | 0 |
