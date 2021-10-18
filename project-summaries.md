# Project Summaries

* **Beating the bookie by using aggregate odds**
  * **Repo**: online-sports-betting
  * **Data**: Soccer matches with bookmakers' odds
  * **Purpose**: Test a betting strategy using aggregated odds. Deploy model using live data.
  * **Tools**: selenium, scipy, pandas, numpy, seaborn
  * **Description of pipeline**:
    * *Acquire & Prepare*: Download soccer odds data from Kaggle.
    * *Explore*: Establish strong linear relationship between real-time aggregated odds and actual event probability.
    * *Model*: Establish which mean odds would have met betting criteria and calculate historical bet results.
    * *Evaluate*: Betting on undervalued odds significantly outprforms a random strategy using only prior probabilities of outcome on the basis of both bet percentage won and cumulative gains.
  * **Explanation of model**: Bookmakers make huge investments in pricing their odds as accurately as possible. The bettor will not be able to beat such models long-term in head-to-head competition but he can benefit from comparing the bookmakers' odds to each other. When a bookmaker is pricing odds significantly above its peers, it signal undervalued odds.

* **Exploring Zillow's mispriced estimates with k-means clustering**
  * **Repo**: zillow-logerror-clustering
  * **Data**: Zillow Zestimate's errors (target var.) with property features
  * **Purpose**: Help Zillow improve its estimates on home selling prices.
  * **Tools**: sklearn.cluster
  * **Description of pipeline**:
    * *Acquire*: Use pd.read_sql and a query to acquire data from SQL database.
    * *Prepare*: Split and scale. Eliminate many multicollinear features.
    * *Explore*: Determine which, if any, features are correlated with log errors. All correlations were under .05.
    * *Model*: Linear regression and feature engineered with clustering.
    * *Evaluate*: The final linear model does not outperform a mean error prediction.
  * * **Explanation of model**: Clustering property features using a spatial distances and clusters optimized with the elbow method (k-means) in order to estblish predictors of log error was a failure.

* **Predicting sale prices of single-unit properties**
  * **Repo**: zillow-prices-linear-modeling-flask
  * **Data**: Home prices (target var.) with location & specific property features
  * **Purpose**: Predict a home's selling price to assist prospective buyers & sellers.
  * **Tools**: Flask, sklearn.linear_model
  * **Description of pipeline**:
    * *Acquire*: Use pd.read_sql and a query to acquire data from SQL database.
    * *Prepare*: Split and scale. Eliminate many multicollinear features.
    * *Explore*: Determine which features are correlated with home prices.
    * *Model*: Linear regression and feature engineered with clustering.
    * *Evaluate*: The final linear model outperform a mean home value prediction.
  * **Explanation of model**: LassoLARS performs automatic regularization. Feature weights are suppressed, thereby helping the model to generalize to new data better.

* **Should I stay or should I go?: Predicting telecom customer churn**
  * **Repo**: telco-churn-classification
  * **Data**: Binary churn label (target var.) with basic & behavioral customer data
  * **Purpose**: Identify customers most like;y to churn.
  * **Tools**: eli5, sklearn.ensemble, sklearn.logistic_classifier
  * **Description of pipeline**:
    * *Acquire*: Use pd.read_sql and a query to acquire data from SQL database.
    * *Prepare*: Convert features to numeric and split. SMOTE oversample training data. Oversampling boosts minority class predictions at the cost of total accuracy.
    * *Explore*: Bar plots comparing churning and staying customers easily identified good fatures: fiber optic usage and tenure.
    * *Model*: kNN, tree, forest, naive Bayes, and logistic regression were similar in performance after tuning
    * *Evaluate*: McNemar’s test showed equivalency of models’ predictions. Decision tree wins for simplicity. Significantly improved recall (classification of churn class) over baseline.
  * **Explanation of model**: Gini impurity is a measure of how often an element from the set would be incorrectly labeled if it was randomly labeled according to the distribution of labels in the subset. It can be computed by summing the probability p of an item with label i being chosen times the probability 1 − p of a mistake in categorizing that item. It reaches its minimum (zero) when all cases in the node fall into a single target category. The decision tree finds the feature and value split across all features that maximized Gini impurity at each split. This produces a grossly overfit tree, hence the need for cost complexity pruning. This is represented by a hyperparameter alpha, which I set after fitting many models and maximizing for F1. All nodes with a Gini impurity below the effective alpha are pruned resulting in a much smaller tree that generalizes much better to new, unseen data.

* **Intro to BERT**
  * **Repo**: intro-to-bert-model
  * **Data**: Binary sentiment label (target var.) with IMDb users' movie reviews
  * **Purpose**: Learn how to use Google's massive SOTA language model for ordinary NLP tasks.
  * **Tools**: HuggingFace transformers
  * **Description of pipeline**:
  * **Explanation of model**: Fine-tuned BERT

* **An NLP analysis of Maria Popova's blog, BrainPickings.org**
  * **Repo**: brainpickings-nlp
  * **Data**: Blog posts, tags, and date written (target var.)
  * **Purpose**: Establish early and late themes in Popova's blog.
  * **Tools**: sklearn.feature_extraction, seaborn
  * **Description of pipeline**: pass
  * **Explanation of model**: Logistic regression classifier

* **Ace vs. Ace: An analysis of Gerrit Cole & Jacob deGrom's 2020 Statcast data**
  * **Repo**: ace-versus-ace
  * **Purpose**: Visaulize data and test hypotheses concerning the two pitchers' relative performances.
  * **Tools**: scipy, seaborn
  * **Description of pipeline**: pass
