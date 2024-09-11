# Titanic Survival Prediction Project

This project predicts whether a Titanic passenger survived based on features like class, gender, and family size, using a Support Vector Machine (SVM) model.

## Project Overview

The goal of this project is to create a machine learning model that predicts the survival of Titanic passengers. The data includes information such as passenger class, sex, age, and family details.


## Data Analysis

### Key Findings:
- **Missing Data**: We observed missing values in columns like `Age`, `Cabin`, and `Embarked`, with 177 missing values in `Age` and 687 in `Cabin`.
- **Survival Rate by Gender**:
  - 74% of women survived.
  - 19% of men survived.
- **Embarkation**: Most passengers boarded from `S`, followed by `C` and `Q`.

## Feature Engineering

For this project, we selected features like:
- Passenger class (`Pclass`)
- Sex (`Sex`)
- Number of siblings/spouses aboard (`SibSp`)
- Number of parents/children aboard (`Parch`)
- Port of embarkation (`Embarked`)

We used one-hot encoding to convert categorical features into a format suitable for the model.

## Model Training

We used an SVM classifier with a linear kernel to predict survival. The dataset was split into 80% training and 20% testing. The model achieved an accuracy of **83.15%** on the test set.

## Model Evaluation

### Confusion Matrix:
|        | Predicted No | Predicted Yes |
|--------|--------------|---------------|
| Actual No  | 93           | 12            |
| Actual Yes | 18           | 55            |

This matrix shows that:
- 93 passengers were correctly predicted not to survive.
- 55 passengers were correctly predicted to survive.
- 12 passengers were incorrectly predicted to survive.
- 18 passengers were incorrectly predicted not to survive.

## Conclusion

The SVM model provides good baseline accuracy at 83%. Further improvements can be made through feature engineering and hyperparameter tuning.

## Technologies Used
- **Pandas**: For data manipulation.
- **Scikit-learn**: For machine learning modeling.
- **Numpy**: For numerical operations.
