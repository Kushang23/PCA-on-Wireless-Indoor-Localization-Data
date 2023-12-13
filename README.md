Dataset:
The dataset used for this project is “Wireless Indoor Localization Data”, which is sourced at UCI ML (https://archive.ics.uci.edu/ml/datasets/Wireless+Indoor+Localization#). The data set is gathered by observing the WiFi signal strengths in an indoor location. It is collected by observing the strengths visible on a smart phone. The dataset contains in total 7 attributes and a single target variable. Each attribute is WiFi signal strength observed on a smartphone. The target value is one of the four rooms. The room is predicted based on the 7 signal strengths.
In total there are 2000 data points. 1500 will be used to train and 500 will be tested.
Data Set Characteristics:
Multivariate Number of Instances:
2000 Area:
Computer Attribute Characteristics:
Real Number of Attributes:
7 Date Donated
2017-12-04 Associated Tasks:
Classification Missing Values?
N/A Number of Web Hits:
64421
Dataset Description (https://archive.ics.uci.edu/ml/datasets/Wireless+Indoor+Localization#)
We had to apply PCA and Feature Selection on data. The two classifiers we used were Logistic Regression and Decision Tree.
For the PCA, the dataset was mean centered and scaled. Then using the Covariance matrix and, Eigen Values and Vectors, The Principle components were calculated. The scores were calculated for all the principle components using Eigen Vector (principle components) and the data.
Next, to determine the number of Principle components to be used, we built the models for all values of n (n = no. of Principle components). On looking at the accuracies, we could tell after which component the model was overfitting.
For both Logistic Regression and Decision Tree, the model was overfitting after 3rd component. So we built both the models for n = 3. The results (training time, testing time, accuracy and confusion matrix was noted.
For the Feature Selection, we determined the best to worst Features using the backward search technique. The data was arranged according to the best to worst columns.
Next, to determine the number of Features to be used, we built the models for all values of n (n = no. of features). On looking at the accuracies, we could tell after how many features the model was overfitting.
For both Logistic Regression and Decision Tree, the model was overfitting after 2 features. So we built both the models for n = 2. The results (training time, testing time, accuracy and confusion matrix was noted.
From the results (given in results.docx), it can be said that Feature Selection gives better results than PCA for both the classifiers. The aim of PCA is dimensionality reduction. We remove the attributes with low variance. This will result in losing information. Also, the PCA doesn’t consider target variable for this approach. On the flip side, in Feature Selection, we are removing the attribute based on accuracy considering the target value.
