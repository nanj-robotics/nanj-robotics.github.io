---
permalink: /
title: ""
excerpt: "Robotics & Autonomous Systems Engineer focused on embodied AI — robot manipulation, mobile navigation, motor control, and RL locomotion."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<span class='anchor' id='about-me'></span>
# Robotics & Autonomous Systems Engineer

I build complete robot systems end-to-end — from mechanical design and URDF modeling, to low-level motor control and high-level autonomy stacks. My work spans **ROS 2**, **SLAM / Nav2**, **MoveIt 2 manipulation**, visual perception (**YOLOv11-Seg**, **FoundationPose**), and reinforcement learning for locomotion (**Isaac Gym**, **PPO**).

I am currently pursuing a **B.Eng. in Electrical and Electronic Engineering** at the **University of Bristol** (2024–2027), on track for First Class Honours with an average of 80+ and ranking in the **top 1%** of my cohort.

Most projects below are **solo developed**; team collaborations are noted individually.

[GitHub](https://github.com/nanj-robotics) · [LinkedIn](https://www.linkedin.com/in/qinnan-j-a13714355/)

# 🔥 News
- *2026.08*: Completed **GeniCraner** — 7-DOF robot arm with YOLOv11-Seg + FoundationPose vision-based grasping, including zero-torque mode for VLA data collection.
- *2026.08*: Released **dual_motor_sync** — dual Robstride RS03 motor synchronous control over CAN, achieving **0.01°** synchronization error.
- *2026.07*: Completed **GeniRover** — autonomous navigation & obstacle-avoidance differential-drive mobile robot, deployed on NVIDIA Jetson AGX Orin.
- *2026.04*: Completed FPGA peak detection prototyping project at the University of Bristol.
- *2024.09*: Enrolled in the University of Bristol, Department of Electrical and Electronic Engineering.

# 📝 Selected Projects

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Robot Arm</div><img src='images/geni_craner.jpg' alt="GeniCraner 7-DOF robot arm with vision-based grasping" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
**7-DOF Robot Arm with YOLOv11-Seg + FoundationPose Vision-Based Grasping** · *Jul. 2026 – Aug. 2026*
**Qinnan Jiang**
- Designed and built a 7-DOF robotic arm with a magnetic iron-hex-socket end-effector; actuated by 7 Robstride Dynamics motors (1×RS06, 1×RS03, 5×RS00) over CAN 2.0 at 1 Mbps.
- Implemented the vision-based grasping pipeline: **YOLOv11-Seg** for instance segmentation → **FoundationPose** for 6D pose estimation → hand-eye transform (eye-to-hand, calibrated with **easy_handeye2**) → **MoveIt 2** motion planning & execution.
- Developed **zero-torque mode** (gravity-compensated free-drag) as a `ros2_control` controller using **Pinocchio RNEA** for gravity compensation plus adaptive damping (Kp=0), enabling kinesthetic teaching and VLA data collection.
- Built full ROS 2 stack: custom `ros2_control` hardware interface, S-curve trajectory generator, URDF/Xacro model with STL meshes, and calibration verification script.
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Motor Control</div><video width="100%" autoplay loop muted playsinline preload="metadata" aria-label="Dual Robstride RS03 motor synchronous control demonstration"><source src="images/dual_motor_sync.mp4" type="video/mp4"></video></div></div>
<div class='paper-box-text' markdown="1">
**Dual Motor Synchronous Control for High-Load Robotic Mechanisms** · *Aug. 2026*
**Qinnan Jiang**
- Developed a ROS 2 C++ package for precise mirrored synchronization of two **Robstride RS03** motors over CAN bus, targeting high-load dual-motor joint configurations where a single actuator cannot deliver sufficient torque.
- Implemented **cosine trajectory planning** (zero velocity at start/end) with **500 Hz** back-to-back CAN frame transmission; achieved synchronization error down to **0.01°**.
- Motors run in **MIT mode** (PD torque loop): time-parameterized trajectory sent every 2 ms, speed controlled by `duration`, kp/kd only control tracking accuracy.
- Eliminated torque interruption for seamless successive motion sequences; fully configurable via command-line arguments (angle, time, kp, kd, CAN channel, motor IDs, hold mode).
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ROS 2 / Navigation</div><img src='images/geni_rover.png' alt="GeniRover autonomous navigation differential-drive mobile robot" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
**Autonomous Navigation & Obstacle-Avoidance Differential-Drive Mobile Robot (GeniRover)** · *Jun. 2026 – Jul. 2026*
**Qinnan Jiang**
- Built a four-wheel differential-drive robot with CAN-controlled hub motors (gear ratio 5.2:1), Wheeltec 2D LiDAR, Orbbec Gemini 336L RGB-D camera, and Yahboom 9-axis IMU.
- Implemented the full autonomy stack: **SLAM Toolbox** for online mapping → **Nav2** (AMCL global localization + DWB controller + costmap obstacle/inflation layers) for path planning & real-time obstacle avoidance.
- Fused wheel odometry with IMU yaw rate via **robot_localization EKF**, outputting filtered odometry and `odom → base_footprint` TF for robust state estimation.
- Deployed the entire ROS 2 stack in **Docker** on **NVIDIA Jetson AGX Orin** with GPU passthrough; USB devices passed through with `--device` flags and stable udev symlinks.
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Reinforcement Learning</div><video width="100%" autoplay loop muted playsinline preload="metadata" aria-label="Quadruped-wheeled robot RL locomotion training in Isaac Gym"><source src="images/quadruped_rl.mp4" type="video/mp4"></video></div></div>
<div class='paper-box-text' markdown="1">
**RL Locomotion for a Custom Quadruped-Wheeled Robot (PPO, Isaac Gym)** · *2025 – Present (Ongoing)*
**Qinnan Jiang**
- Designing and training a custom **quadruped-wheeled robot** for robust locomotion using **PPO** in **NVIDIA Isaac Gym**; targeting walking, running, and jumping with high robustness and precision via sim2sim and sim2real transfer.
- **Full-stack solo development**: from SolidWorks assembly modeling and URDF generation, to RL training pipeline design, reward shaping, and sim2real deployment on physical hardware.
- Long-term goal: mount two robotic arms on the quadruped platform to enable **mobile manipulation** capabilities.
- Work conducted during academic breaks (ongoing since 2025); sim2real transfer and hardware deployment in progress.
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">FPGA</div><img src='images/fpga_peak_detection.jpg' alt="FPGA peak detection prototyping on Artix-7" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
**FPGA Peak Detection Prototyping (Artix-7, VHDL)** · *Jan. 2026 – Apr. 2026*
**Qinnan Jiang**, Sangwon, Yu Chen, Kyan Xu, Yutong Shi
- Designed and implemented a **peak detection system for signed numbers** on a **Xilinx Artix-7 FPGA** using **VHDL** with RTL-coding style.
- Developed a robust **Finite State Machine (FSM)** controller to coordinate data flow between the Data Processor and UART-based command interfaces.
- Implemented a reliable **two-way handshaking protocol** to synchronize high-speed FPGA logic with slower UART communication, ensuring **zero data loss**.
- Collaborated in a 5-member team: 3 members (including me) responsible for the Command Processor, 2 members for the Data Processor.
</div></div>

# 🏅 Honors and Awards
- *2024 – Present*: **Top 1%** in EEE cohort, University of Bristol.
- *2024 – Present*: On track for **First Class Honours** (average 80+), University of Bristol.

# 📖 Educations
- *Sep. 2024 – Jun. 2027 (expected)*: **B.Eng. in Electrical and Electronic Engineering**, University of Bristol, Bristol, UK. **First Class Honours track (avg 80+), Top 1% in cohort.**
