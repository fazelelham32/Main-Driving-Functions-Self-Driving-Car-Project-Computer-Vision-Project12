# Complete Self-Driving Car | Autonomous Driving with Python, OpenCV, Flask & Socket.IO

> An end-to-end autonomous driving project that connects a trained deep learning steering model with the **Udacity Self-Driving Car Simulator** using **Python**, **Flask**, **Socket.IO**, **OpenCV**, and **Keras** for real-time vehicle control.

---

# Project Overview

This project demonstrates the deployment of an autonomous driving model inside a driving simulator. A Python application (`drive.py`) communicates with the simulator, receives real-time camera images, preprocesses each frame, predicts the steering angle using a trained deep learning model, and sends steering and throttle commands back to the simulator for autonomous navigation.

---

# Project Objective

The objective of this project is to build the driving pipeline that enables a trained deep learning model to control a simulated self-driving vehicle without manual intervention.

---

# Project Workflow

```text
Udacity Simulator
        │
        ▼
Front Camera Image
        │
        ▼
Socket.IO Communication
        │
        ▼
Image Preprocessing
        │
        ▼
Deep Learning Model
        │
        ▼
Steering Angle Prediction
        │
        ▼
Throttle Calculation
        │
        ▼
Control Commands
        │
        ▼
Autonomous Vehicle
```

---

# System Architecture

```text
Simulator
      │
      ▼
Socket.IO Server
      │
      ▼
drive.py
      │
      ├────────► Image Preprocessing
      │
      ├────────► Steering Prediction
      │
      ├────────► Speed Control
      │
      ▼
Vehicle Commands
```

---

# Project Components

| Component | Description |
|------------|-------------|
| Python | Main application |
| Flask | Backend server |
| Socket.IO | Real-time communication |
| OpenCV | Image processing |
| Keras | Model inference |
| Udacity Simulator | Autonomous driving environment |

---

# Main Functional Modules

## Socket.IO Server

The project initializes a Socket.IO server to establish continuous communication between the autonomous driving application and the simulator.

---

## Flask Server

A lightweight Flask application is used to host the communication interface.

---

## Image Acquisition

The simulator continuously sends front-camera images to the Python application during driving.

---

## Image Preprocessing

Each incoming image is processed before inference.

The preprocessing stage prepares images in the format expected by the trained model.

---

## Steering Prediction

The trained Keras model predicts the steering angle from every processed frame.

---

## Speed Control

A predefined speed limit is maintained while driving.

Throttle values are generated together with steering predictions before being transmitted back to the simulator.

---

## Vehicle Control

Predicted steering angle and throttle are immediately sent back to the simulator through Socket.IO.

This creates a continuous closed-loop autonomous driving system.

---

# Processing Pipeline

```text
Camera Frame
      │
      ▼
Receive Image
      │
      ▼
Preprocess Image
      │
      ▼
Deep Learning Model
      │
      ▼
Predict Steering
      │
      ▼
Calculate Throttle
      │
      ▼
Send Control Commands
```

---

# Project Features

- Autonomous vehicle control
- Real-time steering prediction
- Real-time simulator communication
- Flask server integration
- Socket.IO communication
- Image preprocessing pipeline
- Deep learning model inference
- Continuous vehicle control
- Speed management
- Simulator deployment

---

# Runtime Flow

```text
Start Flask Server

        │

Start Socket.IO

        │

Launch Simulator

        │

Receive Camera Images

        │

Run Deep Learning Model

        │

Predict Steering

        │

Generate Throttle

        │

Control Vehicle
```

---

# Installation

## Clone Repository

```bash
git clone <repository-url>
```

---

## Create Environment

```bash
conda create -n sdcar python=3.7 -y
```

---

## Activate Environment

```bash
conda activate sdcar
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Start Autonomous Driving

```bash
python drive.py
```

---

## Launch Simulator

Open the Udacity Self-Driving Car Simulator and switch to **Autonomous Mode**.

---

# Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Application logic |
| Flask | Backend server |
| Socket.IO | Simulator communication |
| OpenCV | Image processing |
| TensorFlow / Keras | Steering prediction |
| Udacity Simulator | Autonomous driving simulation |

---

# Driving Pipeline

```text
Simulator
      │
      ▼
Camera Image
      │
      ▼
Preprocessing
      │
      ▼
Prediction Model
      │
      ▼
Steering Angle
      │
      ▼
Throttle
      │
      ▼
Vehicle Control
```

---

# Project Output

The completed application is capable of:

- Receiving live camera frames from the simulator
- Processing incoming images
- Predicting steering angles
- Maintaining vehicle speed
- Sending real-time driving commands
- Driving autonomously without manual control

---

# Project Assets

- `drive.py`
- Deep learning steering model
- Flask server
- Socket.IO communication
- Image preprocessing pipeline
- Udacity simulator integration

---

# Project Screenshot

> Example image included in the project repository.

![Self-Driving Car Sample](test_image.jpg)

> If you keep the original repository structure, place `test_image.jpg` in the project root or update the image path accordingly.

---

# Final Outcome

This project demonstrates the successful deployment of a deep learning-based autonomous driving pipeline by integrating a trained steering model with the Udacity Self-Driving Car Simulator. The application receives real-time camera images, preprocesses each frame, predicts steering angles, controls vehicle speed, and continuously sends driving commands through Flask and Socket.IO, enabling fully autonomous driving inside the simulation environment.
