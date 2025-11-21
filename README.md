# Collaborative CNN Team Project: Cats vs Dogs Classification

## Project Overview

This repository contains a collaborative machine learning project focused on binary image classification for cats and dogs. Two separate Users developed **Convolutional Neural Network (CNN)** models on different datasets to evaluate training performance and cross-dataset generalization.

## Project Structure

├── models/ # Trained model files (.h5)
├── notebooks/ # Jupyter notebooks for training/testing
│ ├── train_v1.ipynb
│ ├── train_v2.ipynb
│ ├── test_v1.ipynb
│ └── test_v2.ipynb
├── results/ # Training/validation/test metrics
├── data/ # Dataset directories (manual download)
│ ├── user1/ # Dataset for User 1
│ └── user2/ # Dataset for User 2
├── report.md # Detailed analysis
├── requirements.txt # Dependencies
└── readme.md # This file

### Main Libraries

* **TensorFlow/Keras**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Scikit-learn**

---

## Usage Instructions

### 1. Train Models

Run the following notebooks in your Jupyter environment:

* `train_v1.ipynb` (Trains the *User 1 model*)
* `train_v2.ipynb` (Trains the *User 2 model*)

### 2. Test Models

Perform cross-dataset generalization tests:

* `test_v1.ipynb` — Model **V1** (trained on User 1 data) is tested on the *User 2 dataset*.
* `test_v2.ipynb` — Model **V2** (trained on User 2 data) is tested on the *User 1 dataset*.

### 3. View Results

* Training and validation metrics are stored in the `results/` directory.
* Full detailed analysis and project conclusions are available in `report.md`.

---

## Results Summary

The table below shows the performance of the models, highlighting cross-dataset generalization:

| Model | Trained On | Tested On | Accuracy |
| :---: | :---: | :---: | :---: |
| **V1** | User 1 | User 1 | **55.96%** |
| **V1** | User 1 | User 2 | **56.06%** |
| **V2** | User 2 | User 2 | **71.98%** |
| **V2** | User 2 | User 1 | **71.20%** |

### Files in results/ Directory

* `metrics_v1.json` — Train/validation metrics for V1
* `metrics_v2.json` — Train/validation metrics for V2
* `test_v1_user2.json` — V1 tested on User 2 dataset
* `test_v2_user1.json` — V2 tested on User 1 dataset

---

## Notebooks Overview

| Notebook Name | Description |
| :--- | :--- |
| `train_v1.ipynb` | CNN development and training by User 1. |
| `train_v2.ipynb` | CNN development and training by User 2. |
| `test_v1.ipynb` | Cross-test: Evaluating Model V1 on external data. |
| `test_v2.ipynb` | Cross-test: Evaluating Model V2 on external data. |

---

## Contribution History (Pull Requests)

List of contributions via these pull requests:

* **User 1 - Initial Model Submission:** [https://github.com/ph-sharma/collaborative_cnn_team01/pull/1](https://github.com/ph-sharma/collaborative_cnn_team01/pull/1)
* **User 2 - Initial Model Submission:** [https://github.com/ph-sharma/collaborative_cnn_team01/pull/3](https://github.com/ph-sharma/collaborative_cnn_team01/pull/3)
* **User 1 - Update/Refinement:** [https://github.com/ph-sharma/collaborative_cnn_team01/pull/4](https://github.com/ph-sharma/collaborative_cnn_team01/pull/4)

---