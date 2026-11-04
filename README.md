# Machine Learning Classification and Ensemble Learning

A comparative study of machine learning classification algorithms and ensemble learning methods using synthetically generated datasets.

## Project Overview

This project focuses on exploring and comparing different machine learning classification algorithms using synthetic datasets with varying geometric structures and class distributions.

The main objective is to understand how different classifiers behave under different classification conditions, analyze their decision boundaries, and investigate how hyperparameter tuning affects model performance and generalization.

The project covers the complete machine learning workflow, including synthetic data generation, exploratory data analysis, preprocessing, model training, hyperparameter experimentation, performance evaluation, and decision boundary visualization.

## Objectives

- Generate synthetic binary classification datasets using Scikit-learn.
- Explore different data distributions and classification structures.
- Implement and compare multiple machine learning classification algorithms.
- Visualize decision boundaries to understand model behavior.
- Investigate the effects of different hyperparameter values on model performance.
- Compare individual classifiers with ensemble learning methods.
- Evaluate training and test accuracy to assess model generalization.
- Analyze the relationship between model complexity and overfitting.

## Datasets

Three synthetic datasets are generated using Scikit-learn to evaluate classifier performance under different conditions.

| Dataset | Description |
|---|---|
| **Moon Dataset** | Non-linear, crescent-shaped class distributions. |
| **Circle Dataset** | Non-linear, concentric circular class distributions. |
| **Classification Dataset** | A synthetic binary classification dataset with numerical features and a different class distribution. |

The datasets are generated using the following Scikit-learn functions:

- `make_moons()`
- `make_circles()`
- `make_classification()`

## Algorithms

Four classification algorithms are implemented and compared:

- **Support Vector Machine (SVM):** Finds decision boundaries that maximize the margin between classes.
- **K-Nearest Neighbors (KNN):** Classifies samples based on the labels of their nearest neighbors.
- **Decision Tree:** Learns classification rules through a tree-based structure.
- **Random Forest:** Combines multiple decision trees to improve prediction stability and generalization.

## Hyperparameter Analysis

An important part of this project is investigating how different hyperparameter values influence classification performance and model behavior.

By experimenting with different parameter configurations, the project examines their effects on decision boundaries, training accuracy, test accuracy, model complexity, and generalization capability.

The main hyperparameters investigated include:

| Algorithm | Hyperparameter | Description |
|---|---|---|
| SVM | `C` | Controls the trade-off between classification errors and margin size. |
| SVM | `gamma` | Determines the influence of individual training samples when using an RBF kernel. |
| KNN | `n_neighbors` | Determines the number of nearest neighbors used for classification. |
| Decision Tree | `max_depth` | Controls the maximum depth and complexity of the tree. |
| Random Forest | `n_estimators` | Determines the number of decision trees in the ensemble. |
| Random Forest | `max_depth` | Controls the maximum depth of each individual tree. |

### Observations on Hyperparameter Changes

- **SVM:** Increasing `C` can make the model more sensitive to training errors, while higher `gamma` values can produce more complex decision boundaries. These configurations may increase the risk of overfitting.
- **KNN:** Increasing `n_neighbors` generally produces smoother decision boundaries and reduces sensitivity to individual data points. However, excessively high values may cause underfitting, while smaller values may make the model more sensitive to noise.
- **Decision Tree:** Increasing `max_depth` allows the model to learn more complex patterns. However, deeper trees may fit the training data too closely, resulting in high training accuracy but lower test accuracy, which indicates overfitting.
- **Random Forest:** Increasing `max_depth` may increase the complexity of individual trees and the risk of overfitting. However, combining multiple trees can reduce variance compared with a single Decision Tree. Increasing `n_estimators` can improve prediction stability, although it also increases computational cost.

These experiments highlight the importance of selecting appropriate hyperparameters to achieve a balance between model complexity and generalization.

## Data Preprocessing

The following preprocessing steps are applied:

- **Train-Test Split:** The datasets are divided into 60% training data and 40% testing data.
- **Feature Scaling:** `RobustScaler` is used to scale numerical features.
- **Data Leakage Prevention:** The scaler is fitted only on the training data and then applied to the test data.

## Model Training and Evaluation

Each classifier is trained using the same training dataset to ensure a fair comparison.

Model performance is evaluated using the following criteria:

- **Training Accuracy:** Measures classification performance on the training data.
- **Test Accuracy:** Measures classification performance on unseen test data.
- **Decision Boundary Visualization:** Helps analyze how different algorithms separate classes and learn classification patterns.
- **Generalization Analysis:** Compares training and test performance to identify potential overfitting.

## Experimental Results and Analysis

The experiments compare SVM, KNN, Decision Tree, and Random Forest across three synthetic datasets with different geometric structures and class distributions.

The analysis focuses not only on classification accuracy but also on how different algorithms respond to changes in hyperparameter configurations.

Decision boundary visualizations provide additional insight into how each classifier learns patterns from the data. Comparing training and test accuracy helps identify differences in model complexity, potential overfitting, and generalization capability.

Overall, the experiments demonstrate that model performance depends not only on the selected algorithm but also on its hyperparameter configuration and the underlying structure of the dataset.

## Technologies

- Python
- Scikit-learn
- NumPy
- Pandas
- Matplotlib
- Seaborn

## Key Takeaways

Through this project, practical experience is gained in:

- Implementing and comparing different machine learning classification algorithms.
- Working with synthetic datasets and non-linear classification problems.
- Understanding the effects of hyperparameter selection on model performance.
- Visualizing and interpreting decision boundaries.
- Evaluating model performance using training and test accuracy.
- Identifying potential overfitting and analyzing generalization.
- Understanding the differences between individual classifiers and ensemble learning methods.
