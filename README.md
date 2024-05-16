# Fraud-Detection

Model Overview
FRAUD DETECTION IN BANKING
1. Data Splitting:
- The dataset is split into training and testing sets using the `train_test_split` function from
scikit-learn. The training set is used to train the model, while the testing set is used to evaluate its performance.
2.Feature Standardization:
- The features in the dataset are standardized using the `StandardScaler` from scikit-learn.
Standardization ensures that all features have a mean of 0 and a standard deviation of 1. This is done because LogisticRegression is dependent on distance and weights and it should not get affected by unevenly scaled datasets.
3. Oversampling of Minority Class:
- The minority class (fraudulent transactions) is oversampled using the
`RandomOverSampler` from the `imbalanced-learn` library. This helps mitigate the impact of class imbalance, allowing the model to better learn from the minority class examples.
4. Calculation of Class Weights:
- Class weights are calculated for the logistic regression model. These weights are used to
give more importance to the minority class during training, helping the model to better handle imbalanced classes.
5. Logistic Regression Model:
- A logistic regression model is instantiated and trained on the oversampled data.
Logistic regression is a commonly used algorithm for binary classification tasks, such as fraud detection.
6. Model Evaluation:
- The trained model is evaluated on the testing set using the `classification_report` from
scikit-learn. This report provides metrics such as precision, recall, F1-score, and support for each class, allowing a comprehensive assessment of the model's performance.
Submitted by
Qamar Ali qamarali9584@gmail.com
+91-8851175381
 
 How I selected the variables?
I performed a correlation analysis on the data which gave me the correlation between the target variable and the remaining features.
After sorting the features based on their correlation coefficient (which varies b/w 0 and 1) I was able to select the relevant features.
Key factors predicting fraudulent customers
1. Transaction Amount:
- Unusually large or small transaction amounts compared to typical customer behaviour can be indicative of fraud.
2. Transaction Frequency and Patterns:
- Sudden spikes or anomalies in transaction frequency, especially during non-typical hours, may indicate fraudulent activity. Unusual patterns, such as a high number of transactions in a short period, might be red flags.
3. Geographical Location:
- Transactions originating from unusual or unexpected locations, especially those known for high fraud rates, could be suspicious.
4. User Authentication and Device Information:
- Changes in user authentication behaviour, such as multiple failed login attempts, can signal potential fraud. Additionally, analysing the device used for the transaction, including device type and location, can provide insights.
5. Transaction Type:
- Certain types of transactions, such as cash withdrawals, international transfers, or purchases in high-risk categories, may be more prone to fraud. Monitoring these transaction types can help identify suspicious activity.
6. Time of Day:
- Unusual transaction times, especially during non-business hours or when the account holder is known to be inactive, can be indicative of fraudulent activity.
 
 Preventions while updating company infrastructure specifically with respect to banking sector:
1. Continuous Monitoring:
Implement continuous monitoring systems to detect unusual patterns or anomalies in transaction behaviour. This can include real-time monitoring of transaction volumes, amounts, and locations.
2. Multi-Factor Authentication :
Strengthen authentication processes by implementing multi-factor authentication. This adds an extra layer of security by requiring users to provide multiple forms of identification, such as passwords, tokens, or biometrics.
3. Behavioural Analytics:
Implement behavioural analytics to establish a baseline of normal user behaviour. Any deviations from the established patterns can trigger alerts for further investigation, potentially identifying fraudulent activities.
10. Transaction Limits
Set transaction limits and implement real-time controls to block or flag transactions that exceed predefined limits.
   
Evaluating the effectiveness of fraud prevention measures implemented in a banking environment:
Key Performance Indicators (KPIs):
Define and track key performance indicators related to fraud prevention. Common KPIs include the number of detected fraud incident rates, false positive rates, the time taken to resolve fraud-related issues, customer complaint rates, etc.
a) Reduction in Fraud Incidents:
Measure the reduction in the number and frequency of fraudulent incidents after implementing the preventive measures. A decrease in fraud incidents is a positive indicator of the effectiveness of the measures.
b) False Positive Rates:
Evaluate false positive rates, which measure the number of legitimate transactions incorrectly flagged as fraudulent. High false positive rates can lead to customer inconvenience and additional operational costs.
c) Customer Feedback and Complaints:
Monitor customer feedback and complaints related to fraud prevention measures. If customers experience challenges or express dissatisfaction, it may indicate areas that require further improvement or adjustment.
d) Response Time to Incidents:
Assess the efficiency of the incident response process. Measure the time taken to detect, investigate, and resolve reported fraud incidents. A quicker response time indicates a more effective and agile response system.
e) Customer Satisfaction Surveys:
Conduct customer satisfaction surveys to gather feedback on their experiences with fraud prevention measures. Positive feedback may indicate that customers feel secure and protected.
