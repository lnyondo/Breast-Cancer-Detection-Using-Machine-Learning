# Breast-Cancer-Detection-Using-Machine-Learning
## Project Overview
This project applies a K‑Nearest Neighbors (KNN) classifier to the UCI Breast Cancer Wisconsin (Original) dataset to detect benign versus malignant tumors based on numeric cytology features. The dataset includes 699 samples and 10 predictors (e.g., clump thickness, uniformity of cell size/shape, marginal adhesion, bare nuclei, mitoses) plus a binary class label.

### Methods
Converted all features to numeric format and replaced missing values coded as "?" with a sentinel value for later handling.

Performed exploratory analysis with describe() and info() to summarize feature distributions and confirm data types and non‑null counts.​

Split the data into training and test sets using a 70/30 split.

Trained a KNN classifier (n_neighbors=5) on the training set and evaluated performance on the held‑out test set using accuracy, precision, recall, F1‑score, and a confusion matrix.

Assessed model robustness with 5‑fold cross‑validation on the full dataset, using accuracy as the scoring metric.​

### Results
Test‑set performance:

- Accuracy: 0.9809

- Precision (malignant): 0.9722

- Recall (malignant): 0.9722

- F1‑score (malignant): 0.9722

Confusion matrix:
|                  | Predicted Benign   | Predicted Malignant |
| ---------------- | ------------------ | ------------------- |
| Actual Benign    | 136 (true benign)  | 2 (false positive)  |
| Actual Malignant | 2 (false negative) | 70 (true malignant) |

5‑fold cross‑validation:

- Fold accuracies: [0.9286, 0.9500, 0.9786, 0.9929, 0.9856]

- Mean CV accuracy: 0.9671.

### Interpretation and Clinical Relevance
The KNN model correctly classifies the vast majority of cases and achieves a strong balance between precision and recall for malignant tumors, suggesting that it can reliably flag most cancers while limiting false alarms. In a clinical setting, such a model is best viewed as a decision‑support tool: it could help prioritize cytology samples for expert review and highlight higher‑risk cases for further work‑up, while final diagnosis remains grounded in cytopathology, imaging, and clinician judgment.

### Project Documents
[Breast cancer Detection_B.pdf](https://github.com/user-attachments/files/25224703/Breast.cancer.Detection_B.pdf)

[Breast cancer Detection Report.pdf](https://github.com/user-attachments/files/25224720/Breast.cancer.Detection.Report.pdf)

