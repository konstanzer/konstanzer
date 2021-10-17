# Project Summaries

* **Beating the bookie by using aggregate odds**
  * **Repo**: online-sports-betting
  * **Data**: Soccer matches with bookmakers' odds
  * **Purpose**:
  * **Tools**: Selenium, scipy
  * **Description of pipeline**:
  * **Explanation of model**:

* **Exploring Zillow's mispriced estimates with k-means clustering**
  * **Repo**: zillow-logerror-clustering
  * **Data**: Zillow Zestimate's errors with property features
  * **Purpose**:
  * **Tools**: sklearn.cluster
  * **Description of pipeline**:
  * **Explanation of model**:

* **Predicting sale prices of single-unt properties**
  * **Repo**: zillow-prices-linear-modeling-flask
  * **Data**: Home prices with property features
  * **Purpose**:
  * **Tools**: Flask, sklearn.linear_model
  * **Description of pipeline**:
  * **Explanation of model**:

* **Should I stay or should I go?: Predicting telecom customer churn**
  * **Repo**: telco-churn-classification
  * **Data**: 
  * **Purpose**:
  * **Tools**: eli5, sklearn.ensemble, sklearn.logistic_classifier
  * **Description of pipeline**:
    * *Acquire*: Use pd.read_sql and a query to acquire data from MySQL database.
    * *Prepare*: Convert features to numeric and split. SMOTE oversample training data. Oversampling boosts minority class predictions at the cost of total accuracy.
    * *Explore*: Bar plots comparing churning and staying customers easily identified good fatures: fiber optic usage and tenure.
    * *Model*: kNN, tree, forest, naive Bayes, and logistic regression were similar in performance after tuning
    * *Evaluate*: McNemar’s test showed equivalency of models’ predictions. Decision tree wins for simplicity. Significantly improved recall (classification of churn class) over baseline.
  * **Explanation of model**: Gini impurity is a measure of how often an element from the set would be incorrectly labeled if it was randomly labeled according to the distribution of labels in the subset. It can be computed by summing the probability p of an item with label i being chosen times the probability 1 − p of a mistake in categorizing that item. It reaches its minimum (zero) when all cases in the node fall into a single target category. The decision tree finds the feature and value split across all features that maximized Gini impurity at each split. This produces a grossly overfit tree, hence the need for cost complexity pruning. This is represented by a hyperparameter alpha, which I set after fitting many models and maximizing for F1. All nodes with a Gini impurity below the effective alpha are pruned resulting in a much smaller tree that generalizes much better to new, unseen data.

* **Intro to BERT**
  * **Repo**: intro-to-bert-model
  * **Data**:
  * **Purpose**:
  * **Tools**: HuggingFace transformers
  * **Description of pipeline**:
  * **Explanation of model**:

* **An NLP analysis of Maria Popova's blog, BrainPickings.org**
  * **Repo**: brainpickings-nlp
  * **Data**:
  * **Purpose**:
  * **Tools**: sklearn
  * **Description of pipeline**:
  * **Explanation of model**:

* **Ace vs. Ace: An analysis of Gerrit Cole & Jacob deGrom's 2020 Statcast data**
  * **Repo**: ace-versus-ace
  * **Purpose**:
  * **Tools**: seaborn
  * **Description of pipeline**:
  * **Explanation of model**:
