# **Titanic Survival Prediction**

This repository contains my solution for the **Titanic - Machine Learning from Disaster** competition on Kaggle. The goal of this project is to predict the survival of passengers aboard the Titanic using machine learning techniques.

## **Project Overview**

The Titanic dataset provides information on passengers aboard the Titanic, including details like age, gender, class, and fare. The challenge is to predict if a passenger survived the Titanic disaster based on these features. The competition serves as a beginner-friendly introduction to data science and machine learning.

## **Files in this Repository**

- **`train.csv`**: Training dataset containing passenger information and survival status.
- **`test.csv`**: Test dataset containing passenger information without survival status.
- **`gender_submission.csv`**: A sample submission file provided by Kaggle.
- **`Titanic Solution.py`**: The main Python script that processes the data, trains the model, and generates predictions.
- **`submission.csv`**: The generated submission file containing survival predictions for the test set, with an accuracy of 76.32% on Kaggle.

## **Solution Workflow**

The solution follows these main steps:

1. **Data Loading**: Load the train and test datasets.

2. **Data Cleaning and Preprocessing**:
   - Fill in missing values for features such as `Age` and `Embarked`.
   - Convert categorical variables (like `Sex`) to numerical values.

3. **Feature Engineering**:
   - Select key features that may influence survival, such as `Pclass`, `Sex`, `Age`, `Fare`, and `Embarked`.

4. **Model Training**:
   - Train a machine learning model (e.g., Random Forest or Logistic Regression) on the training data.

5. **Prediction**:
   - Use the trained model to predict survival on the test data.

6. **Submission File Creation**:
   - Generate `submission.csv` with `PassengerId` and `Survived` columns, as required by Kaggle for submission.

## **Explanation of the Code**

### **Data Preprocessing**
The code begins by loading the datasets (`train.csv` and `test.csv`). It identifies and handles missing values in key features:
- **Age**: Filled with median age to account for missing values.
- **Embarked**: Filled with the most common port of embarkation.

The `Sex` column is encoded to numerical values, with male as `0` and female as `1`. This encoding allows machine learning models to process this feature effectively.

### **Feature Selection**
The model uses the following features for prediction:
- **Pclass**: Passenger class (1st, 2nd, or 3rd).
- **Sex**: Gender of the passenger.
- **Age**: Age of the passenger.
- **Fare**: Ticket fare.
- **Embarked**: Port of embarkation (S, C, Q).

### **Model Training**
The code trains a machine learning model (such as Random Forest or Logistic Regression) on the selected features from the training data. The model’s hyperparameters may be tuned for better performance, though the current version aims to provide a baseline solution for prediction.

### **Making Predictions**
Once the model is trained, it is used to make predictions on the test set. The predictions indicate whether each passenger in the test set survived (1) or not (0).

### **Generating the Submission File**
The predictions are saved in `submission.csv`, which contains:
- **PassengerId**: Identifier for each passenger.
- **Survived**: Prediction of survival status (1 for survived, 0 for deceased).

This file is submitted to Kaggle for evaluation, resulting in an accuracy of **76.32%**.

## **Results**

The model achieved an accuracy score of **0.76315** on the Kaggle leaderboard, reflecting the percentage of passengers for whom survival was correctly predicted.

## **Conclusion**

This project demonstrates the basics of data preprocessing, feature engineering, and model training for a classification task in Python. The Titanic competition provides a straightforward entry point for learning data science techniques, allowing experimentation with feature selection and model tuning.

Feel free to explore the code and make improvements. Feedback and contributions are welcome!
