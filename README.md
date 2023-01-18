# Credit_Risk_Analysis

## Overview of the analysis:
The project uses machine learning algorithms to predict credit risk to help banks predict high-risk cases and provide recommendations on what to do in cases of fraud. The credit risk problem has a highly imbalanced dataset. Different resampling techniques were tested to balance the training classes distribution to overcome the bias towards the majority class (low risk), such as oversampling (RandomOverSampler and SMOTE), undersampling (ClusterCentroids), and combinatorial approach of over- and undersampling using the SMOTEENN algorithm. In addition, Some models, which are naturally built to reduce imbalanced dataset bias, are tested, such as BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. The models' performance was compared to find the best approach to solve the credit risk classification problem. 

## Results:
The balanced accuracy, precision, and recall scores are compared for a different combination of the model tested as follows:

1. Logistic regression with the Naive Random Oversampling technique has a balanced accuracy of 64%, a precision of 1% for high-risk loans, and a recall score of 61% for high-risk loans. This indicates that the model's sensitivity to capture risky loans needs to be further improved, as missing high-risk loans is critical for the business.

<img width="1094" alt="Screenshot 2023-01-18 at 10 12 00 AM" src="https://user-images.githubusercontent.com/48078471/213261219-17350ae1-4bf9-4ed6-99d2-72089ef85cac.png">

2. Logistic regression with SMOTE Oversampling technique has a balanced accuracy of 61.6%, a precision of 1% for high-risk loans, and a recall score of 59% for high-risk loans.

<img width="1132" alt="Screenshot 2023-01-18 at 10 14 13 AM" src="https://user-images.githubusercontent.com/48078471/213261571-c0c065d8-c553-4201-9e10-301738063c62.png">

3. Logistic regression with Cluster Centroids algorithm has a balanced accuracy of 51.6%, a precision of 1% for high-risk loans, and a recall score of 60% for high-risk loans.

<img width="1108" alt="Screenshot 2023-01-18 at 10 15 13 AM" src="https://user-images.githubusercontent.com/48078471/213261723-96365f9f-c00a-482d-8276-1972f8c05594.png">

4. Logistic regression with the SMOTEENN algorithm has a balanced accuracy of 65%, a precision of 1% for high-risk loans, and a recall score of 74% for high-risk loans.

<img width="1107" alt="Screenshot 2023-01-18 at 10 18 47 AM" src="https://user-images.githubusercontent.com/48078471/213262421-505cdba0-c707-4485-9597-ab5a480d9308.png">

5. Balanced Random Forest Classifier has a balanced accuracy of 79%, a precision of 4% for high-risk loans, and a recall score of 67% for high-risk loans.

<img width="1114" alt="Screenshot 2023-01-18 at 10 20 45 AM" src="https://user-images.githubusercontent.com/48078471/213262852-69fab5e3-1291-456a-9794-522418b860aa.png">

Using the Balanced Random Forest Classifier, the feature importance can be found to understand which is meaningful for the credit risk prediction and eliminate the irrelevant features to avoid over-fitting issues. 

<img width="1090" alt="Screenshot 2023-01-18 at 10 21 46 AM" src="https://user-images.githubusercontent.com/48078471/213263005-e17369ca-9cad-4b1d-a695-d3a9e5ef9047.png">

6. Easy Ensemble AdaBoost Classifier has a balanced accuracy of 92.5%, a precision of 7% for high-risk loans, and a recall score of 91% for high-risk loans.

<img width="1103" alt="Screenshot 2023-01-18 at 10 24 58 AM" src="https://user-images.githubusercontent.com/48078471/213263621-0479c0c6-8e4e-4d19-a738-924e08aed193.png">

## Summary:

TThe evaluation results of different machine learning techniques show that the Easy Ensemble AdaBoost Classifier provides the best prediction results in terms of balanced accuracy, precision, and recall scores of high-risk credit, which are 92.5%, 7%, and 91%, respectively. 