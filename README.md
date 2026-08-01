# CIFAR-10 Image Classification Using Transfer Learning and ResNet50

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Model](https://img.shields.io/badge/Model-ResNet50-darkblue)
![Dataset](https://img.shields.io/badge/Dataset-CIFAR--10-green)
![Task](https://img.shields.io/badge/Task-Image%20Classification-purple)
![Test Accuracy](https://img.shields.io/badge/Test%20Accuracy-65.03%25-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## Project Overview

This project applies transfer learning with ResNet50 to classify CIFAR-10 images into 10 object categories:

- airplane
- automobile
- bird
- cat
- deer
- dog
- frog
- horse
- ship
- truck

The goal was not only to build a working image-classification model, but also to understand the complete computer-vision pipeline, including exploratory data analysis, preprocessing, transfer learning, fine-tuning, evaluation, and error analysis.

---

## Why CIFAR-10 Is Challenging

CIFAR-10 images are only **32 × 32 pixels**, which limits visual detail and makes some categories difficult to distinguish.

Commonly confused class pairs include:

- cat vs dog
- deer vs horse
- automobile vs truck
- ship vs airplane

The small image size and similarity between classes make generalization an important challenge.

---

## Exploratory Data Analysis

The exploratory analysis examined:

- dataset size and image dimensions
- class distribution
- sample images
- RGB-channel statistics
- image-quality limitations

![EDA Summary](assets/eda_summary.png)

### Main EDA Findings

- The dataset contains 10 classes.
- Images have the shape `32 × 32 × 3`.
- The selected 10,000-image training subset is approximately balanced.
- Pixel values cover the full range from 0 to 255.
- Low image resolution makes fine details difficult to distinguish.

---

## Overall Pipeline

```text
Data Loading
      ↓
Exploratory Data Analysis
      ↓
Preprocessing
      ↓
Train / Validation / Test Split
      ↓
ResNet50 Base Model
      ↓
Custom Classification Head
      ↓
Frozen-Base Training
      ↓
Fine-Tuning
      ↓
Evaluation and Interpretation
