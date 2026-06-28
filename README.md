# Iris_Flower_Classification
Use the Iris dataset to develop a model that can classify iris flowers into different species based on their sepal and petal measurements. 

**Model Performance Analysis**

Four machine learning algorithms were trained and evaluated on the Iris dataset:
| Model                           | Training Accuracy | Testing Accuracy | Remarks                                                       |
| ------------------------------- | ----------------: | ---------------: | ------------------------------------------------------------- |
| Logistic Regression             |        **97.14%** |       **97.78%** | Excellent generalization with balanced performance            |
| Support Vector Classifier (SVC) |            97.14% |           95.56% | Good performance but slightly lower test accuracy             |
| K-Nearest Neighbors (KNN)       |            96.19% |       **97.78%** | Strong testing accuracy with slightly lower training accuracy |
| Decision Tree (Default)         |       **100.00%** |       **97.78%** | Perfect training accuracy indicates overfitting               |
| Decision Tree (Tuned)           |            97.14% |           95.56% | Reduced overfitting but lower testing accuracy                |

**Detailed Analysis**
1. Logistic Regression
Training Accuracy: 97.14%
Testing Accuracy: 97.78%

Advantages
Very small difference between training and testing accuracy.
High precision, recall, and F1-score across all classes.
No signs of overfitting.
Simple, fast, and computationally efficient.

2. Support Vector Classifier (SVC)
Training Accuracy: 97.14%
Testing Accuracy: 95.56%

Analysis
Performs well on the dataset.
Slightly lower testing accuracy than Logistic Regression and KNN.
Good generalization but not the best-performing model.

3. K-Nearest Neighbors (KNN)
Training Accuracy: 96.19%
Testing Accuracy: 97.78%

Analysis
Achieved the same testing accuracy as Logistic Regression.
Lower training accuracy indicates the model is less likely to overfit.
Performance depends on the choice of K (n_neighbors=7).

4. Decision Tree (Default)
Training Accuracy: 100%
Testing Accuracy: 97.78%

Analysis

Although the testing accuracy is high, the model perfectly classifies the training data.

This indicates that the model has memorized the training dataset instead of learning generalized patterns.

Signs of overfitting:

100% training accuracy
Complex tree
Poor generalization on unseen data compared with simpler models

5. Tuned Decision Tree

Parameters used:

criterion='entropy'
max_depth=3
min_samples_split=15

Results:

Training Accuracy: 97.14%
Testing Accuracy: 95.56%
Analysis
Hyperparameter tuning successfully reduced overfitting.
The gap between training and testing accuracy became smaller.
However, testing accuracy decreased compared to the default Decision Tree.

**Best Model Selection**

Although Logistic Regression, KNN, and the default Decision Tree all achieved a testing accuracy of 97.78%, the Logistic Regression model is the best choice for this project.

| Model                   | Train Accuracy | Test Accuracy | Overfitting | Final Verdict    |
| ----------------------- | -------------: | ------------: | ----------- | ---------------- |
| Logistic Regression     |         97.14% |    **97.78%** | No          | ⭐ **Best Model** |
| KNN                     |         96.19% |    **97.78%** | No          | Very Good        |
| SVC                     |         97.14% |        95.56% | No          | Good             |
| Decision Tree (Default) |           100% |        97.78% | Yes         | Overfitted       |
| Decision Tree (Tuned)   |         97.14% |        95.56% | Reduced     | Acceptable       |

