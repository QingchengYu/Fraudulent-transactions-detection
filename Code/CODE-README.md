# Code

The following table maps each ML technique used for this project to its filename in this folder:

|        ML Technique        |                            Filename                            |
|:--------------------------:|:--------------------------------------------------------------:|
| Logistic Regression        | 1_logistic_regression_hist_gradient_boosting.ipynb             |
| Decision Trees             | 2_decision_tree.ipynb                                          |
| Random Forest              | 3_random_forest_cuda.ipynb                                     |
| Hist Gradient Boosting     | 1_logistic_regression_hist_gradient_boosting.ipynb             |
| XGBoost                    | 4_XG_boost.ipynb                                               |
| Feedforward Neural Network | 5_neural_network.ipynb                                         |

The following experiments were done in this project:

## Logistic Regression:

It is a linear model that utilizes the logistic function, which maps input features to a probability value between 0 and 1. This value is then used to predict the class of the input by setting a threshold, commonly at 0.5.

## Decision Tree:

Decision trees are another popular supervised learning algorithm that can be applied to our classification problem here. Decision trees work by recursively splitting the input data on the most informative features, and create a tree-like structure of decision rules that can be used for prediction. 

## Random Forest:

The Random Forest consists of several decision trees, each of which is constructed on a group of randomly sampled training data. Each decision tree corresponds to a random sample, and the random feature subset is used for training, which can reduce the variance of the model and improve the generalization ability.

## Hist Gradient Boosting:

Histogram-based Gradient Boosting is an ensemble learning technique that combines multiple weak learners, typically decision trees, to form a strong learner. The model is built in a stage-wise manner, with each new tree being added to the ensemble to correct the errors made by the previous trees. The input features are binned into histograms, which accelerates the training process by reducing the number of possible splitting points for each feature.

## XGBoost

XGBoost (or Extreme Gradient Boosting) is one of the most popular gradient boosting techiniques. In our project, the hyperparameters for XGBoost tuning are the number of estimators, learning rate, regularization parameters, maximum depth, and maximum leaf nodes.

## Feedforward Neural Network

Feedforward neural networks are a class of artificial neural networks where the information flows in a unidirectional fashion form the input layer to the output layer. Each layer is a linear projection of the input features followed by an activation function that adds non-linearity. 
