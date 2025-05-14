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

```bash
├── DL_Project3_Final.ipynb      # Main notebook with full implementation and visualizations.
├── DL_Project_3.pdf             # Project report
├── Visualizations               # Contains the graphs and sample data visualizations
├── TestDataSet (1).zip          # Dataset used in the project
├── requirements.txt             # Project dependencies
└── README.md                    # Project documentation
```


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
```

### Running the Notebook

Open and run all cells in `DL_Project3_Final.ipynb`:

```bash
jupyter notebook DL_Project3_Final.ipynb
```
### Running the Notebook
The adverserial dataset saved in the notebook is available at: https://drive.google.com/drive/folders/1bGcPfzcW7fqCyaANRtxbbrwHTYno00PH?usp=sharing

## 📊 Results Summary

| Dataset                 | ResNet-34 Top-1 | ResNet-34 Top-5 |
|-------------------------|-----------------|-----------------|
| Original                | 76.2%           | 94.2%           |
| FGSM (ε = 0.02)         | 3.4%            | 21.2%           |
| PGD (10 steps)          | 0.0%            | 1.8%            |
| PatchPGD (32×32, tuned) | 6.4%            | 29.6%           |

## 🔁 Transferability Analysis

All attacks were transferred to 4 other models. Notably:

- **MobileNet-V2** showed the steepest accuracy drop.
- **ViT-L-32** was the most robust to adversarial perturbations.

## 📌 Key Takeaways

- Single-step **FGSM** is already effective at degrading model performance.
- Iterative **PGD** attacks can fully collapse model accuracy.
- Even localized **PatchPGD** attacks significantly reduce accuracy.
- Hyperparameter tuning is critical, especially for patch-based attacks.

## 📜 License & Acknowledgements

This work was submitted as part of Deep Learning (Spring 2025) at NYU.  
We acknowledge the use of ChatGPT, Grok, Perplexity, StackOverflow, and official documentation for libraries used.

## 📎 Final Report

For detailed methodology, attack visualizations, and evaluation breakdowns, see:  
**`DL_Project_3.pdf`**
