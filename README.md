# Fraud-Detection-System
## Tasks Performed
## 1. Data Cleaning (Missing Values, Outliers, Multi-Collinearity):
Missing Values: During the data preprocessing phase, any missing values in the dataset were either imputed using statistical techniques (such as mean/median imputation) or dropped depending on the proportion of missing data in the columns. Critical variables with large proportions of missing data were carefully handled to avoid data leakage or bias.

Outliers: Outliers were identified using techniques like Z-scores and the IQR method. Since extreme values can significantly impact model performance, outliers were capped or transformed to reduce their influence.

Multi-Collinearity: Multi-collinearity was checked using the Variance Inflation Factor (VIF). Variables with high VIF were either combined, transformed, or removed to avoid redundancy in the model and ensure interpretability.

## 2. Fraud Detection Model (XGBoost):
After experimenting with the Random Forest algorithm, which did not perform as well as expected in terms of accuracy, the model was switched to XGBoost. XGBoost is a powerful gradient boosting algorithm that excels in classification tasks, especially on large, imbalanced datasets such as fraud detection. XGBoost's ability to handle imbalanced datasets and its regularization features helped improve the precision and recall, leading to an impressive accuracy of 99.98%.

## 3. Variable Selection for the Model:
The variables included in the model were selected based on their relevance to fraud detection. The following methods were used:

Correlation Matrix: To check the relationship between variables and remove highly correlated variables to prevent multi-collinearity.

Feature Importance from Random Forest: Initially, the Random Forest model provided a good insight into which variables had the most predictive power. Based on that less important features were dropped.

Domain Knowledge: Variables related to transaction amounts, transaction types, account history, and geographical locations were intuitively important in detecting fraud. They were kept in the model.

## 4. Model Performance Demonstration:
The model performance was measured using:

Accuracy: 99.98%, which shows that most transactions were classified correctly.

Confusion Matrix: Indicating the number of true positives, true negatives, false positives, and false negatives.

Precision: 0.96 for fraud, indicating that 96% of predicted fraud cases were truly fraudulent.

Recall: 0.85 for fraud, meaning that the model correctly identified 85% of the actual fraud cases.

F1 Score: A balanced measure that accounts for both precision and recall, ensuring the model performs well in identifying fraudulent cases while minimizing false positives.

## 5. Key Factors that Predict Fraudulent Customers:
Based on the model and analysis, the key predictors for fraudulent transactions include:

Transaction Amount: Unusually high or low amounts compared to a customer’s historical behavior can indicate potential fraud.

Account Activity: Sudden spikes in the number of transactions, especially international ones.

Transaction Type: Certain types of transactions, such as wire transfers or online purchases, may be more prone to fraud.

Customer Demographics: Features such as geographical location and account age can also play a role.

Behavioral Anomalies: Transactions that deviate from typical spending patterns (time of day, location, etc.).

## 6. Do These Factors Make Sense?:
Yes, they do make sense because they are in line with general expectations of fraud detection:

Transaction Amount: Fraudsters often attempt to make high-value transactions.

Account Activity and Behavior: Fraudulent activity often involves sudden and significant changes in behavior, such as more frequent and unusual transactions.

Transaction Type: Certain types of transactions are inherently riskier and are thus more prone to fraud.

Geographic Location: Fraudsters may operate across borders, so international transactions or those originating from unusual locations are red flags.

## 7. Prevention Measures for Infrastructure Updates:
If a company is updating its infrastructure to combat fraud, several preventative measures should be taken:

Enhanced Authentication: Implement multi-factor authentication (MFA) to make it harder for unauthorized users to access accounts.

Real-time Monitoring: Utilize AI and machine learning models (like XGBoost) to monitor transactions in real-time and flag suspicious activities instantly.

Encryption and Data Security: Ensure all sensitive customer data is encrypted, both in transit and at rest, to prevent unauthorized access.

Fraud Detection Systems: Regularly update fraud detection models with new data to adapt to evolving fraud techniques.

Employee Training: Educate employees on the latest security practices and phishing tactics to prevent internal security breaches.

## 8. Evaluating the Effectiveness of Implemented Actions:
To determine if these actions have been successful, you can:

Monitor Fraud Rates: Track the number of fraudulent transactions before and after the infrastructure update. A decrease in fraud cases indicates success.
Customer Feedback: Regularly survey customers to see if they feel more secure and have noticed any issues.
Model Performance: Continue monitoring the performance metrics of the XGBoost model to ensure it maintains high precision and recall.





