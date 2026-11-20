\# Fraud Credit Detector



> A machine learning-powered web application for identifying potentially fraudulent credit card transactions and assessing their risk in real time.



\## About the Project



Credit card fraud is a highly imbalanced classification problem where fraudulent transactions are rare compared to legitimate ones. Because of this, simply achieving high accuracy is not enough — the model also needs to identify as many fraudulent transactions as possible without generating an excessive number of false alerts.



\*\*Fraud Credit Detector\*\* was built to explore this problem through an end-to-end machine learning application.



The project combines a \*\*Random Forest classification model\*\* with a \*\*FastAPI machine learning service\*\* and a \*\*full-stack web application\*\*. A user can enter transaction details, submit them for analysis, and receive a fraud probability along with an understandable risk level.



The main focus of the ML component is on \*\*fraud recall and overall classification quality\*\*, rather than relying only on accuracy.



\---



\## What It Does



The application takes transaction information such as:



\- Transaction amount

\- Transaction type

\- Location

\- Transaction hour



and processes it through the trained machine learning pipeline.



The system then returns:



\*\*Fraud Probability → Risk Level → Final Classification\*\*



For example, a transaction can be classified as:



\- 🟢 \*\*Low Risk\*\*

\- 🟡 \*\*Medium Risk\*\*

\- 🔴 \*\*High Risk\*\*



along with a \*\*Fraud / Legitimate\*\* prediction.



\---



\## Machine Learning Approach



\### Why Random Forest?



For this project, a \*\*Random Forest Classifier\*\* was selected as the primary classification algorithm.



The model was trained with class imbalance in mind, since fraudulent transactions represent only a small portion of the dataset. Instead of treating both classes equally, the training process uses class weighting to give greater importance to the minority fraud class.



\### Model Configuration



```text

Algorithm       : Random Forest Classifier

n\_estimators    : 200

max\_depth       : 6

min\_samples\_leaf: 3

class\_weight    : balanced

