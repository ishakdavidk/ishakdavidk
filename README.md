# Hi, I'm David Ishak Kosasih

I build AI systems that run on edge devices - from dashcam accident detection to real-time drone tracking. My work sits at the intersection of deep learning research and practical deployment on resource-constrained hardware.

**Ph.D. in Computer Engineering** | **4 published papers** | **7+ years in deep learning**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-ishakdavids-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ishakdavids)
[![Email](https://img.shields.io/badge/Email-ishakdavids@gmail.com-red?style=flat&logo=gmail)](mailto:ishakdavids@gmail.com)

---

## What I Build

### Real-Time Fight Detection | Vision Transformer on Live Video
> **98.99% F1 Score** - Fine-tuned VideoMAE v2 for violence detection

[![Repo](https://img.shields.io/badge/GitHub-fighting__detection-181717?style=flat&logo=github)](https://github.com/ishakdavidk/fighting_detection)

https://github.com/user-attachments/assets/fighting_detection_demo

I fine-tuned a VideoMAE v2 (ViT-Base, pre-trained on Kinetics-400) on the RWF-2000 dataset for real-time violence detection. Only the last 2 transformer blocks + classifier head are unfrozen (~14.2M of 86.2M params), keeping training efficient while achieving near-perfect accuracy.

**How it works:**
- Captures 16-frame clips at 224x224 from a live camera feed
- Runs inference through the fine-tuned ViT to classify Fight vs. Normal
- Displays real-time predictions with confidence scores

`PyTorch` `VideoMAE v2` `HuggingFace Transformers` `Vision Transformer`

---

### Dashcam Accident Detection | YOLOv11 on Edge Hardware
> **Full pipeline from training to Radxa CM5 / Jetson deployment**

[![Repo](https://img.shields.io/badge/GitHub-ego__accident__detection__yolo-181717?style=flat&logo=github)](https://github.com/ishakdavidk/ego_accident_detection_yolo)

An end-to-end system that detects accidents involving the dashcam vehicle (ego-vehicle) and runs entirely on edge devices with NPU acceleration.

**What I built:**
- Two-stage YOLOv11s training pipeline (30 epochs frozen + 80 epochs full fine-tuning at 1024x1024)
- Model conversion chain: PyTorch `.pt` -> ONNX -> RKNN for NPU deployment
- Edge system on Radxa CM5: 4K camera input, NPU inference, event recording with pre/post buffer, GPIO LED alerts, HTTP MJPEG live streaming
- Temporal confidence buffer with cooldown to suppress false positives

`YOLOv11` `RKNN NPU` `ONNX` `Radxa CM5` `NVIDIA Jetson` `OpenCV`

---

### Dashcam Accident Detection | 3D CNN with Spatiotemporal Learning
> **R(2+1)D-18 for video-level accident classification, deployed on Jetson**

[![Repo](https://img.shields.io/badge/GitHub-ego__accident__detection__r2plus1d-181717?style=flat&logo=github)](https://github.com/ishakdavidk/ego_accident_detection_r2plus1d)

A different approach to the same problem - instead of detecting objects frame-by-frame, this model understands the temporal dynamics of an accident using 3D convolutions.

**What I built:**
- R(2+1)D-18 backbone (pretrained on Kinetics-400) with custom binary classification head
- Trained on DoTA dataset, filtered for ego-involved accidents only
- Jetson deployment: dual USB cameras, FP16 inference, batched processing
- Live MJPEG streaming with automatic accident clip saving

`PyTorch` `R(2+1)D` `NVIDIA Jetson` `CUDA` `FP16`

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
Deep Learning     PyTorch | TensorFlow | HuggingFace
Vision            YOLO v11 | VideoMAE v2 | R(2+1)D | OpenCV
Edge Deployment   RKNN NPU | NVIDIA Jetson | ONNX | TensorRT | FP16
Models            CNN | 3D CNN | ViT | Siamese | AE | GAN | VAE | GNN
Analysis          LSTM | Transformers | Anomaly Detection
Hardware          Radxa CM5 | Jetson | Arduino | Raspberry Pi
Languages         Python | Java | JavaScript | Node.js
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
