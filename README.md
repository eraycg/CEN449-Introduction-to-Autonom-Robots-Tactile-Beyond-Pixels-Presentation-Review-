# CEN449-Introduction-to-Autonom-Robots-Tactile-Beyond-Pixels-Presentation-Review-
![Course](https://img.shields.io/badge/Course-Introduction%20to%20Autonomous%20Robots-blue)
![Topic](https://img.shields.io/badge/Topic-Robotic%20Manipulation-orange)
![Model](https://img.shields.io/badge/Model-Sparsh--X-green)

## 📌 Overview
This repository contains the presentation materials and summary for the *"Introduction to Autonomous Robots"* course (4th Year).

We conducted a detailed review and presented the paper *"Tactile Beyond Pixels: Multisensory Touch Representations for Robot Manipulation", which was published by **Meta FAIR* at *CoRL 2025*.

The project focuses on *Sparsh-X*, a novel multisensory tactile backbone that integrates vision, audio, IMU, and pressure data to enhance robotic manipulation capabilities.

## 📄 The Paper
* *Title:* Tactile Beyond Pixels: Multisensory Touch Representations for Robot Manipulation
* *Authors:* Mike Lambeta, Huazhe Xu, Jingwei Xu, et al. (Meta FAIR)
* *Conference:* Conference on Robot Learning (CoRL) 2025
* *Key Contribution:* Introducing *Sparsh-X, a self-supervised learning model for the **Digit-360* sensor.

## 🧠 Key Concepts Covered

### 1. Sparsh-X Architecture
Sparsh-X utilizes a *Transformer-based architecture* with a unique fusion mechanism.
* *Multimodality:* Processes Vision, Audio, IMU, and Pressure data simultaneously.
* *Bottleneck Attention:* Efficiently fuses modalities using a small set of bottleneck tokens to reduce computational cost ($O(N)$ complexity).

### 2. Self-Supervised Learning (SSL)
The model is trained on *1 million tactile frames* without human labels using Masked Image Modeling (MIM). It employs a Teacher-Student architecture (similar to DINOv2) to learn robust physical features.

### 3. Frozen Representations & Adaptation
We analyzed how *frozen Sparsh-X representations* outperform visual-only baselines in:
* *Force Estimation:* Reducing error to 35mN.
* *Surface Classification:* Identifying friction and texture via audio/vibration.
* *Slip Detection:* Utilizing high-frequency audio data to detect microslips.

### 4. Sim-to-Real Adaptation
Explored the use of *ControlNet* to adapt simulation-trained policies (like 'Hora') to the real world by injecting tactile feedback, significantly reducing object drift during in-hand rotation.

## 📂 Repository Structure

```bash
├── 661_tacticle_pixels.pdf      # The original research paper
├── Presentation_Slides.pptx     # Our presentation slides
├── README.md                    # Project documentation
└── assets/                      # Images used in the presentation


📊 Evaluation & Results
In our presentation, we highlighted the following results from the paper:

Plug Insertion Task: Success rate increased from 20% (Vision only) to 90% (Sparsh-X) due to the detection of contact sounds ("clicks").

In-Hand Rotation: Vertical drift was reduced by 90% using tactile feedback.

👥 Authors / Presenters
Cem Keleş-2020556037 - Theory, Architecture & Data Collection

Kamil Eray Gündüz-2020556028- Experiments, Robotics Policies & Results

🔗 References
Original Paper Link (https://openreview.net/forum?id=gD6YV5OuW3#discussion15.12.2025)

Meta FAIR Robotics
