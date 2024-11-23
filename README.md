To enhance the efficiency of Security Operation Centers (SOCs) a machine learning model that predicts the triage grade of cybersecurity incidents is much needed. 
The model will classify incidents into three categories:
1.	True Positive (TP)
2.	Benign Positive (BP)
3.	False Positive (FP)
   
Building the model involves the following steps:

•	The GUIDE train dataset contains records of cybersecurity incidents along with their corresponding triage grades (TP, BP, FP) based on historical evidence
and customer responses. 
Preprocessing steps include:

Handling Missing Data: Identifying and addressing any missing values in the dataset.

Feature Engineering: Creating new features to improve model.

Encoding: Using appropriate encoding techniques for the dataset columns.


•	Processing Steps:
Train-Validation Split and Stratification: Data is split into 70-30 ratio and stratified sampling is done to create the train and validation sets for training the models.

Baseline Model - Logistic regression, decision tree & Advanced Models- Random Forests, Gradient Boosting Machines (e.g., XGBoost, LightGBM),
and Neural Networks are built using the given dataset.

Performance Metrics: These models are evaluated using the validation set, focusing on macro-F1 score, precision, and recall.

Cross-Validation is implemented to ensure the model's performance is consistent across different subsets of the data and avoid overfitting.

Feature Importance: The best model is picked and retrained with the important features and finally is evaluated with the GUIDE test dataset.

Pickling: The trained model is stored in pickle format.

•	Recommendations for Deployment:

SOC Integration: Integrate the model with SOC tools to automate triage and provide context-rich recommendations for analysts.

Handling Misclassifications: Implement a feedback loop for analysts to correct errors and use confidence scores to flag low-confidence predictions for human review.

Note: As the training dataset in large , ensure to train the models in separate notebooks.
