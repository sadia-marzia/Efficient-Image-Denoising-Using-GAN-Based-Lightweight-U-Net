# Efficient-Image-Denoising-Using-GAN-Based-Lightweight-U-Net

## 📌 Overview
This repository presents an **efficient GAN-based Lightweight U-Net model** for **image denoising**, designed to achieve high-quality restoration while maintaining **low computational complexity**. The proposed framework is particularly suitable for **real-time and resource-constrained environments**, where traditional deep-learning denoising models are often impractical.

Image denoising plays a crucial role in computer vision and imaging systems, as noise degradation directly affects downstream tasks such as segmentation, detection, and recognition. This work demonstrates that a **compact generator architecture combined with adversarial learning and a weighted multi-loss strategy** can deliver strong denoising performance without heavy computational overhead.

---

## 🎯 Objectives
- Design a **lightweight GAN-based denoising model**
- Reduce computational cost while preserving structural and perceptual image quality
- Achieve robust generalization across multiple datasets
- Enable **real-time deployment** on low-resource devices

---

## 🧠 Proposed Architecture

### 🔹 Generator: Lightweight U-Net
- Compact U-Net structure
- **Depthwise separable convolutions** to reduce parameters and FLOPs
- Encoder–decoder architecture with skip connections for detail preservation

### 🔹 Discriminator
- Guides the generator through **adversarial learning**
- Encourages realistic texture and fine detail reconstruction

---

## 🔧 Loss Function Design
A key contribution of this work is the **weighted multi-loss optimization strategy**, which balances multiple denoising objectives:

- **L1 Loss** – Pixel-level reconstruction accuracy  
- **Perceptual Loss (VGG-based)** – High-level feature consistency  
- **SSIM Loss** – Structural integrity preservation  
- **GAN Loss** – Natural texture and realism  

The composite loss ensures an optimal trade-off between accuracy, structure, and visual realism.

---

## 📊 Experimental Results

### 🔹 Dataset 1 (Primary Dataset)
| Noise Level | PSNR | SSIM |
|------------|------|------|
| 50 / 255   | 24.45 | 0.829 |
| 100 / 255  | 22.46 | 0.628 |

### 🔹 Dataset 2 (Benchmark Dataset)
- Consistent denoising trends observed
- Demonstrates **robustness and cross-domain generalization**

---

## 🚀 Key Contributions
- Lightweight GAN-based U-Net for efficient image denoising
- Use of **depthwise separable convolutions** for reduced complexity
- Novel **weighted multi-loss optimization framework**
- Strong performance with low computational requirements
- Suitable for **real-time and edge-device deployment**

---
├── data/ # Training and evaluation datasets
├── models/
│ ├── generator.py # Lightweight U-Net generator
│ └── discriminator.py # GAN discriminator
├── loss/ # Multi-loss function definitions
├── training/ # Training scripts
├── evaluation/ # PSNR, SSIM evaluation scripts

└── README.md # Documentation

## 🗂️ Repository Structure
