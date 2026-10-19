<div align="center">

# Brain Tumor Segmentation & Classification

### Exploring deep learning for medical image analysis

**U-Net · Attention U-Net · Encoder-Based Classification**

CSE428 — Image Processing | BRAC University

</div>

---

## Overview

Locating a tumor and identifying its class are related but different image-analysis tasks. This project explores both using the **BRISC: Annotated Dataset for Brain Tumor Segmentation and Classification**.

The notebook follows the complete experimental workflow—from inspecting images and masks to training models, evaluating predictions, and visualizing results.

| Task | Objective | Approach |
|---|---|---|
| **Segmentation** | Predict a pixel-level tumor mask | U-Net and Attention U-Net |
| **Classification** | Predict the image's class label | Encoder-based classifier |

## Project Highlights

- Explore class distribution, image properties, and mask coverage.
- Pair source images with their corresponding segmentation masks.
- Prepare preprocessing, augmentation, and train/validation/test splits.
- Implement and compare U-Net and Attention U-Net.
- Train segmentation models with a combined binary cross-entropy and Dice loss.
- Evaluate classification through per-class metrics and a confusion matrix.
- Visualize training behaviour and predicted tumor masks.

## Methodology

### 1. Understand the Data

Inspect the dataset structure, class labels, image dimensions, and foreground-to-background distribution in segmentation masks.

### 2. Prepare the Inputs

Match images with masks, prepare data splits, and apply preprocessing and training-time augmentation.

### 3. Train the Models

**U-Net** provides an encoder–decoder segmentation baseline with skip connections.

**Attention U-Net** introduces attention gates on skip connections to investigate their effect on segmentation performance.

An **encoder-based classifier** addresses the separate image-classification task.

### 4. Evaluate and Inspect

Assess segmentation overlap, examine classification errors, and inspect visual predictions alongside numerical metrics.

## Evaluation

| Task | Metrics and Outputs |
|---|---|
| Segmentation | Dice coefficient, IoU, pixel accuracy |
| Classification | Precision, recall, F1-score, confusion matrix |
| Training analysis | Training and validation curves |
| Qualitative analysis | Images, ground-truth masks, predicted masks |

Saved notebook outputs record the original experiments. A fresh training run may produce different results because of random initialization, hardware, and library versions.

## Technology Stack

| Category | Tools |
|---|---|
| Language | Python |
| Deep learning | PyTorch, torchvision |
| Image processing | OpenCV, Pillow |
| Data handling | NumPy, pandas |
| Evaluation | scikit-learn |
| Visualization | matplotlib |
| Notebook environment | Jupyter / Kaggle |

## Getting Started

### Option A — Kaggle

The notebook was developed using Kaggle-style dataset paths.

1. Upload `cse-428-final-project.ipynb` to Kaggle.
2. Attach the BRISC dataset.
3. Enable a GPU for training.
4. Update the dataset base path to match its location.
5. Run the notebook cells sequentially.

### Option B — Local Environment

Clone the repository:

```bash
git clone https://github.com/Alokamit310/Brain-Tumor-Segmentation-Classification.git
cd Brain-Tumor-Segmentation-Classification
```

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open `cse-428-final-project.ipynb` and update its dataset paths before execution. GPU acceleration is recommended for training.

### Dataset and Checkpoints

The dataset and trained weights are not included in this repository.

- Obtain BRISC from its original source.
- Preserve the image, mask, and manifest structure expected by the notebook.
- Update the notebook's paths to your dataset location.
- Run the training cells to generate checkpoints before running evaluation cells that load them.

## Repository Contents

| File | Purpose |
|---|---|
| `cse-428-final-project.ipynb` | Data exploration, model implementation, training, and evaluation |
| `requirements.txt` | Python dependencies |
| `.gitignore` | Excludes local datasets, checkpoints, and environment files |
| `README.md` | Project overview and execution instructions |

## Learning Focus

The project examines practical questions in medical image analysis:

- How do segmentation and classification require different evaluation methods?
- How does an attention-based architecture compare with a standard U-Net?
- What do overlap metrics reveal that pixel accuracy alone may miss?
- Where do visual predictions expose errors hidden by aggregate scores?

## Scope and Limitations

This is an academic implementation and evaluation of established architectures.

Results describe the dataset and experimental setup used in the notebook. They do not establish clinical reliability or generalization to other hospitals, scanners, or patient populations.

The project is intended for learning and experimentation, not clinical diagnosis.

---

<div align="center">

**Developed as part of CSE428 — Image Processing**  
**BRAC University**

</div>