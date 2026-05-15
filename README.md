Name: Faisal Khan
Enrollment: 01-131232-105
Faculty: Engr. Saad Mazhar Khan

# AI Lab 15: KNN Medical Diagnosis System

This repository contains the complete implementation of **Lab 13: K-Nearest Neighbors (KNN)** focused on medical diagnostics, specifically evaluating a classification pipeline for breast cancer data. 

## 🚀 Project Overview
The objective of this lab is to understand the behavioral shifts of the KNN classifier under various hyperparameter configurations, feature spaces, and data scaling conditions. In a medical diagnostic system, optimizing for statistical metrics like **Recall** takes absolute clinical priority to avoid life-threatening False Negatives.

---

## 🛠️ Tasks Completed

### Task 1: Performance Shift Without Scaling
* **Objective:** Evaluate the impact of unscaled data on a distance-based algorithm.
* **Insight:** Accuracy shifts when data normalization is omitted because features with larger numerical ranges completely dominate the Euclidean distance metrics, drowning out smaller but critical inputs.

### Task 2: Hyperparameter Tuning (Distance Weights & Manhattan Metric)
* **Objective:** Tune the classifier using `weights='distance'` and Manhattan Distance ($p=1$).
* **Insight:** Assigning weight inversely proportional to distance gives closer neighbors a higher impact, while the Manhattan metric offers robust defense against data outliers.

### Task 3: Clinical Optimization (Minimizing False Negatives)
* **Objective:** Loop through values of $K$ ($3, 5, 7, 9, 11$) to identify the safest configuration for a hospital.
* **Insight:** Prioritized **Recall** over Precision. Identified that higher $K$ values optimized the system to miss the minimum number of active medical cases (Lowest False Negatives).

### Task 4: Feature Dimensionality Reduction
* **Objective:** Slice the feature space down to a simplified 2-feature matrix `[:, :2]`.
* **Insight:** Dropping indicators caused a massive drop in overall accuracy. Proven that over-simplifying high-dimensional medical features creates an unsafe diagnostic environment.

---

## 💻 Tech Stack & Dataset
* **Language:** Python 3.14
* **Libraries:** `pandas`, `scikit-learn`
* **Dataset:** Built-in Scikit-Learn Breast Cancer Dataset
