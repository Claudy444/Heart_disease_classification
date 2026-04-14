# Heart_disease_classification
A binary classification project to predict heart disease using clinical patient data. Includes data exploration, pipeline-based preprocessing, and a performance comparison between multiple machine learning models.


Project: Heart Disease Classifier
Goal: I built this model to help flag heart disease risk early. My main focus wasn't just accuracy, but making sure we don't miss sick patients (minimizing False Negatives).

The Results (Test Set)
Recall: 96% — Out of 28 sick patients, the model caught 27.

Precision: 69% — When the model flags a patient, it's right about 7 out of 10 times.

F1-Score: 0.81 — Shows the model is well-balanced and didn't just "guess" to get high recall.

How I Built It
Algorithm: I used Logistic Regression (compared to RandomForestClassifier) because it’s reliable and gives clear probabilities rather than just a "yes/no" answer.

The "Magic Number": I moved the decision threshold from the default 0.5 down to 0.2471. I did this because, in medicine, a False Alarm is okay, but a missed diagnosis is a bigger call for concern.

Validation: I used 5-fold cross-validation during training to make sure the 0.2471 threshold wasn't just a lucky guess.

Final Confusion Matrix
[[21 12]  <-- 21 Healthy people identified
 [ 1 27]] <-- 27 Sick people identified, only 1 missed.
 What's Next
Pipeline Automation: I want to eventually automate the data cleaning (dropping features, encoding) so the model can handle raw data faster.

Regression Tasks: Moving on to predicting continuous values next to get better at different types of ML tasks.