---
title: "Distributed Quadrotor Swarm Trajectory Planning"
date: 2026-09-01
collection: logs
permalink: /logs/2026-09-01-quadrotor-trajectory-setup/
excerpt: "Notes on setting up Crazyswarm2 with Qualisys MoCap and initial trajectory tracking benchmarks in ROS 2."
tags:
  - ros2
  - aerial-robotics
  - crazyflie
---


### Objective
Documenting initial setup hurdles and parameter tuning for multi-agent Crazyflie flight tests using the Qualisys motion capture system.

### Hardware & Software Stack
* **Firmware:** Crazyflie 2026.02
* **ROS Version:** ROS 2 Humble
* **Mocap Driver:** `qualisys_mocap_ros` via UDP stream

### Issues Encountered
1. Latency spikes over WiFi when broadcasting position setpoints exceeding 100 Hz.
2. Coordinate transform discrepancies between NED (MoCap world) and ENU (ROS frame).