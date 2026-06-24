# Heart Disease Prediction: ML vs. DL Comparative Study

**Author:** Tapiwanashe Gift Marufu  
**Course:** Introduction to Machine Learning

## Project Overview
This repository contains a comprehensive comparative study of classical machine learning and deep learning techniques applied to heart disease prediction using the Cleveland Heart Disease dataset. This project explores the performance gap between classical models (Logistic Regression, SVM, Random Forest) and Deep Neural Networks (Sequential vs. Residual), while conducting a critical audit on data integrity.

## Key Findings
*   **Best Performing Model:** A tuned **Support Vector Machine (SVM)** with an RBF kernel (C=10.0, γ=0.1) achieved the highest performance metrics (Accuracy: 0.9805, Recall: 1.0000, AUC-ROC: 0.9995).
*   **Deep Learning:** The Functional API Residual DNN (Experiment 7) proved to be the most effective deep learning architecture, outperforming the sequential baseline through superior architectural regularisation.
*   **The Duplicate Effect:** A critical audit revealed that 723 of the 1,025 rows in the source dataset were exact duplicates. Re-evaluating the SVM on the deduplicated dataset (302 unique records) resulted in a significant performance drop (Accuracy: 0.8043), demonstrating how duplicate contamination leads to inflated performance metrics.

## Experimental Methodology
The study follows a seven-experiment pipeline, evidence-driven and sequential:
1.  **LR Baseline:** Logistic Regression with L2 regularization.
2.  **LR Sparsity:** Logistic Regression with L1 regularization.
3.  **SVM Baseline:** SVM with RBF kernel (default).
4.  **SVM Optimization:** GridSearch-tuned SVM.
5.  **Random Forest:** Constrained tree ensemble for feature importance.
6.  **Sequential DNN:** Baseline fully connected network.
7.  **Residual DNN:** Functional API network with skip connections and BatchNormalization.

## Project Resources
*   **[Google Colab Notebook](https://colab.research.google.com/drive/15-TcgMS1ZrUKiN60j_NWNwAAwE3eKZep?usp=sharing)**: Access the full implementation, training pipelines, and robustness checks.
*   **[Full Research Report (Google Docs)](https://docs.google.com/document/d/1IbAj7Yt13VGKcQ-XyoSa1DE8-Xx175vyUJfRSOB2GrQ/edit?usp=sharing)**: Access the complete methodology, comparative analysis, and discussion.

## Dataset
*   **Source:** [Kaggle Heart Disease Dataset](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)
*   **Description:** 1,025 rows, 14 clinical features.
*   **Note:** The dataset contains significant duplicate rows; this project includes a specific robustness check to quantify the impact of this data quality issue.

## References
This study builds upon foundational work in medical machine learning:
*   Detrano, R., et al. (1989). "International application of a new probability algorithm for the diagnosis of coronary artery disease." *American Journal of Cardiology*.
*   Grinsztajn, L., et al. (2022). "Why tree-based models still outperform deep learning on tabular data." *NeurIPS*.
*   He, K., et al. (2016). "Deep residual learning for image recognition." *CVPR*.
*   Vapnik, V. N. (1995). *The Nature of Statistical Learning Theory*.
