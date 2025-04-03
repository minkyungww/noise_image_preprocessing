# Noise-Aware Image Preprocessing for Animal Classification

This repository contains code and resources for **image data preprocessing** as part of the term project for the course **DS801: Data Engineering for Big Data Analytics** at KAIST.

## 📘 Project Description

The goal of this project is to **verify and evaluate preprocessing techniques for noisy image data** in the context of a **10-class animal classification task**. The original dataset contains over 31,000 raw animal images (64x64 JPEG) and suffers from several critical data quality issues:

- ❗ **Out-of-distribution (OOD) images**: irrelevant, non-animal data
- 🔄 **Noisy labels**: mislabeling introduced intentionally to simulate real-world scenarios
- ⚖️ **Class imbalance**: uneven number of samples per class

These challenges must be addressed through preprocessing and cleaning in order to improve model performance.

## 🧪 Objective

This code is intended to:

- **Detect and remove outlier images** using image embeddings
- **Correct mislabeled images** via relabeling techniques
- **Handle class imbalance** through data augmentation and oversampling

The final goal is to train a **ResNet-34 model from scratch** (without pretrained weights) and achieve robust performance on a clean test set through these preprocessing strategies.

## 🛠 Dataset

- 📦 **Input**: 31,848 raw images (10 animal classes)
- 📁 **Format**: `img_{uuid}.jpg`, with labels in a `data-labels.json` file (one-hot encoded)
- 🎯 **Target**: Improve the quality of this data for training and create your own clean validation set

More details available in the official dataset link (provided via KLMS or instructor).

## 🧼 Preprocessing Techniques

- **Outlier Detection**: Using pre-trained CNN embeddings to identify and remove OOD samples
- **Label Correction**: Apply relabeling strategies (e.g., self-training, clustering, confidence-based correction)
- **Augmentation & Oversampling**: Techniques like Mixup, rotation, cropping applied to minority classes

All steps follow filename and label format rules provided in the project guidelines.


## 🧑‍🏫 Course & Team

- 📚 **Course**: DS801 - Data Engineering for Big Data Analytics
- 🧑‍💻 Project by Team MacGyver at KAIST, Spring 2024

## 📈 Final Goal

To submit a cleaned training dataset and a new validation set, which together improve the balanced accuracy of a ResNet-34 model trained from scratch, as evaluated on a hidden clean test set.

---

For more details on the project setup and evaluation, refer to the guideline [DS801-TermProjects.pdf].
