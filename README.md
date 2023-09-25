# Na-ve-Bayes-Classifier
1.Suppose we want to build Naïve Bayes classifier for predicting whether a cricket match will be played in the given weather conditions or not. Here the weather conditions are described by features outlook, temperature,etc. The target is play with two class labels Yes and No. 
2.Assume you need to build a classifier for recognizing emotional content in music signals such as Mel Frequency Cepstral Coefficients (MFCCs), Tempo, Chromagram, Spectral and Harmonic features. There are four different classes of music emotions in the dataset: happy, sad, angry, and relax. (Dataset:  music.csv)

This code appears to be related to two different tasks: implementing a Naive Bayes classifier from scratch and then using scikit-learn to perform a similar classification task.

Naive Bayes Classifier from Scratch:

The code starts by importing the necessary libraries, primarily pandas for data manipulation.
It reads a CSV file named 'play.csv' into a pandas DataFrame.
It splits the DataFrame into a training set (train_df) and a test sample (test_sample). The last row of the DataFrame is used as the test sample, excluding the last column, which is assumed to be the target variable.
The code calculates class prior probabilities based on the 'play' column in the training set. These are the probabilities of each class occurring before any feature information is taken into account.
It then calculates feature likelihoods for each feature (column) in the dataset, given each class label. This is done by counting how often each feature value appears for each class.
Class likelihoods are calculated for each class label in the test sample by combining the class prior probabilities and feature likelihoods.
Finally, class conditional probabilities are computed for each class label by normalizing the class likelihoods.
Scikit-Learn Naive Bayes Classifier:

This part of the code reads the same 'play.csv' dataset.
It separates the features ('outlook', 'temp', 'humidity', 'wind') and the target variable ('play') from the DataFrame.
The code uses scikit-learn's CategoricalNB classifier to perform Naive Bayes classification. It also uses a LabelEncoder to encode categorical features into numerical values.
Class prior probabilities are calculated based on the target variable ('play').
A test sample with one data point is created with categorical feature values ('outlook': 'Rain', 'temperature': 'Cool', 'humidity': 'High', 'wind': 'Weak').
The features (both training and test) are encoded using LabelEncoder.
The CategoricalNB classifier is trained on the training data.
The conditional probabilities for each class label are displayed using clf.category_count_.
Additional Actions:

The code includes some additional commands for mounting Google Drive and navigating to a specific directory.
There is also an import of data from a different CSV file ('music.csv') for a different classification task using a Gaussian Naïve Bayes classifier. This part of the code seems unrelated to the previous parts.
Please note that the first part of the code attempts to implement a basic Naive Bayes classifier from scratch, but it seems to have issues (e.g., encountering NaN values) and may not work correctly. The second part, which uses scikit-learn's CategoricalNB, is a more reliable and standard way to perform Naive Bayes classification.
