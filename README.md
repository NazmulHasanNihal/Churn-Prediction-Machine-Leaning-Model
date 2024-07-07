# Customer Churn Prediction

This project aims to predict customer churn using historical data and various machine learning models. The dataset contains customer information and whether they have exited (churned) or not. The project includes data preprocessing, feature engineering, model training, evaluation, and explainability using tools like LIME and SHAP.

## Dataset

The dataset `churn_modeling.csv` includes the following columns:
- `RowNumber`: Row index
- `CustomerId`: Unique customer identifier
- `Surname`: Customer's surname
- `CreditScore`: Credit score of the customer
- `Geography`: Customer's location
- `Gender`: Customer's gender
- `Age`: Customer's age
- `Tenure`: Number of years the customer has been with the bank
- `Balance`: Account balance
- `NumOfProducts`: Number of bank products the customer is using
- `HasCrCard`: Whether the customer has a credit card
- `IsActiveMember`: Whether the customer is an active member
- `EstimatedSalary`: Estimated salary of the customer
- `Exited`: Whether the customer has exited (1) or not (0)

## Project Structure

- `churn_modeling.csv`: The dataset used for training and testing the models.
- `churn_prediction.py`: The main Python script for the project.
- `README.md`: This file.

## Workflow
The script performs the following steps:

Load and preprocess the data:

## Load the dataset.
Drop unnecessary columns (RowNumber, CustomerId, Surname).
Encode categorical variables (Geography, Gender).
Handle class imbalance using SMOTE.

Standardize features using StandardScaler.

## Model Training and Evaluation:

Train a Random Forest classifier pipeline.
Evaluate the model using various metrics (Accuracy, ROC AUC, F1 Score, Precision, Recall, Confusion Matrix, Classification Report).
Train and evaluate a Voting Classifier (Logistic Regression, Random Forest, Gradient Boosting).

## Advanced Evaluation Metrics:

Calculate Matthews Correlation Coefficient (MCC), Cohen's Kappa, and Log Loss.

## Learning Curves:

Plot learning curves to understand model performance over different training sizes.

## Model Explainability:

Use LIME for local interpretable model-agnostic explanations.
Use SHAP for global model interpretability.

## Model Saving and Loading:

Save the trained Voting Classifier model.
Load the model and evaluate it.

## Cross-validation:

Perform standard cross-validation.
Perform time-series cross-validation.
Results

## The script prints the following evaluation metrics for both the Random Forest and Voting Classifier models:

Accuracy
ROC AUC
F1 Score
Precision
Recall
Matthews Correlation Coefficient (MCC)
Cohen's Kappa
Log Loss
Confusion Matrix
Classification Report
Additionally, it generates learning curves, and model explainability plots using LIME and SHAP.

## Additional Information
Cross-validation and Time-series Cross-validation
The script performs both standard cross-validation and time-series cross-validation to evaluate model performance across different data splits.

## Model Explainability
The project uses LIME and SHAP to provide insights into the model's predictions, helping to understand which features are most influential in predicting customer churn.

## Saving and Loading the Model
The trained Voting Classifier model is saved to a file (voting_classifier_model.sav) and can be loaded for future use.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## Acknowledgements
This project was inspired by the need to understand and predict customer churn in various industries. Special thanks to the open-source community for providing tools like scikit-learn, imbalanced-learn, LIME, and SHAP that make such projects possible.
