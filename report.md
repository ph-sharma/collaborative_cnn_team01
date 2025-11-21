# Cross-Dataset CNN Collaboration: Cats vs Dogs Classification Analysis

## Team Information

**Project Name:** collaborative_cnn_team01  

**Team Members:**  
- Parth Sharma (2025AIZ0010)  
- Shairal Verma (2025AIZ0002)

**GitHub Repository:**  
https://github.com/ph-sharma/collaborative_cnn_team01

**Code Notebooks:**  
- **User 1 Code:** https://github.com/ph-sharma/collaborative_cnn_team01/blob/main/Notebook/train_v1.ipynb  
- **User 1 Testing code of User 2 Dataset:** https://github.com/shairalverma-cmd/testing-repo/blob/main/notebooks/test_v2.ipynb  
- **User 2 Code:** https://github.com/shairalverma-cmd/testing-repo/blob/main/notebooks/train_v2.ipynb  
- **User 2 Testing code of User 1 Dataset:** https://github.com/shairalverma-cmd/testing-repo/blob/main/notebooks/test_v1.ipynb  

---

## Executive Summary

This report summarizes a collaborative experiment involving two CNN models trained on different cat–dog image datasets and evaluated for cross-dataset generalization. The study highlights how dataset characteristics and model architecture influence performance and transferability.

## Methodology

### Datasets
- **User 1** used the "Cat & Dog Dataset (Tong Python)" with 6,404 training and 1,601 validation images.  
- **User 2** used the Kaggle "Dogs vs Cats Redux" dataset with 20,000 training and 5,000 validation images.

### Model Architectures
- **Model V1 (User 1)**
  - Conv2D: 32 → 64 → 64 filters  
  - MaxPooling + Global Average Pooling  
  - Dense(128) → Sigmoid  

- **Model V2 (User 2)**
  - Conv2D: 8 → 16 → 32 filters  
  - 30% Dropout  
  - Global Average Pooling  
  - Dense(32) → Sigmoid  

---

## Results

### Training & Validation Performance

| Model | Dataset | Training Acc | Validation Acc |
|-------|---------|--------------|----------------|
| V1 | User 1 | **66.96%** | **55.96%** |
| V2 | User 2 | **72.58%** | **71.98%** |

### Cross-Dataset Test Performance

| Scenario | Model | From Dataset | To Dataset | Accuracy |
|----------|--------|---------------|------------|-----------|
| Baseline | V1 | User 1 | User 1 | **55.96%** |
| Cross-Test | V1 | User 1 | User 2 | **56.06%** |
| Baseline | V2 | User 2 | User 2 | **71.98%** |
| Cross-Test | V2 | User 2 | User 1 | **71.20%** |

---

## Key Insights

1. **Stable Cross-Dataset Performance**  
   Both models maintained stable accuracy when evaluated on the opposite dataset.

2. **Model V2 Outperformed V1**  
   V2 consistently showed higher accuracy due to better architectural regularization.

3. **Regularization Helps Generalization**  
   Dropout in V2 prevented overfitting, enabling stronger cross-dataset robustness.

---

## Conclusions

- Both models generalized reasonably across datasets with no significant degradation.  
- Model V2’s architecture proved more effective and efficient.  
- Dataset diversity significantly impacts model transferability across domains.

---
