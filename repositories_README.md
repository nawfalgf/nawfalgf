<div align="center">

# 🔬 Research & Software Repositories

### Private research code • AI • 3D LiDAR • Point Clouds • Wireless Systems

This page provides an overview of my current **private research and software repositories**.

The repositories contain ongoing research, experimental implementations, model architectures, data-processing pipelines, evaluation tools, and research software. Because some of this work is associated with active or future publications, the complete source code is not publicly available.

**Repository access may be granted upon request** for academic research, collaboration, reproducibility, technical review, or other appropriate uses.

<p>
<a href="README.md"><b>🏠 Back to Profile</b></a>
&nbsp;&nbsp;•&nbsp;&nbsp;
<a href="mailto:nawfal.guefrachi@mst.edu?subject=GitHub%20Repository%20Access%20Request"><b>📩 Request Access</b></a>
</p>

</div>

---

## 🗂️ Repository Overview

I currently maintain **5 primary private repositories** covering several stages of my research, from wireless communications and mobility prediction to modern 3D LiDAR perception and human activity understanding.

```text
                         Research Repositories
                                  │
             ┌────────────────────┼────────────────────┐
             │                    │                    │
             ▼                    ▼                    ▼
       3D LiDAR & AI       Self-Supervised       Wireless & IoT
             │                 Learning                 │
       ┌─────┼─────┐               │                    │
       ▼     ▼     ▼               ▼                    ▼
    PV-RCNN STG- Episodic     LiDARFall-SSL      Predictive ADR
      +     FallNet Activity                        for LoRaWAN
 PointNet-          Recognition
   LSTM
```

| # | Repository | Research Focus | Main Methods |
|---|---|---|---|
| 01 | **PV-RCNN + PointNet-LSTM Activity Recognition** | End-to-end LiDAR human activity recognition | PV-RCNN, PointNet, LSTM, tracking |
| 02 | **STG-FallNet** | Spatiotemporal LiDAR fall detection | Point attention, temporal convolutions, Transformer |
| 03 | **LiDARFall-SSL** | Self-supervised LiDAR fall classification | Contrastive learning, masked reconstruction |
| 04 | **Episodic Point-Cloud Activity Recognition** | Activity recognition from point-cloud sequences | PointNet, BiGRU, temporal attention |
| 05 | **Predictive ADR for Mobile LoRaWAN** | Mobility-aware wireless optimization | RNN, LSTM, ADR, RSSI estimation |

---

# 01 — 🧍 PV-RCNN + PointNet-LSTM LiDAR Activity Recognition

**Status:** 🔒 Private Repository  
**Area:** 3D LiDAR • Human Activity Recognition • Deep Learning

An end-to-end framework for recognizing human activities directly from 3D LiDAR scenes.

The system begins with **PV-RCNN-based pedestrian detection**, associates detections over time, extracts each detected person's 3D point cloud, normalizes and samples the human points, builds temporal sequences, and classifies the resulting activity using a **PointNet + LSTM** architecture.

### Framework

```text
3D LiDAR Scene
      │
      ▼
   PV-RCNN
      │
      ▼
Pedestrian Detection
      │
      ▼
3D Human Tracking
      │
      ▼
Human Point-Cloud Extraction
      │
      ▼
Normalization + Point Sampling
      │
      ▼
Temporal Point-Cloud Sequence
      │
      ▼
   PointNet
      │
      ▼
     LSTM
      │
      ▼
Temporal Attention
      │
      ▼
Activity Classification
```

The framework is designed for activities such as walking, running, falling, dizzy walking, talking on the phone, and injured-leg walking.

**Technologies**

`Python` • `PyTorch` • `OpenPCDet` • `PV-RCNN` • `PointNet` • `LSTM` • `Open3D`

---

# 02 — 🚨 STG-FallNet

### Spatiotemporal Geometry Network for LiDAR Fall Detection

**Status:** 🔒 Private Repository  
**Area:** Fall Detection • Temporal Deep Learning • 3D Point Clouds

STG-FallNet is a modular deep-learning framework for **fall versus non-fall classification from real-world 3D LiDAR sequences**.

Rather than treating every LiDAR frame independently, the model is designed to learn both the person's **spatial geometry** and how that geometry changes through time.

The framework combines point-level feature learning with body-geometry descriptors, motion-aware representations, multi-scale temporal processing, and Transformer-based sequence modeling.

### Concept

```text
LiDAR Sequence
      │
      ▼
Human Point Clouds
      │
      ├───────────────┐
      ▼               ▼
Point Features   Geometry Features
      │               │
      └───────┬───────┘
              ▼
       Feature Fusion
              │
              ▼
   Temporal Feature Modeling
              │
              ▼
      Transformer Encoder
              │
              ▼
        Fall / Non-Fall
```

The repository also contains the experimental pipeline for training, validation, threshold selection, evaluation, and research-oriented visualization.

**Technologies**

`Python` • `PyTorch` • `Point Clouds` • `Attention` • `Transformers` • `Temporal Modeling`

---

# 03 — 🧠 LiDARFall-SSL

### Self-Supervised Learning for LiDAR Fall Classification

**Status:** 🔒 Private Repository  
**Area:** Self-Supervised Learning • 3D AI • Fall Detection

LiDARFall-SSL explores how **unlabeled real-world LiDAR measurements** can be used to learn meaningful human representations before supervised fall-classification training.

The project combines self-supervised objectives such as **masked point reconstruction** and **contrastive representation learning**, followed by supervised fine-tuning for fall versus non-fall classification.

### Learning Strategy

```text
           Unlabeled LiDAR Data
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
 Masked Reconstruction   Contrastive Learning
          │                   │
          └─────────┬─────────┘
                    ▼
          Pretrained 3D Encoder
                    │
                    ▼
          Labeled Fall Dataset
                    │
                    ▼
             Fine-Tuning
                    │
                    ▼
            Fall / Non-Fall
```

A major motivation is improving representation quality when labeled real-world data are limited and studying **synthetic-to-real generalization** for privacy-preserving human sensing.

**Technologies**

`Self-Supervised Learning` • `Contrastive Learning` • `Masked Modeling` • `Point Transformers` • `PyTorch`

---

# 04 — 🎞️ Episodic Point-Cloud Activity Recognition

**Status:** 🔒 Private Repository  
**Area:** Temporal Point Clouds • Human Activity Recognition

This project studies human activity recognition using **episodes of consecutive LiDAR frames instead of isolated point-cloud snapshots**.

Each frame is encoded using a shared PointNet-style spatial encoder. The sequence of frame representations is then processed by a **bidirectional GRU**, while learned temporal attention emphasizes the most informative parts of the episode.

### Architecture

```text
Frame 1 ──► Point Encoder ──┐
Frame 2 ──► Point Encoder ──┤
Frame 3 ──► Point Encoder ──┤
   ...                      ├──► BiGRU ──► Temporal Attention ──► Activity
Frame T ──► Point Encoder ──┘
```

The implementation is structured to support temporal sequences with variable numbers of valid frames and point clouds with variable point counts through masking and custom batching.

**Technologies**

`PointNet` • `BiGRU` • `Temporal Attention` • `Point Clouds` • `PyTorch` • `LiDAR`

---

# 05 — 📡 Predictive ADR for Mobile LoRaWAN Devices

**Status:** 🔒 Private Repository  
**Area:** Wireless Communications • Machine Learning • IoT

This repository comes from my earlier work in telecommunications and intelligent wireless systems.

The project investigates **mobility-aware Adaptive Data Rate (ADR)** for LoRaWAN devices. Historical mobility information is processed by RNN/LSTM models to estimate the device's next position, which can then support predictive radio-parameter decisions.

### Concept

```text
Historical Device Positions
          │
          ▼
       RNN / LSTM
          │
          ▼
Next-Position Prediction
          │
          ▼
Distance / RSSI Estimation
          │
          ▼
Predictive ADR Decision
          │
          ▼
LoRaWAN Radio Configuration
```

The repository connects machine-learning-based mobility prediction with LoRaWAN communication parameters and experimental gateway/device integration concepts.

**Technologies**

`LoRaWAN` • `LSTM` • `RNN` • `Adaptive Data Rate` • `RSSI` • `Wireless Networks` • `IoT`

---

## 🔬 Research Progression

Together, these repositories represent the evolution of my technical interests:

```text
Telecommunications
      │
      ▼
Wireless + IoT Systems
      │
      ▼
Machine Learning
      │
      ▼
3D LiDAR Perception
      │
      ▼
Point-Cloud Deep Learning
      │
      ▼
Temporal Human Activity Recognition
      │
      ▼
Self-Supervised 3D Learning
      │
      ▼
Privacy-Preserving Intelligent Sensing
```

Although the application areas differ, the repositories share a common goal:

> **Building intelligent systems that learn useful spatial and temporal representations from real-world sensor data.**

---

## 🔐 Repository Access

The complete implementations are currently maintained in **private GitHub repositories**.

Access may be considered for:

- Academic research
- Research collaboration
- Reproducibility and technical review
- Potential joint projects
- Relevant educational or non-commercial research use

To request access, please include:

**1.** Your name  
**2.** Institution or affiliation  
**3.** Repository of interest  
**4.** Brief description of the intended use

<p align="center">

<a href="mailto:nawfal.guefrachi@mst.edu?subject=GitHub%20Repository%20Access%20Request">
<img src="https://img.shields.io/badge/Request%20Repository%20Access-nawfal.guefrachi%40mst.edu-D14836?logo=gmail&logoColor=white" />
</a>

</p>

---

## 🤝 Research & Collaboration

I am interested in collaborations involving:

`3D LiDAR` • `AI` • `Machine Learning` • `Point Clouds` • `Human Activity Recognition` • `Fall Detection` • `Self-Supervised Learning` • `Computer Vision` • `Intelligent Sensing` • `Wireless Systems`

For research discussions, collaboration, or repository-access inquiries:

📧 **nawfal.guefrachi@mst.edu**

---

<div align="center">

### 🏠 [Back to Main Profile](../README.md)

**Research • Build • Evaluate • Share**

</div>
