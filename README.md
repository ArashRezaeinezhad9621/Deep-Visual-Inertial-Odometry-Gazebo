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

<table align="center">
  <tr>
    <td><img src="Images/Dataset_Thesis.gif"/></td>
  </tr>
</table>
<br clear="left"/>

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

<table align="center">
  <tr>
    <td><img src="Images/Environment.png" width="750"/></td>
  </tr>
  <tr>
    <td><img src="Images/Sample_Images.png" width="750"/></td>
  </tr>
</table>
<br clear="left"/>

## 🏗 Methodology

The proposed architecture combines spatial and temporal learning:

<table align="center">
  <tr>
    <td><img src="Images/Proposed_Networks.png" width="750"/></td>
  </tr>
</table>

### 🔹 Feature Extraction
- Pretrained VGG16 used to extract visual features from consecutive frames  
<table align="center">
  <tr>
    <td><img src="Images/Convolutional_Layer.png" width="600"/></td>
  </tr>
</table>  
### 🔹 Motion Representation
- Features from two frames are combined to capture motion dynamics
### 🔹 Temporal Modeling
- ConvLSTM + LSTM layers learn temporal dependencies
### 🔹 Output
- 7-dimensional vector:
- 3D position (x, y, z)
- 4D orientation (quaternion)

## 📊 Results

The proposed method was evaluated against baseline approaches such as VINet.
<table align="center">
  <tr>
    <td><img src="Images/Trajectories.png" width="750"/></td>
  </tr>
</table>


<table align="center">
  <tr>
    <td align="center"><img src="Images/Results_Tables.png" width="600"/></td>
  </tr>
</table>

## 🔮 Future Work
- Integrate Kalman filtering for improved heading accuracy
- Extend to multi-sensor fusion (e.g., GPS, magnetometer)
- Validate on real-world datasets (Sim-to-Real transfer)
- Improve robustness in challenging environments
- Expand dataset diversity and complexity

## 👤 Author

Arash Rezaeinezhad  
M.Sc. in Electronics  
Deep Learning & Robotics Enthusiast  
