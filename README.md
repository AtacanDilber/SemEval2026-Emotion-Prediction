# SemEval2026-Task 2: Predicting Variation in Emotional Valence and Arousal over Time from Ecological Essays


This repository presents a Transformer-based regression system developed for **SemEval-2026 Task 2 (Subtask 1)**.  
The task focuses on predicting continuous emotional **valence** and **arousal** values from ecological essays, modeling emotions on continuous dimensions rather than discrete emotion categories.

---

## Project Overview

Traditional emotion classification relies on fixed labels (e.g., happy, sad, angry).  
In contrast, this task models emotions using **continuous valence and arousal scales**, which better capture emotional intensity and variation in real-world text.

This project formulates the task as a supervised regression problem and applies a modern NLP pipeline built on pretrained Transformer models. The system follows the official task setup and evaluation protocol and was developed as part of the CS445 course project.

---

## Methodology

The proposed system is based on the following components:

- **Text Encoder:** RoBERTa
- **Architecture:** Split-head regression model  
  - Shared textual representation  
  - Separate output heads for valence and arousal
- **Loss Function:** Concordance Correlation Coefficient Loss (CCCLoss)
- **Hyperparameter Optimization:** Optuna
- **Training Strategy:** K-Fold cross-validation
- **Evaluation:** Ensemble averaging across folds
- **Metrics:**  
  - Concordance Correlation Coefficient (CCC)  
  - Pearson correlation  
  - Composite score (task-specific)

This design allows the model to capture shared semantic information while learning dimension-specific emotional representations.

---

## Results Summary
The system achieves strong and stable performance under cross-validation, with consistently higher accuracy for **valence** than for **arousal>

Under five-fold cross-validation, the final ensemble achieves a strong average composite score and Pearson correlation, with consistently high>

Detailed quantitative results, analysis, and visualizations are provided in the project report.

---

## Repository Structure

Notebooks/ # Main implementation notebook
Neports/ # Project report (PDF)
Data/ # Dataset folder (not included; see data/README.md)


- The **notebook** contains the full experimental pipeline and model implementation.
- The **report** provides detailed methodology, evaluation, results, and discussion.
- The **data folder** contains instructions only; dataset files are not distributed.

---

## Dataset

The dataset used in this project is provided by the **SemEval-2026 Task 2 organizers** and is **not included** in this repository.

The notebook preserves the original file paths used during development to ensure
consistency with the reported results. Instructions for placing the organizer-
provided CSV files locally are available in: data/README.md


---

## Reproducibility Notes

This repository is intended as a research and learning showcase rather than a
production-ready package.

The implementation notebook has been preserved in its original form and has not
been refactored to avoid unintended changes to the experimental setup. Users are
welcome to adapt file paths, modularize the code, or extend the system for further
experimentation.



