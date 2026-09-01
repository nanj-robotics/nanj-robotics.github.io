---
permalink: /
title: ""
excerpt: "Robotics & Autonomous Systems Engineer focused on embodied AI — robot manipulation, mobile navigation, perception, and robot learning."
author_profile: true
redirect_from:
  - /about/
  - /about.html
---
<span class='anchor' id='about-me'></span>
# Robotics & Autonomous Systems Engineer
I am a robotics engineer focused on **embodied AI**, working across mobile navigation, robot manipulation, visual perception, reinforcement learning. My projects are built on the **ROS 2** (**SLAM / Nav2**, **MoveIt 2**), with visual perception (**YOLOv11-Seg**, **FoundationPose**) and reinforcement learning (**Isaac Gym**, **PPO**) for locomotion.
Beyond real‑robot systems, I am gradually expanding into **Isaac Sim / Isaac Lab**, world models, and vision‑language‑action (VLA) models, working toward broader and more generalizable embodied intelligence.
I am currently pursuing a **B.Eng. in Electrical and Electronic Engineering** at the **University of Bristol** (2024–2027), on track for First Class Honours with an average of 80+ and ranking in the **top 1%** of my cohort.
[GitHub](https://github.com/nanj-robotics) · [LinkedIn](https://www.linkedin.com/in/qinnan-j-a13714355/)

# 🔥 News
- *2026.09*: Completed **RoboMantis** — Dual 7‑DOF robotic arms with YOLOv11‑Seg + FoundationPose vision‑based grasping, zero‑torque gravity‑compensated mode for VLA data collection.
- *2026.08*: Completed **GeniCraner** — 7‑DOF robot arm with YOLOv11‑Seg + FoundationPose vision‑based grasping, including zero‑torque mode for VLA data collection.
- *2026.08*: Released **dual_motor_sync** — dual Robstride RS03 motor synchronous control over CAN, achieving **0.01°** synchronization error.
- *2026.07*: Completed **GeniRover** — differential‑drive mobile robot with GNSS‑RTK, MPPI local planner, iteratively field‑tested in outdoor environments with promising real‑world navigation results, deployed on NVIDIA Jetson AGX Orin.
- *2026.04*: Completed FPGA peak detection prototyping project at the University of Bristol.
- *2024.09*: Enrolled in the University of Bristol, School of Electrical, Electronic and Mechanical Engineering.

# 📝 Selected Projects
<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Dual‑Arm Robot</div><video autoplay loop muted playsinline preload="metadata" aria-label="RoboMantis dual 7‑DOF robot arms with vision‑based grasping"><source src="images/RoboMantis.mp4" type="video/mp4"></video></div></div>
<div class='paper-box-text' markdown="1">
**Dual 7‑DOF Robot Arms with YOLOv11‑Seg + FoundationPose Vision‑Based Grasping (RoboMantis)** · *Aug. 2026 – Sep. 2026*

**Qinnan Jiang**
- Built a dual 7‑DOF magnetic‑grasping robotic arm platform with Robstride series motors over CAN bus, including dual‑arm URDF/Xacro modeling and separated **ros2_control** hardware interfaces for left and right manipulator.
- Implemented vision‑based grasping pipeline: **YOLOv11‑Seg** instance segmentation + **FoundationPose** 6D object pose estimation, hand‑eye calibration for fixed external RGB‑D camera.
- Deployed coordinated dual‑arm motion planning via **MoveIt 2**, developed independent zero‑torque gravity‑compensated controller for each arm supporting kinesthetic teaching and VLA dataset collection.
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ROS 2 / Navigation</div><img src='images/geni_rover.jpg' alt="GeniRover autonomous navigation differential‑drive mobile robot" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
**Autonomous Navigation Differential‑Drive Mobile Robot (GeniRover)** · *Jun. 2026 – Jul. 2026*

**Qinnan Jiang**
- Custom differential‑drive mobile robot supporting in‑place rotation; hardware includes CAN‑bus hub motors, 2D LiDAR, RGB‑D camera, IMU and **GNSS‑RTK** module, deployed on **NVIDIA Jetson AGX Orin**.
- Implemented complete ROS2 navigation stack: **SLAM Toolbox** mapping, Nav2 with AMCL localization, and **MPPI** as local planner. 
- Fused wheel odometry, IMU and RTK pose data through **robot_localization EKF** to generate stable robot base state estimation.
- Conducted iterative field tests in outdoor unstructured environments, obtained promising real‑world navigation performance. Supports manual tele‑op, map‑based autonomous navigation and dynamic obstacle avoidance.
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Reinforcement Learning</div><video autoplay loop muted playsinline preload="metadata" aria-label="Quadruped‑wheeled robot RL locomotion training in Isaac Gym"><source src="images/quadruped_rl.mp4" type="video/mp4"></video></div></div>
<div class='paper-box-text' markdown="1">
**RL Locomotion for a Custom Quadruped‑Wheeled Robot (PPO, Isaac Gym)** · *2025 – Present (Ongoing)*

**Qinnan Jiang**
- Training a custom **quadruped‑wheeled robot** for robust locomotion using **PPO** in **NVIDIA Isaac Gym**, targeting walking, running, and jumping via sim2real transfer.
- **Full‑stack development**: SolidWorks assembly modeling → URDF generation → RL training pipeline design → sim2real deployment.
- Long‑term goal: mount two robotic arms for mobile manipulation; next step: migrate the training pipeline to **Isaac Lab**. Ongoing since 2025, sim2real transfer in progress.
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Motor Control</div><video autoplay loop muted playsinline preload="metadata" aria-label="Dual Robstride RS03 motor synchronous control demonstration"><source src="images/dual_motor_sync.mp4" type="video/mp4"></video></div></div>
<div class='paper-box-text' markdown="1">
**Dual Motor Synchronous Control for High‑Load Robotic Mechanisms** · *Aug. 2026*

**Qinnan Jiang**
- Built a ROS 2 C++ package for precise mirrored synchronization of two **Robstride RS03** motors over CAN bus for high‑load dual‑motor joints.
- Implemented **cosine trajectory planning** with 500 Hz CAN transmission in MIT PD torque mode, achieving **0.01°** synchronization error.
- Eliminated torque interruption for seamless motion sequences; fully configurable via command‑line arguments.
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">FPGA</div><img src='images/fpga_peak_detection.jpg' alt="FPGA peak detection prototyping on Artix‑7" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
**FPGA Peak Detection Prototyping (Artix‑7, VHDL)** · *Jan. 2026 – Apr. 2026*
**Qinnan Jiang**, Sangwon, Yu Chen, Kyan Xu, Yutong Shi
- Designed a **peak detection system** for signed numbers on **Xilinx Artix‑7 FPGA** using **VHDL** with RTL‑coding style.
- Developed an **FSM controller** and two‑way handshaking protocol to synchronize high‑speed FPGA logic with UART communication, ensuring zero data loss.
- 5‑member team: I co‑developed the Command Processor module (3 members), 2 members handled the Data Processor.
</div></div>

# 🏅 Honors and Awards
- *2024 – Present*: **Top 1%** in EEE cohort, on track for **First Class Honours** (avg 80+), University of Bristol.

# 📖 Educations
- *Sep. 2024 – Jun. 2027 (expected)*: **B.Eng. in Electrical and Electronic Engineering**, University of Bristol, Bristol, UK. **First Class Honours track (avg 80+).**
