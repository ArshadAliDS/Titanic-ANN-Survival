# Titanic Survival Prediction Using Artificial Neural Networks (ANN) with Keras

## Overview

In this project, I have implemented an **Artificial Neural Network (ANN)** to predict passenger survival on the Titanic using the famous **Titanic dataset**. The goal is to classify passengers as either survivors or non-survivors based on various features such as gender, age, ticket class, and fare. This project utilizes **deep learning techniques** with the **Keras** and **TensorFlow** libraries.

---

## Problem Statement

The Titanic dataset is a well-known dataset used in machine learning, where the goal is to predict whether a passenger survived or not. This is a **binary classification problem**, where we need to predict the class `0` (Did not survive) or `1` (Survived) based on the given features.

### Features

- `Pclass` (Passenger class)
- `Sex`
- `Age`
- `SibSp` (Number of siblings/spouses aboard)
- `Parch` (Number of parents/children aboard)
- `Fare`
- `Embarked` (Port of Embarkation)

---

## Objective

- Build an **Artificial Neural Network** (ANN) to classify passengers as survivors or non-survivors.
- Use **deep learning techniques** for feature scaling, model building, and evaluation.
- Demonstrate the effectiveness of ANN models for binary classification problems.

---

## Dataset

The dataset used for this project is the **Titanic dataset**, which can be found on [Kaggle](https://www.kaggle.com/c/titanic) or accessed via a URL in the code. It contains information about Titanic passengers, including their demographics, ticket class, and survival status.

---

## Preprocessing Steps

1. **Drop irrelevant columns:** I removed columns like `PassengerId`, `Name`, `Ticket`, and `Cabin` because they are not directly useful for prediction.
2. **Handle missing values:** Missing values in `Age` were filled with the median age, and missing values in `Embarked` were filled with the mode (most frequent value). 
3. **Convert categorical variables:** The categorical variables `Sex` and `Embarked` were converted into numeric form using **Label Encoding**.
4. **Feature scaling:** To ensure that all input features are on the same scale, I applied **StandardScaler** to standardize the features.

---

## Building the ANN Model

For the classification task, I created a **Sequential Neural Network model** using the **Keras** library:

- **Input layer:** The first layer accepts the preprocessed features (7 input features).
- **Two hidden layers:** Each with **16 neurons** and **8 neurons**, respectively, using the **ReLU (Rectified Linear Unit)** activation function.
- **Output layer:** A single neuron with the **sigmoid** activation function to predict the probability of survival (0 or 1).

The model was compiled using the **Adam optimizer** and **binary crossentropy** loss function, which is suitable for binary classification tasks. I trained the model for 50 epochs with a batch size of 32.

---

## Model Evaluation

The model's performance was evaluated using:
- **Accuracy Score** on the test set.
- **Classification Report** to provide insights into precision, recall, and F1-score.
- **Confusion Matrix** to understand the number of correct and incorrect predictions.
