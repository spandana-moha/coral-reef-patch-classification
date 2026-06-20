# Coral Patch Classification using Deep Learning

## Project Overview

This project focuses on automated coral reef benthic classification using deep learning and computer vision techniques. Instead of performing classification on entire underwater reef images containing multiple coral categories, an annotation-guided patch extraction pipeline was developed to generate single-label image patches for supervised learning.

The dataset was constructed using expert-provided coral annotations and coordinate information. Image patches of size 224×224 pixels were extracted around annotation points and balanced across six major benthic classes:

* Crustose Coralline Algae (CCA)
* Macroalgae
* Off
* Porites
* Sand
* Turf

A ResNet18 convolutional neural network was trained on 60,000 balanced coral patches and achieved a validation accuracy of 82.38%.

## Key Results

* Dataset Size: 60,000 image patches
* Number of Classes: 6
* Patch Resolution: 224×224
* Model: ResNet18
* Validation Accuracy: 82.38%
* Macro F1 Score: 81.79%

## Methodology

1. Coral annotation preprocessing
2. Top-class selection based on annotation frequency
3. Annotation-guided patch extraction
4. Dataset balancing
5. Data augmentation and preprocessing
6. ResNet18 transfer learning
7. Model evaluation using confusion matrix and classification metrics

## Results

The trained model demonstrated strong performance across most coral categories, with particularly high recall for Porites, Sand, and Off classes. The primary challenge remained distinguishing Crustose Coralline Algae from Turf and Sand due to visual similarity.

## Technologies Used

* Python
* PyTorch
* OpenCV
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook
