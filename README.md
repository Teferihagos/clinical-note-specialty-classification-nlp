# Clinical Note Specialty Classification Using NLP

## Project Overview

## Project Overview

This project uses Natural Language Processing (NLP) and machine learning to classify clinical notes into medical specialties. The goal is to simulate a healthcare workflow where unstructured clinical text must be organized automatically.

This project follows a production-style structure by separating preprocessing, training, and evaluation into modular Python scripts.


## Business Problem

Healthcare systems store large amounts of information as free-text clinical notes. Manually sorting these notes into specialties is slow and inconsistent. This project builds an NLP pipeline that predicts the specialty of a clinical note from its text.

## Dataset

This project uses the MTSamples medical transcription dataset from Kaggle. The original dataset contained 40 specialties, but this project focused on the 10 most frequent specialties to create a cleaner and more reliable classification problem.

## Workflow

1. Data understanding
2. Data cleaning
3. Text preprocessing
4. TF-IDF feature extraction
5. Model training
6. Model evaluation
7. Model comparison

## Text Preprocessing

The preprocessing steps included:

* converting text to lowercase
* removing punctuation and special characters
* removing common English stopwords

## Models Used

* Logistic Regression
* Linear SVM

## Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

## Results

* Logistic Regression Accuracy: **38.5%**
* Linear SVM Accuracy: **27.5%**

Logistic Regression performed better than Linear SVM on this dataset. This suggests that Logistic Regression generalized better under class imbalance and default model settings.

## Key Findings

* The model performed best on large classes such as Surgery.
* Smaller specialties were harder to classify because of class imbalance.
* The normalized confusion matrix showed that several specialties were frequently confused with dominant classes.
* Testing multiple models was important, because the more advanced-sounding model did not perform better.

## Project Structure

```text
clinical-note-specialty-classification/
│
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   └── clinical_note_specialty_classification.ipynb
├── src/
│   ├── preprocessing.py
│   ├── train.py
│   └── evaluate.py
├── models/
│   ├── best_model.pkl
│   └── tfidf_vectorizer.pkl
├── images/
│   ├── confusion_matrix.png
│   └── model_comparison.png
├── reports/
│   └── project_summary.md
├── README.md
├── requirements.txt
└── .gitignore
```

## Future Improvements

* tune TF-IDF parameters
* apply class balancing methods
* test advanced NLP models
* expand beyond the top 10 specialties

## How to Run

1. Clone the repository
2. Install dependencies from `requirements.txt`
3. Open the notebook in the `notebooks` folder
4. Run the cells in order

## Author

Teferi A. Hagos
