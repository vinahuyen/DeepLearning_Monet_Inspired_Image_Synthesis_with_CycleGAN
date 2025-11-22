# Deep Learning: Monet-Inspired Image Synthesis with CycleGAN
### *Transforming Real-World Photos into Impressionist Art Using Deep Learning*

---

## 📌 Overview
This project applies **CycleGAN**, a type of Generative Adversarial Network designed for *unpaired* image-to-image translation, to transform everyday photographs into images resembling the style of **Claude Monet**.

The model learns Monet’s brushwork, color palette, and textures, enabling it to generate realistic impressionist-style artwork from standard photos.

This work is developed as part of the Kaggle competition: **"I'm Something of a Painter Myself."**

---

## 🎯 Objectives
- Translate real photos into Monet-style paintings.  
- Train CycleGAN on **unpaired datasets** (Monet paintings & real photos).  
- Apply data augmentation to improve model generalization.  
- Visualize and compare original vs. generated images.  
- Submit high-quality Monet-style predictions to Kaggle.

---

## 🧠 Methodology

### 1. Dataset
The dataset contains:
- **Monet paintings** (`monet_jpg/`)
- **Real-world photos** (`photo_jpg/`)

Provided by Kaggle for unpaired translation.

---

### 2. Model: CycleGAN
CycleGAN consists of:

#### **2 Generators**
- Photo → Monet  
- Monet → Photo  

#### **2 Discriminators**
- Assess realism of generated outputs

#### **CycleGAN uses**
- **Adversarial loss**  
- **Cycle-consistency loss**  
- **Identity loss**

These ensure content preservation while producing Monet-like textures.

---

## 🛠 Environment Setup
This project uses:
- Python 3.11  
- PyTorch  
- Torchvision  
- CUDA (GPU T4 ×2 on Kaggle)  
- TensorBoard (optional)  
- Pillow, Matplotlib  

---

## 🚀 Training

### Key training features:
- Image size resized to **256×256**
- Data augmentation (flip, color jitter)
- Normalization & denormalization helpers
- Mixed precision (AMP)
- Multi-GPU support (if available)

Training runs for **multiple epochs**, steadily improving the Monet-style outputs.

---

## 🖼 Results

The model outputs:
- Monet-style translations for each input photo  
- Side-by-side visualizations of:
  - Original images  
  - Augmented images  
  - Generated Monet-style images  

Final submissions are saved as JPEG files in the required `images/` format for Kaggle scoring.

---

## 📁 Repository Structure

