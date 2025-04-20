# 🧠 SVM Optimization on UCI Letter Recognition Dataset

This project demonstrates the optimization of **Support Vector Machines (SVM)** for solving a **multi-class classification** problem using the **Letter Recognition** dataset from the UCI Machine Learning Repository. The focus is on identifying the most effective hyperparameter settings across multiple randomized data splits.

---

## 📊 Dataset Overview

- **Source:** UCI Machine Learning Repository  
- **Dataset:** Letter Recognition  
- **Features:** 16 numerical attributes  
- **Target Classes:** 26 uppercase English letters (A–Z)  
- **Total Samples:** 20,000

---

## 🔧 Workflow & Methodology

### 🧼 Data Preprocessing

- The dataset is loaded via `fetch_openml`.
- Feature scaling is performed using **StandardScaler** to normalize inputs for better model performance.

### 🔀 Sampling Strategy

- The dataset is split into **70% training** and **30% testing** sets.
- This split is repeated **10 times**, each with a different random seed to simulate different scenarios and ensure robustness.

### 🔍 Model Optimization

- The model used is **Nu-Support Vector Classification (NuSVC)** from `sklearn.svm`.
- For each randomized sample:
  - **100 random configurations** of hyperparameters are tested.
  - Hyperparameters explored:
    - `kernel`: `['linear', 'rbf', 'poly']`
    - `nu`: from **0.1 to 0.9**
    - `epsilon`: from **0.01 to 0.2**
  - The model is trained and evaluated on the test set.
  - The **best accuracy and corresponding parameters** are stored.

### 📈 Evaluation & Visualization

- Accuracy progression is tracked for each sample.
- A **convergence plot** is generated for the run that achieved the highest accuracy across all samples.

---



