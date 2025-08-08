Flask-based Fraud Detection Machine Learning System utilizes XGBoost for training and SMOTE for handling imbalanced data, achieving an F1 score of 0.92 on Kaggle dataset.
 
User Interaction:
Users submit transaction data to the Flask app for fraud prediction.Flask preprocesses this data and uses a pre-trained ML model to determine fraud likelihood

Model Maintenance:
A scheduler periodically checks an S3 bucket for new data.Upon finding new data, the system triggers model retraining

Model Retraining:
A pre-trained model is loaded and fit with new provided data.Updated models are synchronized with the app's model cache and stored in the S3 bucket.
