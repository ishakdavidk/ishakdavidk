# Hi, I'm David Ishak Kosasih

I build AI systems that run on edge devices - from real-time video recognition to drone tracking. My work sits at the intersection of deep learning research and practical deployment on resource-constrained hardware.

**Ph.D. in Computer Engineering** | **7+ years in deep learning**

[![Portfolio](https://img.shields.io/badge/Portfolio-ishakdavidk.github.io-00c878?style=flat&logo=googlechrome&logoColor=white)](https://ishakdavidk.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-ishakdavids-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ishakdavids)
[![Email](https://img.shields.io/badge/Email-ishakdavids@gmail.com-red?style=flat&logo=gmail)](mailto:ishakdavids@gmail.com)

---

## What I Build

### Real-Time Fight Detection | Live Video Analysis with VideoMAE v2

[![Repo](https://img.shields.io/badge/GitHub-fighting__detection-181717?style=flat&logo=github)](https://github.com/ishakdavidk/fighting_detection)

https://github.com/user-attachments/assets/fighting_detection_demo

Fine-tuned VideoMAE v2 (ViT-Base, pre-trained on Kinetics-400) on the RWF-2000 dataset for real-time violence detection in live video, achieving 98.99% F1 score. Only the last 2 transformer blocks + classifier head are unfrozen (~14.2M of 86.2M params) for efficient training.

**How it works:**
- Captures 16-frame clips at 224x224 from a live camera feed
- Runs inference through the fine-tuned ViT to classify Fight vs. Normal
- Displays real-time predictions with confidence scores

`PyTorch` `VideoMAE v2` `HuggingFace Transformers` `Vision Transformer`

---

### Co-Location Detection | Published Research
> **Sensors Journal 2021** - Can two phones tell if they're in the same room?

[![Repo](https://img.shields.io/badge/GitHub-RP__CLT-181717?style=flat&logo=github)](https://github.com/ishakdavidk/RP_CLT)
[![Paper](https://img.shields.io/badge/DOI-10.3390%2Fs21144773-green?style=flat)](https://doi.org/10.3390/s21144773)

My master's thesis turned published paper. The idea: train an autoencoder on one phone's magnetometer signal, then test reconstruction on another phone's signal. If reconstruction error is low, the phones are co-located.

**What I built:**
- Two autoencoder architectures: Dense AE for 1D time-series, Convolutional AE for 32x32 signal images
- Android app for magnetometer data collection
- Full experimental pipeline for evaluating co-location accuracy

`TensorFlow` `Android` `Autoencoder` `Anomaly Detection`

---

### DQN Agent | Teaching an AI to Play RoboCop 3
> **Reinforcement learning on Sega Genesis via OpenAI Retro**

[![Repo](https://img.shields.io/badge/GitHub-Reinforcement--Learning-181717?style=flat&logo=github)](https://github.com/ishakdavidk/Reinforcement-Learning)

A Deep Q-Network agent that learns to play RoboCop 3 on Sega Genesis. Built with experience replay, target networks, and custom reward shaping.

**What I built:**
- 4-layer CNN processing 4 stacked 84x84 grayscale frames
- Custom reward engineering: +700 for kills with ammo, penalties for wasted shots
- Trained over 1,300 episodes, best checkpoint at episode 400

`PyTorch` `OpenAI Retro` `DQN` `Reinforcement Learning`

---

### Genetic Algorithm | Custom Crossover Methods for TSP
> **Novel crossover strategies tested on up to 1,000-city problems**

[![Repo](https://img.shields.io/badge/GitHub-Evolutionary--Computation-181717?style=flat&logo=github)](https://github.com/ishakdavidk/Evolutionary-Computation)

Implemented three crossover strategies for solving the Traveling Salesman Problem: standard Ordered Crossover (OX), a group-based "Natural Crossover," and a selective "Semi-Natural Crossover" that biases 75% toward the better parent.

`Python` `Genetic Algorithm` `TSPLIB`

---

## Publications

| Year | Paper | Venue |
|------|-------|-------|
| 2023 | [Multichannel 1D Data Augmentation with GAN](https://doi.org/10.3390/s23187693) | Sensors |
| 2022 | [Neural Network for Predicting ECG from PPG](https://doi.org/10.33851/JMIS.2022.9.1.11) | J. Multimedia Info. System |
| 2021 | [Unsupervised Co-Location Detection from Magnetometer](https://doi.org/10.3390/s21144773) | Sensors |
| 2020 | [Co-location Detection Using Mobile Magnetometer](https://doi.org/10.1109/ICTC49870.2020.9289619) | IEEE ICTC |

---

## Tech Stack

```
Deep Learning       PyTorch | TensorFlow | Sequence Models (RNN/LSTM/GRU) | GANs / VAEs | Siamese Networks | Autoencoders
Computer Vision     YOLO | Vision Transformers / VideoMAE v2 | 3D CNN (R(2+1)D, SlowFast) | OpenCV | Action Recognition | Object Detection
Edge Deployment     NVIDIA Jetson | RKNN NPU | ONNX | TensorRT | FP16 Optimization | Radxa CM5
Programming         Python | Java / Android | SQL | Linux / Server Admin | Git / GitHub
Research            Representation Learning | Anomaly Detection | Website Fingerprinting | Time Series Analysis | Graph Neural Networks
Hardware            Arduino | Raspberry Pi | PLC Programming | Embedded Systems | Sensor Integration
```

---

## Background

|  | Details |
|--|---------|
| **Now** | AI Researcher at OnD AI - building on-device video intelligence for edge deployment |
| **2024** | Postdoc at Ewha Womans University - Tor website fingerprinting with deep learning |
| **2021-2024** | Ph.D. Computer Engineering, Dongseo University (GPA: 4.25/4.50) |
| **2019-2021** | M.Sc. Computer Engineering, Dongseo University (GPA: 4.31/4.50) |
| **2013-2017** | B.Eng. Electrical Engineering, Petra Christian University (Honors, 3.54/4.00) |
