# CIFAR-10 Image Classification Using Transfer Learning and ResNet50

![Project Title](assets/title_slide.png)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Model](https://img.shields.io/badge/Model-ResNet50-darkblue)
![Dataset](https://img.shields.io/badge/Dataset-CIFAR--10-green)
![Task](https://img.shields.io/badge/Task-Image%20Classification-purple)
![Test Accuracy](https://img.shields.io/badge/Test%20Accuracy-65.03%25-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## Project Overview

This project applies transfer learning with ResNet50 to classify CIFAR-10 images into 10 object categories.

The main goal was to build a complete computer-vision pipeline and understand the reasoning behind data exploration, preprocessing, model design, training, fine-tuning, evaluation, and error analysis.

---

## Why CIFAR-10 Is Challenging

![Why CIFAR-10 Is Challenging](assets/why_cifar10_is_challenging.png)

CIFAR-10 images are only **32 × 32 pixels**, which limits fine visual detail. Some categories are also visually similar, such as:

- cat vs dog
- deer vs horse
- automobile vs truck
- ship vs airplane

These similarities make classification and generalization more difficult.

---

## Overall Pipeline

![Overall Pipeline](assets/overall_pipeline.png)

The complete workflow was:

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
