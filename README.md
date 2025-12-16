# Brain-Computer-Interface (BCI) — Motor Imagery Classification

[![Python](https://img.shields.io/badge/Python-3.9+-blue)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red)]()
[![EEG](https://img.shields.io/badge/EEG-Motor%20Imagery-green)]()
[![License](https://img.shields.io/badge/License-MIT-yellow)]()

## Overview

This repository contains research code for **Motor Imagery (MI) classification in Brain–Computer Interfaces (BCI)** using modern deep learning approaches. The project focuses on robust feature learning from EEG signals and improving classification performance across subjects.

**Key goals**:

* Reliable MI classification from multi-channel EEG
* Subject-independent / cross-subject generalization
* Reproducible experiments with clean training pipelines

---

## Highlights

* End-to-end EEG preprocessing → model training → evaluation
* Support for classical ML baselines and deep learning models
* Modular design for experimenting with architectures
* Clear evaluation using accuracy, confusion matrices, and learning curves

---

## Dataset

Supported datasets (or planned support):

* BCI Competition IV (2a / 2b)
* PhysioNet MI EEG Dataset

> ⚠️ Datasets are **not included** due to license restrictions. Scripts assume raw EEG files placed in `data/raw/`.

---

## Methodology

1. **Signal Preprocessing**

   * Band-pass filtering
   * Artifact handling
   * Epoch extraction

2. **Feature Learning**

   * Time-domain and frequency-domain representations
   * CNN-based spatial–temporal feature extraction

3. **Classification**

   * Deep neural networks (CNN-based)
   * Optional classical baselines (SVM, LDA)

---

## Repository Structure

```
Brain-Computer-Interface/
│── README.md
│── requirements.txt
│── data/
│   ├── raw/          # Original EEG files (not included)
│   ├── processed/    # Preprocessed EEG epochs
│
│── src/
│   ├── preprocessing.py
│   ├── dataset.py
│   ├── models.py
│   ├── train.py
│   ├── evaluate.py
│   └── utils.py
│
│── notebooks/
│   ├── exploratory_analysis.ipynb
│   └── training_demo.ipynb
│
│── results/
│   ├── confusion_matrix.png
│   ├── training_curves.png
│
│── experiments/
│   └── config.yaml
```

---

## Installation

```bash
git clone https://github.com/AbirDas-5151/Brain-Computer-Interface.git
cd Brain-Computer-Interface
pip install -r requirements.txt
```

---

## Usage

### Preprocessing

```bash
python src/preprocessing.py --input data/raw --output data/processed
```

### Training

```bash
python src/train.py --config experiments/config.yaml
```

### Evaluation

```bash
python src/evaluate.py --checkpoint checkpoints/model.pth
```

---

## Results

| Model  | Accuracy | Notes                    |
| ------ | -------- | ------------------------ |
| CNN-MI | XX%      | Cross-subject evaluation |

> Replace `XX%` with your best verified result.

---

## Research Context

This repository supports ongoing and published research in **EEG-based Motor Imagery analysis** and explainable AI for neural signals.

If you use this code in academic work, please cite appropriately.

---

## Future Work

* Transformer-based EEG encoders
* Self-supervised pretraining for EEG
* Explainability (Grad-CAM for EEG)
* Real-time inference pipeline

---

## Author

**Abir Das**
AI Researcher | Computer Vision & Biomedical AI

---

## License

This project is licensed under the MIT License.
