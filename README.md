
#  Cancer Detection using DenseNet121 + Swin Tiny (Fine-Grained Hybrid Model)

## 📘 Overview
This repository implements a **hybrid deep learning pipeline** for cancer detection that fuses **DenseNet121** (a convolutional feature extractor) with **Swin Transformer Tiny** (a hierarchical vision transformer). The goal is to leverage **CNN’s local feature sensitivity** and **Transformer’s global context modeling** for high-accuracy fine-grained image classification in medical imaging tasks.

The project was built and tested in a Jupyter/Colab environment and designed for extensibility to various cancer detection datasets (histopathology, dermoscopy, mammography, etc.).

---

## 🧩 Architecture
- **DenseNet121** — pretrained on ImageNet, used as a *dense feature extractor*.
- **Swin Transformer Tiny** — used to capture *hierarchical self-attention patterns*.
- **Feature Fusion** — extracted embeddings from both networks are concatenated or averaged.
- **Fine-Grained Classifier Head** — multi-layer perceptron with dropout for robust classification.
- **Loss Function** — categorical cross-entropy (for multi-class classification).
- **Optimizer** — AdamW with learning-rate scheduling.

---

## 📊 Key Features
- Hybrid CNN–Transformer architecture  
- Transfer learning with pretrained weights  
- Fine-grained tuning via feature fusion  
- GPU-compatible and notebook-friendly  
- Easily adaptable to new datasets  

---

## 🧠 Dataset
You can plug in any medical imaging dataset with labeled categories.  

**Recommended directory structure:**

dataset/
├── train/
│ ├── class_0/
│ └── class_1/
├── val/
└── test/

---

