# Fake Alert - Fake News Detection using Machine Learning

## Overview

Fake Alert is a machine learning project that detects whether a news article is fake or legitimate based on its textual content. The goal of this project was to explore how Natural Language Processing (NLP) techniques can be used to identify misinformation and compare the performance of different machine learning models on news data.

The project was developed using Python in Jupyter Notebook and includes data preprocessing, exploratory data analysis, feature engineering using TF-IDF, model training, evaluation, and prediction on custom news articles.

---

## Dataset

The dataset used in this project is a multilingual fake news dataset containing news articles from different domains such as:

* Business
* Politics
* Technology
* Education
* Sports
* Entertainment
* Celebrity News

For this implementation, only the English dataset was used.

The original dataset was collected as part of the research work:

**"A Transformer Based Approach to Multilingual Fake News Detection"**

published in ACM Transactions on Asian and Low-Resource Language Information Processing (ACM-TALLIP).

---

## Project Workflow

### 1. Data Preparation

The dataset was provided as separate files for different domains. These files were combined into a single dataset and organized into three columns:

* text
* label
* domain

---

### 2. Data Cleaning

Before training the models, the text data was cleaned by:

* Converting text to lowercase
* Removing URLs
* Removing punctuation
* Removing special characters
* Removing extra spaces

This helped reduce noise in the dataset and improve model performance.

---

### 3. Exploratory Data Analysis

Basic EDA was performed to understand:

* Distribution of fake and legitimate news
* Domain-wise distribution
* Missing values
* Dataset balance

Visualizations were created using Matplotlib and Seaborn.

---

### 4. Feature Engineering

Since machine learning models cannot work directly with text, the cleaned news articles were converted into numerical representations using:

**TF-IDF (Term Frequency - Inverse Document Frequency)**

TF-IDF assigns higher importance to words that are useful for distinguishing documents while reducing the impact of very common words.

---

### 5. Model Training

Two models were trained and evaluated:

#### Multinomial Naive Bayes

Used as a baseline model because it performs well on text classification problems and is computationally efficient.

#### XGBoost Classifier

Used as an advanced model to improve prediction performance by capturing more complex relationships in the data.

---

### 6. Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

The performance of both models was compared to determine the better classifier.

---

### 7. Feature Importance

For interpretability, feature importance analysis was performed on the XGBoost model to identify words that had a strong influence on the predictions.

This provided insight into how the model was making decisions.

---

### 8. Custom Prediction System

A prediction function was created that allows users to enter any news article and receive:

* Prediction (Fake or Legitimate)
* Confidence Score

Example:

Input:

"Scientists confirm that aliens have landed in New York."

Output:

Prediction: Fake

Confidence Score: 93.5%

---

## Libraries Used

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost

---

## What I Learned

Through this project, I gained practical experience in:

* Data preprocessing
* Natural Language Processing
* Feature engineering using TF-IDF
* Text classification
* Model evaluation
* Working with real-world datasets
* Building end-to-end machine learning pipelines

---

## Future Improvements

Some possible improvements for this project include:

* Adding support for multiple languages
* Using transformer-based models such as BERT
* Building a web application using Flask or Streamlit
* Integrating real-time news verification APIs
* Adding explainable AI techniques such as SHAP

---

## Author

Sanika Nayse

Machine Learning and Data Science Enthusiast
