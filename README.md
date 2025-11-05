# MST_Prediction: Multi-source Spatio-temporal Transfer Prediction for Air Traffic Flow

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-%3E1.7-red)
![License](https://img.shields.io/badge/License-MIT-green)

Official implementation of **"Multi-source Data Spatio-temporal Reconstruction and Transfer Fusion Method for Air Traffic Flow Prediction"**.

## 📖 Abstract

Air traffic flow exhibits complex nonlinear characteristics under multi-source disturbances such as abnormal weather and peak flow during holidays. Addressing the limitations of historical traffic flow dependency models, we propose the **Multi-source Spatio-temporal Transfer Prediction (MSTP)** method featuring:

- **Unified Graph Encoding** of weekly, calendar, weather, and holiday data
- **Temporal Awareness Enhancement (TAE)** with Graph Simple Recurrent Unit (G-SRU)
- **Multi-range Dynamic Network Attention (MDNA)** for adaptive feature weighting
- **Many-to-many transfer fusion** using Kernel Canonical Correlation Analysis (KCCA)

Compared with baseline methods (GCN, LSTM), MSTP achieves **8%-12% reduction** in prediction error on the PEK-air dataset.

## 🚀 Key Features

- **Multi-source Data Reconstruction Data Reconstruction**: Decouples features from weekly, calendar, weather, and holiday data
- **Dynamic Spatio-temporal Modeling**: Captures both periodic patterns and event-driven disruptions
- **Joint Arrival/Departure Flow Prediction**: Simultaneous forecasting through forecasting through nonlinear kernel mapping

## 🏗️ Model Architecture

The MSTP framework consists of three core components:

1. **Temporal Awareness Enhancement (TAE)**
   - Time2Vec embeddings for periodic pattern learning
   - Custom Graph Simple Recurrent Unit (G-SRU) for temporal dynamics

2. **Multi-range Dynamic Network Attention (MDNA)**
   - Network-level attention for source contribution source contribution assessment
   - Dynamic attention for special event handling

3. **Many-to-many Transfer Fusion**
   - Kernel CCA for nonlinear correlation analysis correlation analysis
   - Cross-source feature alignment in high-dimensional space

## 📦 Installation

```bash
git clone https://github.com/yourusername/MST_Prediction.git
cd MST_Prediction
pip install -r requirements.txt
