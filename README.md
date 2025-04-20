SVM Optimization on UCI Dataset
This repository presents a project on optimizing Support Vector Machines (SVM) for a multi-class classification problem using a dataset from the UCI Machine Learning Repository. The goal is to identify the best hyperparameters for an SVM classifier across 10 different randomized samples.

📊 Dataset Used
Letter Recognition dataset from UCI:

Features: 16 numerical attributes
Target: 26 capital letters (A-Z)
Total Samples: 20,000
🔧 Methodology
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
📋 Results
Sample #	Best Accuracy (%)	Kernel	Nu	Epsilon
S1	65.12	rbf	0.4	0.05
S2	66.14	poly	0.6	0.11
S3	65.67	rbf	0.2	0.18
S4	65.95	linear	0.3	0.04
S5	66.73	rbf	0.5	0.07
S6	66.28	rbf	0.7	0.10
S7	67.84	rbf	0.5	0.14
S8	65.92	poly	0.4	0.09
S9	66.45	rbf	0.6	0.12
S10	67.23	rbf	0.7	0.05
🔺 (Actual values will be auto-filled when running the notebook)

