# Jailbreaking Deep Models — Adversarial Attacks on ResNet-34

**Course:** Deep Learning (Spring 2025)  
**Team SPAR:** Aryan Mamidwar, Spandan Rout  
**Emails:** arm9337@nyu.edu, sr7729@nyu.edu  

## 🧠 Overview

This project investigates adversarial robustness in deep image classifiers, primarily attacking a pretrained **ResNet-34** on a 100-class ImageNet subset. We implemented and compared three adversarial methods:

- **FGSM (Fast Gradient Sign Method)**  
- **PGD (Projected Gradient Descent)**  
- **Patch-PGD (Localized Attack with PGD)**  

We also evaluated the transferability of these attacks to **DenseNet-121**, **EfficientNet-B0**, **MobileNet-V2**, and **ViT-L-32**.

## 📁 Structure

- `DL_Project3_Final.ipynb` – Main notebook with full implementation and visualizations.
- `./datasets/` – Folder containing clean and adversarial test sets.


## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- PyTorch
- TorchVision
- NumPy
- Matplotlib

### Setup

```bash
git clone https://github.com/Spandan-2002/Jailbreaking-Deep-Models.git
cd DL_Project3
pip install -r requirements.txt
