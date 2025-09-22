# Student-Performance 

📘 Student Performance Prediction
📌 Project Overview

This project focuses on analyzing and predicting student exam performance using Python (Pandas, Matplotlib, Scikit-learn).
It explores both Supervised Learning and Unsupervised Learning approaches to gain insights into how study hours and related factors affect student scores.

🛠 Tools & Libraries
Python
Pandas & NumPy – Data manipulation
Matplotlib & Seaborn – Data visualization
Scikit-learn – Machine Learning models & evaluation

📊 Dataset
Source: Student Performance Dataset (Kaggle)
Features: Hours of study, Scores (and optionally other factors like participation, sleep, etc.)
Target (engineered): Pass/Fail (Scores ≥ 50 → 1, else 0)

🔎 Steps & Workflow
1. Data Cleaning & EDA
Handled missing values and duplicates
Explored distributions with histograms, boxplots, pairplots
Checked correlations between features with heatmaps

2. Supervised Learning (Classification & Regression)
Models tried:
Logistic Regression
Decision Tree
Random Forest
SVM
KNN
Naive Bayes

Metrics: Accuracy, Precision, Recall, F1-score, ROC, AUC
⚠️ Finding: Artificial target (Pass/Fail) caused overfitting, accuracy looked perfect but not realistic.
3. Unsupervised Learning (Clustering)
KMeans Clustering
Hierarchical Clustering
Evaluated using Silhouette Score

Results:
KMeans Silhouette = 0.68
Hierarchical Silhouette = 0.61
KMeans proved more stable & consistent across train/test splits.

4. Bonus Exploration
Polynomial Regression to capture non-linear patterns
Experimented with adding/removing features to test model sensitivity

📈 Results
Model	Metric	Score
Logistic Regression	Accuracy (misleading)	100%
KMeans	Silhouette Score	0.68
Hierarchical	Silhouette Score	0.61

Key Takeaway:
Supervised methods were not ideal due to the lack of a natural target variable.
Unsupervised (KMeans) provided more meaningful insights for clustering students’ performance.

📂 Project Structure
├── data/                # Dataset (CSV)
├── notebooks/           # Jupyter Notebooks
├── models/              # Saved models (pkl files)
├── visuals/             # Plots and figures
├── requirements.txt     # Dependencies
└── README.md            # Project overview

🚀 How to Run
Clone the repo
git clone https://github.com/username/student-performance.git
cd student-performance


Install requirements
pip install -r requirements.txt


Run the notebook
jupyter notebook notebooks/student_performance.ipynb

📝 Conclusion
Supervised learning isn’t reliable here without a real target → risk of overfitting.
Unsupervised clustering, especially KMeans, gave more practical insights.
This project demonstrates EDA, regression, classification, clustering, and evaluation metrics end-to-end.
