# Fake News Detection with NLP 📰🔍

This project is developed to classify Turkish news texts using Natural Language Processing (NLP) techniques and machine learning methods. The goal is to analyze the content of the texts and classify them correctly. The project compares the performance of different algorithms by modeling with each of them.

## Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Method](#method)
- [Results](#results)
- [Installation and Running Instructions](#installation-and-running-instructions)

## Project Overview

This project is designed to classify Turkish news headlines. The dataset consists of news headlines with labels indicating whether the news is "True" or "False". The project applies NLP steps to process the texts and then creates models using different machine learning algorithms. The accuracy of the models is compared, and the best performing model is selected.

## Technologies Used

The project is developed using the following technologies and libraries:

- **Python**: The project is written in Python.
- **Google Colab**: The project is run on Google Colab.
- **zemberek-python**: Used for Turkish text processing.
- **emoji**: Used to remove emojis from texts.
- **pandas**: Used for data manipulation and analysis.
- **numpy**: Used for numerical computations.
- **nltk**: Provides various functions for Natural Language Processing.
- **scikit-learn**: Used to build and evaluate machine learning models.
- **XGBoost**: A high-performance classification algorithm.
- **matplotlib and seaborn**: Used for data visualization.

## Project Structure

- `dataset.xlsx`         : Dataset used in the project
- `turkce-stop-words.txt` : Turkish stopwords list
- `Fake_news_detection_with_NLP.ipynb`            : Main Jupyter notebook file
- `README.md`             : Project description


## Dataset

The dataset consists of news headlines and their labels indicating the truthfulness of the news. The labels are either "True" (accurate) or "False" (misleading). The dataset includes the following columns:

- **News**: The news headlines (text data)
- **Result**: Labels indicating whether the news is true (True) or false (False)

## Method

### 1. Data Preprocessing

- **Removal of Punctuation and Numbers**: Unnecessary punctuation marks and numbers are removed from the texts.
- **HTML Tag Removal**: HTML tags are removed from the text.
- **Emoji Removal**: Emojis in the text are identified and removed.
- **Stopwords Removal**: Turkish stopwords and additional custom stopwords are removed from the text.
- **Tokenization**: Texts are split into meaningful units (words).

### 2. Feature Extraction

- **Bag-of-Words**: The text data is transformed into numerical features using `CountVectorizer`.
- **TF-IDF**: The importance of words is calculated using `TfidfTransformer`, and the texts are weighted accordingly.

### 3. Modeling

Different machine learning algorithms were used to build classification models for text classification:

- **Naive Bayes**: A simple yet effective classification algorithm.
- **K-Nearest Neighbors (KNN)**: A classification algorithm based on proximity to the nearest neighbors.
- **Support Vector Machine (SVM)**: Used for non-linear classification.
- **Logistic Regression**: A commonly used regression model for classification problems.
- **XGBoost**: A high-performance and fast classification model.

### 4. Model Evaluation

Model performance is evaluated using metrics like **accuracy score** and **confusion matrix**. The model with the highest accuracy was the **XGBoost** model.

## Results

- **Naive Bayes**: 85.35%
- **K-Nearest Neighbors**: 83.44% (Best result with 7 neighbors)
- **SVM**: 87.90%
- **Logistic Regression**: 84.08%
- **XGBoost**: 91.08%

The **XGBoost** model achieved the best performance with the highest accuracy.
