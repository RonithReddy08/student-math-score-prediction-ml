# Student Math Performance Prediction Using Machine Learning

This project is a complete machine learning pipeline and web application designed to predict a student's math score based on demographic and academic factors. The objective is to demonstrate how machine learning can provide insights into student performance and how it can be applied in educational data analysis and predictive modeling.

The system uses a trained regression model integrated into a Flask-based web interface. Users input student attributes to receive real-time math score predictions out of 100.

---

## 1. Introduction

Educational outcomes are shaped by a wide range of influences—socioeconomic, demographic, and academic. This project applies machine learning techniques to explore these influences and predict math performance. By deploying an end-to-end solution, we showcase the use of real-world datasets to drive personalized insights for students.

---

## 2. Project Goals

- Build a supervised regression model that predicts math scores based on student profiles.
- Identify key contributing factors such as reading and writing ability, parental education, and test prep.
- Develop a clean and accessible web interface for user input and prediction display.
- Illustrate the entire machine learning workflow: data ingestion, feature engineering, model training, evaluation, and deployment.

---

## 3. Features

- Predicts math scores using a trained machine learning model.
- Inputs include:
  - Gender
  - Race/Ethnicity
  - Parental Level of Education
  - Lunch Type
  - Test Preparation Course
  - Reading Score
  - Writing Score
- Fully integrated with a Flask-based web application.
- Responsive and clean UI built with HTML/CSS.
- Model performance logs and artifacts saved for reproducibility.

---

## 4. Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/RonithReddy08/student-math-score-prediction-ml
   cd fuzzy-spoon
    ```
3. Install the required dependencies: `pip install -r requirements.txt`

## 5 .Usage

1. Run the application: `python app.py`
2. Access the web interface in your browser at `http://localhost:5055`
3. Fill in the student information and submit the form to obtain the predicted math score.

## 6. Dataset
The dataset used is sourced from Kaggle: Students Performance in Exams.

It contains 1,000 records and the following features:

- gender: male / female
- race/ethnicity: group A–E (anonymized labels)
- parental level of education: education attainment level
- lunch: standard or free/reduced lunch
- test preparation course: none or completed
- math score, reading score, writing score: integer scores (0–100)

## 7. Model Training
The goal was to predict the math score of a student based on academic and demographic input using supervised regression.

### 7.1 Models Evaluated
Linear Regression
- Simple, interpretable baseline
- Could not capture non-linear relationships in the data

Decision Tree Regressor
- Handled non-linear patterns
- Susceptible to overfitting

Random Forest Regressor ✅ (Selected)
- Ensemble of decision trees
- Reduced overfitting, strong generalization
- Delivered highest R² score (~85%) and most stable predictions
- Easy to deploy and interpret feature importances

CatBoost Regressor
- Advanced gradient boosting model with excellent performance on categorical features
- Slightly better accuracy, but slower and heavier for deployment
- Not selected to keep the app lightweight

### 7.2 Final Model Choice
We selected Random Forest Regressor due to its:
- High accuracy
- Balanced performance
- Low overfitting
- Fast inference time

### 7.3 Preprocessing Steps
- Categorical Encoding: One-hot encoding for all categorical features
- Train/Test Split: 80% training, 20% testing
-Target Variable: math score
- Evaluation Metrics: R² score, Mean Absolute Error (MAE)

## 8. Results
- R² Score: ~85% on test data
- Key contributors: reading score, writing score, test preparation course, parental education
- Predictions were consistent and showed minimal variance between training and test sets


## 9. Author
Ronith R
- USN: 1CR20CS160
- University: Visvesvaraya Technological University (VTU)
- Accredited with A Grade by NAAC

Under the Guidance of:
- Lynsha HP, Assistant Professor
- Department of Computer Science & Engineering

