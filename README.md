# Segmentation of Low-Grade Glioma

This project focuses on segmenting low-grade gliomas from brain MRI scans using deep learning models.

## 🧠 Methodology
- **Models**:
  - **ResNet18** – tumor presence classifier.
  - **U-Net** – main segmentation model (31M parameters).
  - **U-Net Mini** – lightweight version (1.8M parameters).
- **Loss Functions**:
  - `BCEWithLogitsLoss` (with class weighting).
  - Dice Loss for evaluation.

## 📊 Results
- **ResNet18**: 98% accuracy on tumor presence classification.  
- **Segmentation Performance (Dice coefficient)**:
  - ResNet18 + U-Net → **93.1%** (all images), **79.1%** (glioma only).
  - ResNet18 + U-Net Mini → **89.9%** (all images), **68.9%** (glioma only).
- Competitive with Kaggle solutions (best reported Dice ≈ 96%).

## 📖 References
- [Kaggle Dataset](https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation)  
- Siddique et al., *U-Net and Its Variants for Medical Image Segmentation*, IEEE Access, 2021.  
