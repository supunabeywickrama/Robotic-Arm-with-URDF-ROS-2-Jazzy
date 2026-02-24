# Create and Visualize a Robotic Arm with URDF – ROS 2 Jazzy

![OS](https://img.shields.io/ubuntu/v/ubuntu-wallpapers/noble)
![ROS_2](https://img.shields.io/ros/v/jazzy/rclcpp)
![License](https://img.shields.io/badge/license-BSD--3--Clause-blue)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/73304991-a061-4096-8046-14de332297d0" />


## 📌 Project Overview

[![Demo Video](https://img.shields.io/badge/Demo%20Video-Play-brightgreen?style=for-the-badge)](https://drive.google.com/file/d/13OEK-YXBt-oT0lRJwvT69zpwy0lL9KAe/view?usp=sharing)

This project demonstrates how to create and visualize a real-world robotic arm using **URDF/XACRO in ROS 2 Jazzy**.

We model the **myCobot 280 robotic arm by Elephant Robotics** using URDF (Unified Robot Description Format), then visualize it in **RViz** using `urdf_tutorial`.

This project gives the robot a **digital body** that ROS 2 tools can understand for:

- ✅ Simulation  
- ✅ Motion planning  
- ✅ Sensor integration  
- ✅ TF transformations  
- ✅ Collision checking  

---

## 🧠 What is URDF?

URDF (Universal Robot Description Format) is an XML-based format that describes a robot’s physical structure.

A robot body consists of:

### 🔹 Links
Rigid parts of the robot (bones)

### 🔹 Joints
Connections between links that allow motion

Joint types include:
- `revolute` (rotational motion)
- `fixed` (no motion)
- `prismatic` (linear motion)

URDF defines:
- Geometry
- Mass
- Inertia
- Joint limits
- Visual meshes
- Collision shapes

---

## 🏗 Project Structure

<img width="461" height="552" alt="image" src="https://github.com/user-attachments/assets/69d15edd-6171-41b7-9751-4bfa9035cd4a" />


---

## ⚙️ Installation & Setup

### 1️⃣ Create Workspace

```bash
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src
```
---

## 2️⃣ Create Packages

mkdir mycobot_ros2
cd mycobot_ros2

ros2 pkg create --build-type ament_cmake --license BSD-3-Clause mycobot_description
ros2 pkg create --build-type ament_cmake --license BSD-3-Clause mycobot_ros2

---

## 3️⃣ Create Folder Structure

mkdir -p ~/ros2_ws/src/mycobot_ros2/mycobot_description/meshes/mycobot_280/visual
mkdir -p ~/ros2_ws/src/mycobot_ros2/mycobot_description/urdf/control
mkdir -p ~/ros2_ws/src/mycobot_ros2/mycobot_description/urdf/mech
mkdir -p ~/ros2_ws/src/mycobot_ros2/mycobot_description/urdf/sensors
mkdir -p ~/ros2_ws/src/mycobot_ros2/mycobot_description/urdf/robots


