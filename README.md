# Cardiomyocyte-Ageing-Nucleus-Data-Analysis
# Explainable AI Reveals Morphological and Chromatin Biomarkers of Nuclear Ageing

This repository contains the source code used for the study:

**Explainable AI Reveals Morphological and Chromatin Biomarkers of Nuclear Ageing**

The project presents an explainable artificial intelligence framework for automated nuclear ageing classification and biomarker discovery from DAPI-stained fluorescence microscopy images of human induced pluripotent stem cell-derived cardiomyocytes (iPSC-CMs).

---

## Overview

The proposed framework integrates:

- Automated nucleus segmentation
- Quality-controlled single-nucleus extraction
- Vision Transformer (ViT-B/16) classification
- Attention Rollout explainability
- Nuclear morphology analysis
- Chromatin texture (GLCM) analysis
- Statistical biomarker discovery
- Principal Component Analysis (PCA)

The framework identifies quantitative biomarkers associated with nuclear ageing while providing interpretable deep learning predictions.

---

## Repository Structure

```
.
├── data/
│   ├── processed/
│   └── example/
│
├── segmentation/
│   ├── watershed_segmentation.py
│   └── quality_control.py
│
├── models/
│   ├── train_vit.py
│   ├── test_vit.py
│   └── attention_rollout.py
│
├── biomarker_analysis/
│   ├── morphology_features.py
│   ├── glcm_features.py
│   ├── statistical_analysis.py
│   └── biomarker_ranking.py
│
├── figures/
│
├── notebooks/
│
├── requirements.txt
│
└── README.md
```

---

## Dataset

The microscopy images were acquired from cultured human induced pluripotent stem cell-derived cardiomyocytes (iPSC-CMs) at the University of East London Bioscience Laboratory.

The repository contains example data only.

The complete dataset is available through the University of East London Data Repository, subject to institutional data-sharing policies.

---

## Installation

Clone the repository

```bash
git clone https://github.com/datascintist-abusufian/Deep-Spatiotemporal-Modelling-of-Cardiomyocyte-Ageing-Dysfunction.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Pipeline

### 1. Nuclear Segmentation

```bash
python segmentation/watershed_segmentation.py
```

### 2. Quality Control

```bash
python segmentation/quality_control.py
```

### 3. Train Vision Transformer

```bash
python models/train_vit.py
```

### 4. Evaluate Model

```bash
python models/test_vit.py
```

### 5. Generate Attention Rollout

```bash
python models/attention_rollout.py
```

### 6. Biomarker Discovery

```bash
python biomarker_analysis/statistical_analysis.py
```

---

## Results

The proposed framework achieved:

| Metric | Value |
|---------|-------|
| Test Accuracy | 75.0% |
| Precision | 66.7% |
| Recall | 90.9% |
| F1-score | 0.769 |
| ROC-AUC | 0.881 |

After Benjamini–Hochberg false discovery rate correction, two chromatin texture biomarkers remained statistically significant:

- GLCM Dissimilarity
- GLCM Homogeneity

---

## Software

- Python
- PyTorch
- TorchVision
- NumPy
- SciPy
- Scikit-learn
- scikit-image
- OpenCV
- Matplotlib
- Pandas

---

## Citation

If you use this repository, please cite:

```
Md Abu Sufian, Nadeem Qazi, Prashant Ruchaya.

Explainable AI Reveals Morphological and Chromatin Biomarkers of Nuclear Ageing.

Diagnostics (Submitted).
```

---

## Correspondence

**Md Abu Sufian**

Doctoral Researcher

Department of Engineering and Computing

University of East London

Email: m.sufian@uel.ac.uk

---

## License

This repository is released for academic and research purposes.

Please cite the associated publication when using this code.
