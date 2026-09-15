# Screening Wine Quality with K-Nearest Neighbors

## Overview
This repository contains the deliverable for Assignment 1: an independent, end-to-end
machine-learning workflow applied to the UCI Wine Quality (white wine) dataset. The
assignment builds on the Week 0 lab by moving from "recognize and run a given model"
to "make and justify your own modeling choices" — covering representation, model
selection, evaluation, and generalization using K-Nearest Neighbors (KNN).

**Learning outcomes addressed:** LO1, LO2, LO6, LO8

## Assignment Scenario
Using physicochemical measurements of white wine samples, the task is to predict a
binarized quality label:

- **0 (lower quality):** original quality score ≤ 5
- **1 (higher quality):** original quality score > 5

The workflow includes data preparation, an 80/20 train-test split, model fitting with
KNN, evaluation, and interpretation of how modeling choices (e.g., feature scaling,
choice of *k*, distance metric) affect results.

## Repository Contents
| File | Description |
|---|---|
| `<lastname>_<firstname>_assignment1.ipynb` | Main deliverable — a single reproducible Jupyter notebook containing each assignment question (as a Markdown cell), the corresponding code/analysis, and written responses. |
| `data/` | Cleaned course copy of the UCI Wine Quality (white wine) dataset (if provided/stored locally). |
| `README.md` | This file. |

## Requirements
- Python 3.x
- Jupyter Notebook / JupyterLab
- Libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `scikit-learn`

Install dependencies with:
```bash
pip install numpy pandas matplotlib scikit-learn
```

## How to Run
1. Clone or download this repository.
2. Ensure the wine quality dataset file is placed in the expected data path referenced
   at the top of the notebook.
3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
4. Open `<lastname>_<firstname>_assignment1.ipynb` and run all cells top to bottom.

## Methodology Notes
- **Train/test split:** 80% training, 20% test.
- **Model selection:** Performed using only the training set (e.g., cross-validation);
  the held-out test set is *not* used for model selection, only for final evaluation.
- **Model:** K-Nearest Neighbors (`scikit-learn`'s `KNeighborsClassifier`).
- **Target:** Binary quality label derived from the original quality score.