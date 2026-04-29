# 🚀 Deep Visual-Inertial Odometry using Gazebo Simulation

<p align="justify">
A deep learning-based framework for visual-inertial odometry (VIO) using a custom dataset generated in Gazebo. This project integrates monocular images and IMU data with a CNN-RNN architecture to estimate robot trajectory with improved accuracy.
</p>

## 🧠 Overview

<p align="justify">
Visual-Inertial Odometry (VIO) plays a critical role in autonomous navigation. Traditional methods often struggle in dynamic environments and require careful manual tuning.
</p>

In this project, we propose a learning-based VIO system that:

- Uses a custom dataset generated in Gazebo
- Extracts spatial features using a VGG16-based CNN
- Learns temporal dependencies using LSTM / ConvLSTM
- Fuses image and IMU data
- Achieves significant improvement in trajectory estimation accuracy

📉 **Result**: Mean Squared Error (MSE) improved from **4.99 → 0.63**


## 🗂 Dataset (Gazebo Simulation)

A custom dataset was created using the Gazebo simulator to ensure:

- Controlled environment
- High similarity between training and testing data
- Flexible sensor integration

### 🔧 Sensors Used
- Monocular Camera
- IMU (Accelerometer + Gyroscope)

### 📦 Dataset Includes
- Image sequences
- IMU measurements
- Ground truth trajectories

![Dataset Sample](media/dataset_sample.png)

![Gazebo Simulation](media/gazebo_simulation.gif)
