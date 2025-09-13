# Handwritten-Digits-Recognition-By-KNN


Based on this repository provided, here is a complete explanation of the K-Nearest Neighbors (KNN) classification process for the MNIST handwritten digit dataset.

## Summary
The document demonstrates the use of a K-Nearest Neighbors (KNN) classifier to recognize handwritten digits from the MNIST dataset. It highlights the importance of selecting an appropriate number of neighbors (n_neighbors) to achieve good model accuracy. The initial attempt with a large number of neighbors results in low accuracy, while a subsequent adjustment dramatically improves the model's performance.

## 1. Data Loading and Preparation
The process begins with importing libraries such as pandas, numpy, and matplotlib.pyplot for data handling and visualization, as well as sklearn.datasets to load the MNIST dataset. The dataset contains 1797 handwritten digits. Each image is an 8x8 matrix of pixel values, which is then reshaped into a flattened array of 64 features for the classifier. The corresponding labels for each digit (0-9) are stored in the y variable.

## 2. Initial Model Training and Evaluation (with n_neighbors = 200)
A KNeighborsClassifier is initialized with n_neighbors=200. This initial model is trained on the first 1000 data points. The model's performance is then evaluated on the remaining 797 data points. The classification report and confusion matrix show that the accuracy is only 81%. The document notes that this is a high error rate and attributes it to the large number of neighbors chosen for the model.

## 3. Re-evaluation with an Improved Parameter (n_neighbors = 3)
To improve the accuracy, a new KNN classifier is created with a smaller n_neighbors value of 3 and weights='distance'. This new model is trained on the same initial 1000 data points and evaluated on the same remaining 797 data points. This change results in a significant improvement, raising the model's accuracy to 96%. The new classification report and confusion matrix confirm this much better performance.

## Conclusion
The document demonstrates a critical concept in machine learning: hyperparameter tuning. It shows that the choice of the n_neighbors parameter is crucial for the performance of a KNN classifier. By starting with a poorly chosen value and then correcting it, the document provides a clear example of how model accuracy can be drastically improved by adjusting key parameters. The final model achieves a very high accuracy of 96% in classifying handwritten digits.
