# Hi, I’m Nawfal Guefrachi 👋

### Researcher • Engineer • Educator

I enjoy **doing research, building intelligent systems, and teaching others how technology works**.

My work sits at the intersection of **Artificial Intelligence, Machine Learning, Computer Vision, 3D LiDAR sensing, and real-time data processing**. I particularly enjoy taking a research idea from the whiteboard all the way to a working system, experiment, paper, or classroom demonstration.

I also genuinely enjoy teaching. There is something satisfying about taking a complicated topic and hearing someone eventually say:

> “Oh... now it makes sense.”

😄 **Fun fact:** I can probably talk about LiDAR, neural networks, or why an experiment failed for much longer than anyone originally intended.

---

## 👨‍💻 About Me

I am a researcher and software engineer with a background spanning:

- Artificial Intelligence
- Machine Learning & Deep Learning
- Computer Vision
- 3D LiDAR & Point Clouds
- Signal and Sensor Processing
- Telecommunications
- Embedded & IoT Systems
- Software Development
- Teaching & Research

My academic journey began in **Telecommunications Engineering**, where I worked with communication systems, IoT devices, LoRaWAN networks, embedded hardware, and wireless protocols.

Over time, my interests shifted increasingly toward **Artificial Intelligence and intelligent sensing**, particularly the question:

> **How can machines understand what is happening in the physical world using sensors while respecting people's privacy?**

That question now drives much of my research.

---

# 🔬 Research Focus

My current research focuses primarily on:

### 🚶 Human Activity Understanding

Developing AI models capable of understanding pedestrian activities from 3D point clouds.

### 📡 3D LiDAR Perception

Processing LiDAR point clouds for:

- Human detection
- Activity recognition
- Fall detection
- Tracking
- Scene understanding
- Privacy-preserving monitoring

### 🧠 Deep Learning

Exploring architectures including:

- PointNet
- LSTM
- CNNs
- Transformers
- Point Cloud Transformers
- Hybrid neural networks
- Self-Supervised Learning

### 🔄 Synthetic-to-Real Learning

Investigating how models trained using simulated or synthetic data can generalize to real-world sensor measurements.

---

# 🚀 Current Work

## Privacy-Preserving Fall Detection Using 3D LiDAR

One of my current projects investigates **fall detection using real-world 3D LiDAR point clouds**.

Instead of using RGB cameras, the system relies on geometric point-cloud information to distinguish between:

```text
        NON-FALL
           │
           │
           ▼
      Human Activity
           ▲
           │
           │
          FALL
```

The goal is to build intelligent monitoring systems that can recognize potentially dangerous events while providing better privacy than conventional camera-based approaches.

My current work also explores **self-supervised learning** to learn useful representations from unlabeled real-world LiDAR measurements.

---

# 🏙️ Elevated LiDAR Research

A major part of my research involves **elevated LiDAR sensing for pedestrian monitoring**.

A simplified version of the pipeline looks like this:

```text
                   Elevated LiDAR
                        │
                        ▼
                 3D Point Cloud
                        │
                        ▼
               Pedestrian Detection
                        │
                        ▼
                Pedestrian Cropping
                        │
                        ▼
              Point Cloud Processing
                        │
                        ▼
             Deep Learning Classifier
                        │
                        ▼
               Activity Recognition
```

I have worked with both **synthetic and real-world datasets** to study pedestrian activity recognition and model generalization.

---

# 📄 Research & Publications

### IEEE Sensors Journal

**Pedestrian Activity Classification with Hybrid Deep Learning Models Using Elevated LiDAR 3D Point Clouds**

The work investigates deep-learning approaches for pedestrian activity classification using elevated 3D LiDAR sensing.

The research includes:

- Point-cloud deep learning
- Pedestrian activity recognition
- Synthetic LiDAR generation
- Real-world evaluation
- Robustness experiments
- Synthetic-to-real generalization
- Runtime and computational analysis

---

# 🤖 AI & Machine Learning

Some of the architectures and techniques I have worked with include:

```text
Deep Learning
│
├── PointNet
├── LSTM
├── CNN
├── Transformer
├── Point Cloud Transformer
├── Hybrid Neural Networks
└── Self-Supervised Learning
```

For 3D object detection:

```text
3D Detection
│
├── SECOND
├── PV-RCNN
└── OpenPCDet
```

---

# 📡 Sensors & 3D Vision

I enjoy working at the intersection between **physical sensors and AI**.

Some of the tools and platforms I have worked with include:

- Ouster 3D LiDAR sensors
- Ouster SDK
- Open3D
- OpenPCDet
- Blender
- Synthetic LiDAR simulation
- Real-time point-cloud visualization
- Point-cloud preprocessing
- 3D bounding boxes
- Spatial filtering and ROI processing

---

# 🛰️ Earlier Research

Before focusing heavily on AI and LiDAR, I worked on several wireless communication and embedded-system projects.

## LoRaWAN Mobility Prediction

I developed a project using an **LSTM network to predict the future position of a mobile wireless node based on its previous trajectory**.

The broader idea was to use learned mobility patterns to improve network decisions and communication scheduling.

## Ultra-Low-Power Wake-Up Receiver

I also worked on a **wake-up receiver system designed to reduce the energy consumption of wireless devices**.

Instead of keeping the main communication radio continuously active:

```text
Main Radio
    │
    └── SLEEP

Wake-Up Receiver
    │
    └── LISTENING
           │
           ▼
     Wake-Up Packet
           │
           ▼
       MCU Interrupt
           │
           ▼
      Main Radio ON
```

I also worked on packet structures, addressing, communication protocols, and embedded-node behavior.

---

# 👨‍🏫 Teaching

Teaching is another part of my academic experience that I genuinely enjoy.

I have worked with students in areas including:

- Digital Logic
- Electronic Devices
- Programming
- Engineering laboratories
- Embedded systems
- Technical projects

I enjoy helping students move from:

```text
"I have absolutely no idea what this means."
```

to:

```text
"Wait... that's actually pretty simple."
```

That transition is one of my favorite parts of teaching.

---

# 🛠️ Technical Toolbox

### Programming

![Python](https://img.shields.io/badge/Python-Programming-blue?logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-Programming-blue?logo=cplusplus&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-Engineering-orange)

`Python` • `C` • `C++` • `MATLAB`

### Artificial Intelligence

![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red?logo=pytorch&logoColor=white)

`PyTorch` • `Deep Learning` • `Machine Learning` • `Transformers` • `Self-Supervised Learning`

### 3D / Computer Vision

`Open3D` • `OpenPCDet` • `PointNet` • `PV-RCNN` • `SECOND` • `Point Cloud Transformers`

### Sensors & Simulation

`Ouster SDK` • `3D LiDAR` • `Blender` • `Synthetic Data Generation`

### Research

`Scientific Computing` • `Experimental Design` • `Data Visualization` • `Technical Writing` • `Research Communication`

---

# 🧩 How I Like to Work

Most projects I enjoy follow roughly this pattern:

```text
Interesting Problem
        │
        ▼
Research Question
        │
        ▼
Collect / Generate Data
        │
        ▼
Build Something
        │
        ▼
Break Something
        │
        ▼
Figure Out Why
        │
        ▼
Build It Better
        │
        ▼
Evaluate
        │
        ▼
Publish / Present / Teach
```

The **“break something”** stage tends to be particularly reliable.

---

# 🌱 Currently Exploring

I am particularly interested in:

- Self-Supervised Learning for 3D data
- Foundation models for point clouds
- Synthetic-to-real transfer
- Privacy-preserving sensing
- Human-centered AI
- Intelligent healthcare monitoring
- Real-time LiDAR perception
- Multimodal sensing
- Robust AI systems

---

# 🎯 Research Interests

```text
Artificial Intelligence
        +
3D Computer Vision
        +
LiDAR Sensing
        +
Deep Learning
        +
Human Activity Understanding
        +
Privacy
```

My long-term interest is in building **intelligent sensing systems that can understand the physical world accurately, efficiently, and responsibly**.

---

# 🤝 Open to Collaboration

I am always interested in conversations and potential collaborations involving:

- Artificial Intelligence
- Machine Learning
- Computer Vision
- LiDAR
- 3D Point Clouds
- Robotics and sensing
- Healthcare AI
- Human activity recognition
- Synthetic data
- Intelligent transportation
- Privacy-preserving sensing
- Research software development

---

# 📌 Featured Projects

### 🔹 LiDAR Fall Detection
Real-world 3D LiDAR fall/non-fall classification using deep learning and self-supervised representation learning.

### 🔹 Elevated LiDAR Activity Recognition
Deep-learning models for pedestrian activity recognition from elevated 3D LiDAR point clouds.

### 🔹 Synthetic LiDAR Generation
Generating labeled LiDAR scenes using Blender for training and evaluating 3D perception systems.

### 🔹 3D Pedestrian Detection
Pedestrian detection pipelines using SECOND, PV-RCNN, and OpenPCDet.

### 🔹 LoRaWAN Mobility Prediction
LSTM-based prediction of mobile-node trajectories in wireless networks.

### 🔹 Wake-Up Receiver
Low-power wireless communication architecture using an always-listening wake-up receiver.

---

# 📊 GitHub

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&hide_border=true)

</div>

> Replace `YOUR_GITHUB_USERNAME` above with your actual GitHub username.

---

# 📫 Let's Connect

I am happy to connect with researchers, engineers, students, and anyone interested in AI and intelligent sensing.

📧 **Email:** [nawfal.guefrachi@mst.edu](mailto:nawfal.guefrachi@mst.edu)

💼 **LinkedIn:** [LinkedIn Profile](https://www.linkedin.com/in/nawfal-guefrachi/)

🎓 **Google Scholar:** [Google Scholar Profile](https://scholar.google.com/citations?user=qNGBEkMAAAAJ&hl=fr&inst=15611845720231691803&oi=ao)

💻 **GitHub:** [GitHub Profile](https://github.com/nawfalgf)

---

<div align="center">

### Thanks for stopping by! 👋

**Research • Build • Teach • Repeat**

</div>
