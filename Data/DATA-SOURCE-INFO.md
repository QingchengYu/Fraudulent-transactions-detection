# Applied Machine Learning Project Deliverable 3
## Fraudulent Transaction Detection

The data sources used for this project is the IEEE-CIS Fraud Detection Dataset on Kaggle

|        Filename       |                                                      Description                                                     |
|:---------------------:|:--------------------------------------------------------------------------------------------------------------------:|
| train_transaction.csv | Part of the training set. A CSV file with transaction information and whether or not the transaction was fraudulent. |
| train_identity.csv    | Part of the training set. A CSV file with identity information.                                                      |
| sample_submission.csv | (Contest specific; not used) Submission format for the actual contest                                                |

We join the train_transaction.csv and train_identity.csv datasets in pandas and use a 80%-20% develpment set to test set split for our project.

### Data Source

* The IEEE-CIS Fraud Detection dataset is provided by Vesta Corporation from Kaggle, those data come from Vesta's real-world e-commerce transactions.
* The dataset is divided into two parts: identity and transaction. These two types of data are joined by the unique feature 'TransactionID', which represents a unique timedelta from a given reference datetime.
* The identity data contains features about identification information, network connection information, and digital signatures associated with transactions. 
* The transaction data contains features about money transfers and other consumption services, providing information about the purchase of goods, as well as information about the seller.
* The dataset contains a total of 871 columns.
* Due to security and privacy concerns, all features are masked and represented by numerical IDs, except for device types and device systems.




### Plan

* Exploratory Data Analysis (EDA): Analyze the preprocessed dataset to identify trends, patterns, and correlations that may be useful in building the model.
* Model Selection: Experiment with various machine learning algorithms, such as logistic regression, random forests, gradient boosting machines and neural network, to identify the most suitable model for the problem.
* Model Training: Train the selected model using the preprocessed dataset, applying techniques like cross-validation and hyperparameter tuning to optimize its performance.
* Model Evaluation: Assess the performance of the trained model using appropriate evaluation metrics, such as precision, recall, F1 score, and AUC-ROC curve.

### Data Preprocessing

* Check the missing value rate for each of the features in the dataset, and drop the features with higher than 70% missing data which not provide enough information
* Separated these categorical variables and numerical variables from the dataset, filled in numerical values with median values
* Drop highly correlated (> 0.9) features to reduce redundant information for model training
* Split the dataset into a development set and a test set in the ratio of 4:1 by using stratified splitting (because the dataset is imbalanced).
* Implemented StandardScaler for numerical features, one-hot encoding for categorical features, and target encoding for high cardinality categorical features. 
* Resampling development dataset by using SMOTE to create a balanced dataset that classes have the same size of samples.
