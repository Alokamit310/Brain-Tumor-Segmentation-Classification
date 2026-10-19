# Brain Tumor Segmentation and Classification

A CSE428: Image Processing course project at BRAC University, exploring deep learning for brain tumor segmentation and classification using the BRISC dataset.

## Overview

The project investigates two tasks:

- Segmentation: identifying tumor regions in an image.
- Classification: predicting the image's class label.

The notebook implements U-Net and Attention U-Net for segmentation, along with an encoder-based classifier.

## Workflow

1. Inspect dataset structure and class distribution.
2. Pair images with segmentation masks.
3. Preprocess images and prepare augmentation.
4. Create training, validation, and test splits.
5. Train segmentation models using a combined binary cross-entropy and Dice loss.
6. Evaluate segmentation using Dice, IoU, and pixel accuracy.
7. Train and evaluate an encoder-based classifier.
8. Visualize predictions, training curves, and classification results.

## Technologies

Python, PyTorch, torchvision, OpenCV, NumPy, pandas, matplotlib, and scikit-learn.

## Dataset

BRISC: Annotated Dataset for Brain Tumor Segmentation and Classification.

Dataset files are not included in this repository. Obtain the dataset from its original source and preserve the image, mask, and manifest structure expected by the notebook.

## Running the Notebook

The notebook was developed with Kaggle-style dataset paths.

### On Kaggle

1. Upload the notebook.
2. Attach the BRISC dataset.
3. Enable a GPU for training.
4. Update the dataset base path to match the attached dataset.
5. Run the cells sequentially.

### Locally

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Open Jupyter:

```bash
jupyter notebook
```

Open `cse-428-final-project.ipynb`, update the dataset paths, and run the cells sequentially.

Training cells generate model checkpoints. Evaluation cells that load checkpoints require those files to exist.

## Evaluation

- Segmentation: Dice coefficient, intersection over union, and pixel accuracy.
- Classification: precision, recall, F1-score, and confusion matrix.

Saved notebook outputs document the original experiment. Results from a fresh run may vary with the environment and training randomness.

## Scope and Limitations

This project implements and evaluates established architectures for educational purposes. It is not a clinically validated diagnostic system.

Dataset files and trained model checkpoints are excluded from this repository.