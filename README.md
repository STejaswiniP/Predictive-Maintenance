# Predictive Maintenance Using Big Data Analytics

## Overview

This project applies big data processing and machine learning techniques to predict machine failures using equipment sensor data. It uses **PySpark** for data processing and machine learning libraries to train and evaluate classification models.

The objective is to identify potential machine failures before they occur, helping improve equipment reliability and reduce unexpected downtime.

## Objectives

- Analyze industrial sensor data for predictive maintenance.
- Build a machine learning pipeline for machine failure prediction.
- Compare multiple classification algorithms.
- Evaluate model performance, particularly its ability to identify machine failures.
- Explore how data-driven predictions can support proactive maintenance decisions.

## Dataset

**Dataset:** AI4I 2020 Predictive Maintenance Dataset

The dataset contains 10,000 records representing industrial operating conditions and machine failure information.

Key features include:
- Product type
- Air temperature
- Process temperature
- Rotational speed
- Torque
- Tool wear
- Machine failure labels

The dataset is suitable for exploring classification-based predictive maintenance.

## Technologies Used

- **Python** – Programming and model development
- **Apache Spark / PySpark** – Data processing and machine learning workflows
- **Pandas and NumPy** – Data manipulation and numerical operations, where applicable
- **Scikit-learn** – Model evaluation and supporting machine learning utilities, where applicable
- **Google Colab / Kaggle** – Notebook-based development and experimentation

## Methodology

### 1. Data Preparation
- Loaded and explored the AI4I 2020 dataset.
- Examined data quality and class distribution.
- Prepared relevant sensor features for model training.
- Excluded identifier and failure-mode fields that could introduce target leakage.

### 2. Exploratory Data Analysis
- Analyzed sensor measurements and their distributions.
- Examined the imbalance between normal operating records and machine failures.
- Identified relevant features for predictive modelling.

### 3. Model Development
The following classification algorithms were compared:

- Logistic Regression
- Decision Tree
- Random Forest

Models were trained and evaluated using a consistent experimental workflow. Random Forest was selected based on validation performance, considering F2-score and precision-recall AUC.

### 4. Model Evaluation
The selected model was evaluated on a held-out test set using accuracy, precision, recall, F1-score, F2-score, ROC-AUC, and PR-AUC.

Failure detection was given particular attention because missing an actual machine failure can be costly.

## Results

The Random Forest model achieved the following reported test results:

| Metric | Score |
|---|---:|
| Accuracy | 97.93% |
| Precision | 69.09% |
| Recall | 74.51% |
| F1-score | 71.70% |
| F2-score | 73.36% |
| ROC-AUC | 0.9854 |
| PR-AUC | 0.7871 |

The results indicate strong overall classification performance, while the recall score reflects the model's ability to identify actual machine failures.

## Key Learnings

- Applying PySpark to data-processing and machine learning workflows.
- Comparing classification algorithms using validation data.
- Understanding class imbalance in industrial failure prediction.
- Evaluating models using metrics beyond accuracy.
- Using precision-recall metrics to assess failure detection.

## Repository Contents

- `Predictive_Maintenance_BDA (1).ipynb` – Notebook containing the project implementation and experiments.

## How to Run

1. Clone or download this repository.
2. Open the notebook in Google Colab or a compatible Jupyter environment.
3. Download the AI4I 2020 Predictive Maintenance Dataset from the UCI Machine Learning Repository.
4. Upload the dataset or configure the notebook to access its location.
5. Install any missing dependencies required by the notebook.
6. Execute the notebook cells in sequence to reproduce the analysis and experiments.

## Future Improvements

- Explore additional classification algorithms and hyperparameter tuning.
- Investigate methods for improving failure detection while controlling false alarms.
- Evaluate the model on additional industrial datasets.
- Explore deployment as a predictive maintenance monitoring application.

## Author

**Tejaswini Palutla**

B.Tech, Computer Science and Engineering  
Amrita Vishwa Vidyapeetham, Amaravati Campus

[GitHub Profile](https://github.com/STejaswiniP)
