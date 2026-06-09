# Brain Tumor Classification: CNN vs. KNN

## Overview
This repository contains a Jupyter Notebook (`fMRI_Image_Analysis.ipynb`) that evaluates two different machine learning approaches for classifying brain tumors from MRI scans: a Convolutional Neural Network (CNN) and a K-Nearest Neighbors (KNN) model utilizing Histogram of Oriented Gradients (HOG) features. The project categorizes scans into four classes: glioma, meningioma, pituitary tumor, and no tumor.
* All models were trained over an fMRI dataset imported from Kaggle.com:
  https://www.kaggle.com/datasets/deeppythonist/brain-tumor-mri-dataset?resource=download

## Key Findings & The Accuracy Paradox
The results of this study highlight a classic example of the "Accuracy Paradox" in medical imaging and imbalanced datasets:

* **CNN Performance:** Achieved 96.0% accuracy with an Area Under the Curve (AUC) of 0.99–1.00. The deep learning architecture successfully extracted the complex spatial features required to distinctly separate the tumor classes from healthy tissue.
* **KNN Performance:** Achieved a deceptively high 97.7% accuracy, but an AUC of only ~0.50. The ROC analysis revealed that the KNN model had almost no genuine predictive power; it simply defaulted to predicting the majority class due to severe dataset imbalance.

This stark contrast emphasizes the danger of relying solely on raw accuracy metrics and proves the superiority of the CNN architecture for this clinical diagnostic task.

## Repository Contents
* `fMRI_Image_Analysis.ipynb`: The main notebook containing the data processing, model training, evaluation metrics, and ROC curve visualizations.
