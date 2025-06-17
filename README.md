# 3D-U-Net-with-ConvLSTM-for-Cloud-Prediction-using-SEVIR-Data
This project implements an advanced deep learning solution for cloud prediction using satellite infrared data from the SEVIR (Storm EVent ImageRy) dataset. The model predicts 6 future cloud frames (30+ minutes ahead) from 12 input frames with high spatial resolution (192×192 pixels)
# 3D U-Net Cloud Prediction with ConvLSTM

Built advanced 3D U-Net model with ConvLSTM for SEVIR weather prediction using TensorFlow, achieving 0.88 Dice score, 0.88 IoU for accurate cloud forecasting in severe weather early warnings.

## 🌩️ Project Overview

This project implements a deep learning solution for cloud prediction using satellite infrared data from the SEVIR dataset. The model predicts **6 future cloud frames** (30+ minutes ahead) from **12 input frames** with high spatial resolution (192×192 pixels), achieving exceptional performance with **88%+ accuracy**.

## 🏗️ Architecture

- **3D U-Net** encoder-decoder with skip connections for spatial feature preservation
- **ConvLSTM** layers for temporal sequence modeling (96 filters, 3×3 kernel)
- **Combined loss function** (60% Binary Cross-Entropy + 40% Dice loss)
- **Memory-efficient preprocessing** for large-scale satellite data processing
- **Progressive filtering**: 16→32→64 filters in encoder, reverse in decoder

## 📊 Results

| Metric | Training | Validation |
|--------|----------|------------|
| **Dice Coefficient** | 0.8971 (89.71%) | **0.8857 (88.57%)** |
| **Loss** | 0.1216 | **0.1394** |
| **Training Epochs** | 30 (early stopping at 28) | - |
| **Convergence** | Excellent (no overfitting) | - |

## 🚀 Quick Start

### Prerequisites
Clone repository
git clone https://github.com/krish7935/3D-U-Net-with-ConvLSTM-for-Cloud-Prediction-using-SEVIR-Data
cd 3D-UNet-Cloud-Prediction-SEVIR

Install dependencies
pip install -r requirements.txt

