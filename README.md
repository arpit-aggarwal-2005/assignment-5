##SVM Optimization on UCI Dataset
This repository presents a project on optimizing Support Vector Machines (SVM) for a multi-class classification problem using a dataset from the UCI Machine Learning Repository. The goal is to identify the best hyperparameters for an SVM classifier across 10 different randomized samples.

#📊 Dataset Used
Letter Recognition dataset from UCI:

Features: 16 numerical attributes
Target: 26 capital letters (A-Z)
Total Samples: 20,000
#🔧 Methodology
Dataset Selection & Preprocessing:

StandardScaler applied to features for normalization.
Sampling:

Data split into training (70%) and testing (30%) using 10 random seeds.
Model Optimization:

Optimized NuSVC with 100 random combinations of:
kernel = ['linear', 'rbf', 'poly']
nu from 0.1 to 0.9
epsilon from 0.01 to 0.2
Best accuracy and parameters were recorded per sample.
Evaluation:

Accuracy recorded over iterations
Convergence graph plotted for the sample with the highest accuracy
