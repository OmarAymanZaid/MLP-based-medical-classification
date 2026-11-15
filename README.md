# MLP-based medical classification

Reimplementation and experimental evaluation of an MLP-based medical classification model, based on the paper:

**Stroke Prediction using Clinical and Social Features in Machine Learning**  
Aidan Chadha (2025) — [arXiv:2501.00048](https://arxiv.org/abs/2501.00048)

## Overview

This project reproduces a Multi-Layer Perceptron (MLP) model for predicting stroke occurrence from clinical and demographic features.

The work follows the original paper's approach, evaluates the model on its original dataset, and investigates its generalization to a different medical tabular dataset. We also compare it against a simple baseline and experiment with improvements to the original architecture and training procedure.

## Project Objectives

- Reimplement the paper's MLP architecture and training configuration.
- Reproduce and evaluate the reported results on the original dataset.
- Apply the model to a different medical classification dataset.
- Compare the MLP against a simple baseline using consistent data splits.
- Experiment with improvements and evaluate their impact.

## Model Architecture

The paper's MLP consists of:

| Layer | Configuration |
|---|---|
| Input | 10 features |
| Hidden 1 | 128 neurons |
| Hidden 2 | 64 neurons |
| Hidden 3 | 32 neurons |
| Output | 2 classes |

Each hidden layer uses Batch Normalization, ReLU activation, and Dropout (0.3).

**Reported training configuration:**
- Optimizer: Adam
- Learning rate: 0.01
- Batch size: 32
- Epochs: 400
- Loss: Weighted Cross-Entropy

The implementation may include documented adjustments where necessary, particularly to introduce a validation set and prevent test-set leakage.

## Datasets

### Original Dataset

[Stroke Prediction Dataset — Kaggle](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

Used to reproduce the original paper's experiment.

### New Dataset

A separate public medical tabular classification dataset will be selected for evaluating the model's generalization.

The selected dataset must be different from the original paper's dataset and satisfy the project's dataset requirements.

*Dataset name and source: To be added.*

## Experimental Work

The project is organized around the following experiments:

1. **Paper Reproduction:** Implement and evaluate the original MLP.
2. **New Dataset Evaluation:** Adapt and train the model on the selected dataset.
3. **Baseline Comparison:** Compare against a simpler classification model using the same data splits.
4. **Model Improvements:** Investigate selected modifications, such as weight decay, learning-rate scheduling, early stopping, or alternative approaches to class imbalance.

All model selection and hyperparameter tuning are performed using the validation set. The test set is reserved for final evaluation.

## Evaluation

Classification performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Training and validation loss curves are also used to examine model convergence and potential overfitting.

For bonus experiments, selected configurations are evaluated across three random seeds, with results reported as mean and standard deviation.

## Repository Structure

```text
.
├── data/                   # Dataset files (not necessarily tracked)
├── notebooks/              # Exploration and experiments
├── src/                    # Model and training implementation
├── results/                # Metrics, plots, and experiment outputs
├── requirements.txt
└── README.md
```

*The structure may evolve as implementation progresses.*

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd <repository-name>
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Prepare the datasets

Download the datasets from their respective sources and place them in the expected data directories.

Refer to the dataset preparation instructions in the relevant notebook or source files.

### 4. Run the experiments

Follow the execution instructions provided in the notebooks or scripts.

## Results

Results, comparisons with the original paper, baseline performance, and experimental improvements will be documented here once the experiments are completed.

## Team

Developed as a Deep Learning course project at the Faculty of Computers and Artificial Intelligence, Helwan University.

*Team members and individual contributions: To be added.*
