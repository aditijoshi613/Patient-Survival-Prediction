# Patient Survival Prediction

## DATA604 Final Project

### Problem Statement
In the healthcare industry, accurately predicting whether a patient is at risk of death during hospitalization is crucial for timely intervention and improved patient care. This study aims to address this challenge by utilizing various representation methods for classification, including raw data, Principal Component Analysis (PCA), Kernel PCA (KPCA), and Autoencoder. The effectiveness of these dimensionality reduction methods will be compared to determine the most reliable approach. The KNN algorithm will be employed for classification purposes.

### Data Description

The Patient Survival Prediction dataset (https://www.kaggle.com/datasets/mitishaagarwal/patient) consists of various factors related to hospitalized patients. There are 91713 data points with 85 features each. The dataset has a binary output variable “hospital_death” representing whether the patient died (1) or not (0).

### Conclusion

After using various data representation methods for transforming the data and conducting several experiments to determine the hyperparameters for those methods as well as for the KNN models, the following conclusions are derived:
1. The time required for conducting hyperparameter tuning experiments reduces after dimensionality reduction.
2. Using raw data to train, validate and test the KNN model gives the best performance metrics because considering all the features in the given dataset helps to capture all the necessary information and hence, evaluate complex relations between features and the outcome to build a complex model.
3. The kernel PCA method gives the worst performance metrics when the transformed data is used to train, validate and test the KNN model. This is because kernel methods are computationally heavy and cannot be used to transform high dimensional data with a number of samples as high as 100000. Due to this reason, only a slice of the dataset is used to evaluate this method and hence, overfitting occurs (i.e., the test f1 score/accuracy is lesser than the training f1 score/accuracy by 10%).
4. The performance of the autoencoder framework can be boosted by adding additional layers and optimizing additional hyperparameters.
Conclusively, using dimensionality reduction techniques can help achieve performance similar to raw data for classification problems while saving the computational overload and hence, the resources and time required for training, validating, and testing classification models.


