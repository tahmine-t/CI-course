# Feature Selection - Phase 2

This project involves implementing feature selection techniques for an image classification task using the SYN Digits dataset. The goal is to classify images using a Multi-Layer Perceptron (MLP) and a Support Vector Machine (SVM), with an emphasis on improving the model's accuracy and performance through feature selection and hyperparameter tuning.

<p align="center">
  <img src="images/imge10.png" alt="feature_selection" width="400">
</p>

## Overview

The project consists of two main parts:
1. **SVM Classification**: Evaluating and fine-tuning Support Vector Machines with different kernels and hyperparameters to improve classification accuracy.
2. **Neural Network and Feature Selection**: Using an MLP for feature selection and refining the model by reducing the input feature space based on the most important features.

## Data

The SYN dataset, also known as the **SYN Digits Dataset**, is a well-known dataset consisting of images of handwritten digits. This dataset is widely used in the machine learning and computer vision communities for tasks such as digit recognition and classification.

<p align="center">
  <img src="images/imge4.png" alt="SYN_Dataset" width="400">
</p>

**Dataset Details:**

- **Source:** The SYN Digits Dataset is commonly used as a benchmark dataset for various machine learning and computer vision projects. The dataset contains a collection of images of handwritten digits, which are often used for tasks like digit recognition, classification, and image processing.

- **Contents:** The dataset includes a substantial number of grayscale images, each depicting a handwritten digit from 0 to 9. These images serve as the primary data for your feature selection and classification tasks in this project.

- **Format:** Images in the SYN dataset are typically stored as pixel values in a matrix format, making them suitable for training and testing machine learning models.

The SYN dataset is a popular choice for practicing feature selection, image classification, and other machine learning tasks.

## Metrics Used for Evaluation

The classification performance is evaluated using the following metrics:
1. **Confusion Matrix**: Helps identify true positives, false positives, true negatives, and false negatives for each class.
2. **Precision**: Measures how many of the predicted positive values were actually correct.
3. **Recall**: Measures how many of the actual positive values were correctly predicted.
4. **F1 Score**: The harmonic mean of precision and recall, balancing both metrics to assess overall classification performance.

## SVM Classification

Three different SVM kernel functions were evaluated:
1. **Linear Kernel**: Suitable when classes are linearly separable.
2. **RBF Kernel**: Best suited for non-linear decision boundaries, which performed the best in this dataset with an accuracy of **0.90**.
3. **Polynomial Kernel**: Useful for data with polynomial decision boundaries, yielding an accuracy of **0.87**.

The RBF kernel with a **C value of 10** was found to give the best performance, providing an accuracy of **0.90** on the test set.

### Hyperparameter Tuning with C Parameter

The **C** parameter of the SVM was varied to examine its effect on model accuracy:
- **C = 10**: Best performance with 0.90 accuracy.
- **C = 1**: Slightly worse performance with 0.89 accuracy.
- **C = 0.1**: Significantly reduced performance with 0.72 accuracy.
- **C = 0.01**: Poor performance with 0.17 accuracy.

The results indicate that **C = 10** provides the best trade-off between model flexibility and performance.

### Regularization in Neural Networks

**L1 Regularization** was applied to the MLP to prevent overfitting by penalizing weights that are close to zero:
- The L1 regularization penalty is computed as `loss = l1 * sum(abs(weights))`.
- A series of experiments were conducted with different regularization parameters (`reg_l1_param`) to determine the optimal configuration.

**Best Configuration**:
- **Hidden Layer Size**: 100
- **L1 Regularization**: 0.001
- **Test Accuracy**: 0.88

## Feature Selection Process

The feature selection process involved training the model on all features and selecting the most important ones based on the absolute sum of weights in the first layer of the MLP. The process was repeated iteratively to find the top 150 features.

- The top 10 features provided an accuracy of **0.3764** with a score of **0.3689**.
- With increasing features, the accuracy improved and stabilized at **0.70** for the top 110 features.

The final model achieved the best score of **0.70** with **110 features**.

### Training the Model

1. **SVM**: Train the SVM with different kernels and hyperparameters.
2. **MLP**: Use the MLP to train with different regularization parameters and perform feature selection.
3. **Feature Selection**: Perform feature selection to determine the most important features and improve the classifier.

### Evaluation

Evaluate the classifier's performance using the confusion matrix, precision, recall, F1 score, and accuracy metrics.

## Results

The project includes various results, including:
- **Accuracy scores** for different configurations (SVM, MLP).
- **Confusion matrices** for SVM performance.
- **Feature selection results**, showing how accuracy improves as more features are selected.
