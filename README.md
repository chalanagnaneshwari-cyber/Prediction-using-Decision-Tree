Titanic Survival Prediction using Decision Tree

#Project Overview

This project uses a **Decision Tree Classifier** to predict whether a passenger survived the Titanic disaster.

The prediction is based on the following features:

- Passenger Class (`pclass`)
- Sex (`sex`)
- Age (`age`)
- Fare (`fare`)

The target variable is:

- **Survived** (`0 = No`, `1 = Yes`)

---

#Objective

The main objective of this project is to train a machine learning model to predict passenger survival and evaluate its performance on data it has not seen before.

---

#Technologies Used

- Python
- Pandas
- Seaborn
- Matplotlib
- Scikit-learn

---

#Project Steps

# 1. Data Preparation
The required columns were selected from the Titanic dataset. Rows with missing values were removed, and the `sex` column was converted into numerical values.

- Female = 0
- Male = 1

# 2. Train-Test Split
The dataset was divided into:

- **80% Training Data**
- **20% Testing Data**

The split used:

- `test_size = 0.2`
- `random_state = 42`
- `stratify = y`

# 3. Baseline Model
A simple baseline was created by always predicting the most common survival outcome. The Decision Tree model was compared with this baseline.

# 4. Model Training
A Decision Tree Classifier was trained using:

```python
DecisionTreeClassifier(max_depth=4, random_state=42)
```

# 5. Model Evaluation
The model was evaluated using:

- Accuracy Score
- Confusion Matrix
- Mean Squared Error (MSE)

# 6. Overfitting Analysis
Different tree depths from **1 to 12** were tested. Training and testing accuracy were compared to understand overfitting.

A very deep tree may perform extremely well on training data but worse on new data because it can memorize the training data instead of learning general patterns.

# 7. Feature Importance
The project also identifies the importance of each feature using:

```python
model.feature_importances_
```

---

# Results

The Decision Tree model was tested on unseen data and compared with the baseline model.

The confusion matrix was used to understand correct predictions and prediction errors.

The feature importance analysis showed which passenger characteristics had the greatest impact on survival prediction.

---

# Limitations

- The Titanic dataset is relatively small.
- Only four features were used for prediction.
- Results may change with a different train-test split.
- A very deep Decision Tree can lead to overfitting.

---

# Conclusion

This project demonstrates how a Decision Tree can be used to predict Titanic passenger survival. It also highlights the importance of testing a model on unseen data, comparing it with a baseline, and avoiding overfitting.
