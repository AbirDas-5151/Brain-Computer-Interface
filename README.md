# Brain-Computer-Interface (BCI) — Motor Imagery Classification

[![Python](https://img.shields.io/badge/Python-3.9+-blue)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red)]()
[![EEG](https://img.shields.io/badge/EEG-Motor%20Imagery-green)]()
[![License](https://img.shields.io/badge/License-MIT-yellow)]()

## Overview

This repository contains the **exact experimental implementation** used for **Motor Imagery (MI) classification in Brain–Computer Interface (BCI) systems**. All experiments were conducted in **Google Colab**, and the full experimental notebook is provided for transparency and reproducibility.

The work focuses on learning discriminative representations from multi-channel EEG signals for reliable motor imagery classification using deep learning.

---

## What This Repository Represents

* ✅ A **real research experiment**, not a demo
* ✅ End‑to‑end EEG pipeline: preprocessing → training → evaluation
* ✅ Results generated directly from the provided notebook
* ❌ Not a real‑time BCI system

---

## Experimental Setup

### Platform

* Google Colab (GPU runtime)

### Task

* Motor Imagery EEG classification

### Input

* Multi‑channel EEG signals segmented into trials/epochs

### Output

* Discrete motor imagery class predictions

---

## Dataset

The experiment uses a **public Motor Imagery EEG dataset** commonly employed in BCI research.

⚠️ **Dataset files are not included** due to licensing restrictions.

Expected directory (if re-running locally):

```
data/
└── raw/   # EEG recordings
```

---

## Methodology (As Implemented)

### 1. EEG Preprocessing

* Signal loading
* Channel selection
* Epoch extraction
* Normalization / scaling

### 2. Model Architecture

* Deep learning–based classifier implemented in PyTorch
* Learns spatial–temporal features directly from EEG signals

### 3. Training

* Supervised learning
* Cross‑entropy loss
* Batch‑based optimization

### 4. Evaluation

* Classification accuracy
* Confusion matrix visualization

---

## Repository Structure

This structure mirrors how the experiment was actually conducted.

```
Brain-Computer-Interface/
│── README.md
│── requirements.txt
│
│── notebooks/
│   └── BCI_Motor_Imagery_Experiment.ipynb   # Full Colab experiment
│
│── src/
│   ├── models.py      # Model definition (extracted from notebook)
│   ├── train.py       # Training & evaluation logic
│   └── utils.py       # Helper functions
│
│── results/
│   ├── confusion_matrix.png
│   └── training_curve.png
```

---

## Running the Experiment

### Option 1 — Recommended (Colab)

Open the notebook in Google Colab:

```
notebooks/BCI_Motor_Imagery_Experiment.ipynb
```

Run cells sequentially.

### Option 2 — Local (Optional)

```bash
pip install -r requirements.txt
python src/train.py
```

---

## Results

Representative results from the experiment:

* Motor imagery classification accuracy (see notebook)
* Confusion matrix visualization

All reported results are **generated directly from the provided notebook**.

---

## Research Context

This repository supports academic work in:

* Brain–Computer Interfaces (BCI)
* EEG signal analysis
* Motor Imagery classification

The code is shared to ensure **reproducibility and transparency** of the experiment.

---

## Limitations

* Offline analysis only
* Dataset‑specific evaluation
* No real‑time inference pipeline

---

## Author

**Abir Das**
AI Researcher | Biomedical Signal Processing & Deep Learning

---

## License

MIT License
