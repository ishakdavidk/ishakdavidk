# David Ishak Kosasih

**AI Researcher | Ph.D. in Computer Engineering**

Deep learning researcher with 7+ years of experience in anomaly detection, representation learning, computer vision, and edge AI deployment. Currently focused on on-device video event recognition at OnD AI.

Seoul, South Korea | [LinkedIn](https://linkedin.com/in/ishakdavids) | [GitHub](https://github.com/ishakdavidk) | ishakdavids@gmail.com

---

## Research Interests

- Spatiotemporal deep learning for video-based action and event recognition
- Representation learning (contrastive learning, autoencoders, Siamese networks)
- On-device / edge AI inference optimization
- Computer vision (object detection, video understanding)
- Deep learning-based website fingerprinting
- Generative models (GANs, VAEs, diffusion models)

---

## Featured Projects

### Real-Time Fight Detection with Vision Transformer
[`fighting_detection`](https://github.com/ishakdavidk/fighting_detection)

Real-time violence detection in video using a fine-tuned **VideoMAE v2** (Vision Transformer) on the RWF-2000 dataset.

- Fine-tuned ViT-Base (pre-trained on Kinetics-400) by unfreezing last 2 transformer blocks + classifier (~14.2M / 86.2M trainable params)
- Input: 16 frames at 224x224 resolution
- Achieved **98.99% Validation F1** at epoch 5 of 15
- Supports live real-time detection from camera feeds

**Tech:** PyTorch, VideoMAE v2, HuggingFace Transformers

---

### Dashcam Accident Detection with YOLOv11 + Edge Deployment
[`ego_accident_detection_yolo`](https://github.com/ishakdavidk/ego_accident_detection_yolo)

End-to-end ego-vehicle accident detection pipeline using **YOLOv11**, optimized for edge deployment on **Radxa CM5** and **NVIDIA Jetson**.

- Two-stage YOLOv11s training: 30 epochs frozen warm-up + 80 epochs full fine-tuning at 1024x1024
- Model conversion pipeline: `.pt` -> ONNX -> RKNN for NPU acceleration
- Full edge deployment features: RKNN NPU inference, Radxa Camera 4K (IMX415), event recording with pre/post buffer, GPIO LED indicator, HTTP MJPEG streaming
- Temporal confidence buffer with cooldown to reduce false positives

**Tech:** YOLOv11, RKNN, ONNX, Python, OpenCV

---

### Dashcam Accident Detection with R(2+1)D 3D CNN
[`ego_accident_detection_r2plus1d`](https://github.com/ishakdavidk/ego_accident_detection_r2plus1d)

Real-time ego-involved traffic accident detection from dashcam video using **R(2+1)D-18** 3D CNN, trained on the DoTA dataset and deployable on NVIDIA Jetson.

- R(2+1)D-18 backbone pretrained on Kinetics-400 with custom binary classification head
- Input: 16-frame segments at 112x112, binary classification (Normal/Accident) with sigmoid probability
- Jetson deployment with dual USB cameras, FP16 inference, batched inference
- MJPEG stream on port 8080 with automatic accident clip saving

**Tech:** PyTorch, R(2+1)D, NVIDIA Jetson, CUDA

---

### Co-Location Detection Using Magnetometer Data
[`RP_CLT`](https://github.com/ishakdavidk/RP_CLT)

Research implementation for determining whether mobile devices are in the same physical location by comparing magnetometer sensor readings using autoencoders. **Published in Sensors journal (2021).**

- Two architectures: Dense Autoencoder (1D time-series) and Convolutional Autoencoder (32x32 grayscale signal images)
- Anomaly detection approach: low reconstruction error = co-located, high error = different locations
- Developed an Android app for data collection

**Tech:** TensorFlow, Android, Python

**Paper:** [DOI: 10.3390/s21144773](https://doi.org/10.3390/s21144773)

---

### Deep Q-Network for RoboCop 3 (Sega Genesis)
[`Reinforcement-Learning`](https://github.com/ishakdavidk/Reinforcement-Learning)

A DQN reinforcement learning agent that learns to play RoboCop 3 on Sega Genesis using OpenAI Retro.

- DQN with experience replay and target network
- Input: 4 stacked 84x84 grayscale frames processed through 4-layer CNN
- Custom reward shaping (+700 for kills with ammo, penalties for waste)
- 1300 episodes of training with best model checkpoint at episode 400

**Tech:** PyTorch, OpenAI Retro, DQN

---

### Genetic Algorithm for Traveling Salesman Problem
[`Evolutionary-Computation`](https://github.com/ishakdavidk/Evolutionary-Computation)

GA implementation for TSP featuring standard Ordered Crossover (OX) and two custom "natural" crossover methods.

- Three crossover strategies: OX, Natural Crossover (group-based), Semi-Natural Crossover (selective, 75% to better parent)
- Tested on TSPLIB datasets with 48 to 1000 cities

**Tech:** Python

---

## Publications

1. **Kosasih, D.**, Lee, B.-G., & Lim, H. (2023). *Multichannel One-Dimensional Data Augmentation with Generative Adversarial Network.* Sensors, 23, 7693. [DOI: 10.3390/s23187693](https://doi.org/10.3390/s23187693)

2. **Kosasih, D.**, Lee, B.-G., & Lim, H. (2022). *Neural Network and Cloud Computing for Predicting ECG Waves from PPG Readings.* Journal of Multimedia Information System, 9, 11-20. [DOI: 10.33851/JMIS.2022.9.1.11](https://doi.org/10.33851/JMIS.2022.9.1.11)

3. **Kosasih, D.**, Lee, B.-G., Lim, H., & Atiquzzaman, M. (2021). *An Unsupervised Learning-Based Spatial Co-Location Detection System from Low-Power Consumption Sensor.* Sensors, 21, 4773. [DOI: 10.3390/s21144773](https://doi.org/10.3390/s21144773)

4. **Kosasih, D.**, Lim, H., & Lee, B.-G. (2020). *Co-location Detection System Using Mobile Magnetometer Data.* IEEE ICTC 2020, 1833-1838. [DOI: 10.1109/ICTC49870.2020.9289619](https://doi.org/10.1109/ICTC49870.2020.9289619)

---

## Experience

| Period | Role | Organization |
|--------|------|-------------|
| 2025.05 - Present | **AI Researcher** | OnD AI, Gyeonggi-do |
| 2024.03 - 2025.02 | **Postdoctoral Researcher** | Ewha Womans University, Seoul |
| 2019.03 - 2024.02 | **Research Assistant** | Dongseo University, Busan |
| 2018.09 - 2019.02 | **Research Assistant** | Petra Christian University, Surabaya |

### Current Role: AI Researcher at OnD AI
- Developed an on-device dashcam accident detection system using spatiotemporal deep learning for real-time video inference on embedded edge devices
- Designed and deployed a drone detection pipeline using deep learning-based computer vision models optimized for real-time inference

### Postdoctoral Researcher at Ewha Womans University
- Collected and analyzed TCP data of encrypted Tor traffic using deep learning for website fingerprinting research
- Contributed to scientific papers for publication

### Research Assistant at Dongseo University (NRF Project)
- Contributed to a 5-year NRF project: *"Secure Healthcare-Cloud Framework for AI-based Resource Management"*
- Research topics: anomaly detection, representation learning, co-location detection, GAN-based data augmentation, ECG prediction from PPG data
- Managed laboratory server infrastructure

---

## Education

| Degree | Field | University | Period | GPA |
|--------|-------|-----------|--------|-----|
| **Ph.D.** | Computer Engineering | Dongseo University, Busan | 2021 - 2024 | 4.25 / 4.50 |
| **M.Sc.** | Computer Engineering | Dongseo University, Busan | 2019 - 2021 | 4.31 / 4.50 |
| **S.T. (B.Eng.)** | Electrical Engineering | Petra Christian University, Surabaya | 2013 - 2017 | 3.54 / 4.00 (Honors) |

- **Ph.D. Dissertation:** Similarity Constraint Loss for Siamese-based Representation Learning Optimization
- **M.Sc. Thesis:** Co-location Detection System Using Mobile Magnetometer Data
- **B.Eng. Thesis:** Making Mobile Applications for Parking Systems Based on Internet of Things (IoT)

---

## Technical Skills

| Category | Skills |
|----------|--------|
| **Deep Learning** | PyTorch, TensorFlow, CNN, 3D CNN (R(2+1)D), Vision Transformers (VideoMAE v2, MViT), Siamese Networks, Autoencoders, GANs, VAEs, Diffusion Models |
| **Computer Vision** | YOLO (v11), Video Understanding, Object Detection, Action Recognition, Image Processing |
| **Edge AI** | RKNN NPU, NVIDIA Jetson (CUDA, TensorRT, FP16), ONNX, Model Optimization |
| **Data & Analysis** | Time Series (LSTM, Transformers), Graph Neural Networks, Anomaly Detection |
| **Programming** | Python, Java, JavaScript, Node.js, Assembly |
| **Hardware** | Arduino, Raspberry Pi, Radxa CM5, PLC, Embedded Systems |
| **Languages** | Indonesian (Native), English (Advanced), Korean (KIIP Level 4 / ~TOPIK 3) |

---

## Awards

| Year | Competition | Place |
|------|------------|-------|
| 2015 | IMAC Robot Competition - Sepuluh Nopember Institute of Technology | 3rd |
| 2012 | Electrical Fiesta Lego Mindstorms - Petra Christian University | 2nd |
| 2010 | Electrical Fiesta Lego Mindstorms - Petra Christian University | 3rd |
