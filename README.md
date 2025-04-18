# mecanum_control_debug

This repository was created to request help with configuring a mecanum-wheeled robot in **ROS 2 Humble** using **Gazebo Ignition** and the `mecanum_drive_controller` from the `ros2_controllers` package.

I'm developing a mobile robot with **four Mecanum wheels**, inspired by the layout of the **KUKA youBot**. The goal is to achieve full omnidirectional control using `ros2_control` and `gazebo_ros2_control`. All URDF and configuration files were written manually.

While the controller loads without errors and velocity commands are being published, the robot **does not move at all** — not forward, sideways, or rotating. I understand that some movement imperfections are expected due to the non-square footprint of the platform, but in my case the control simply isn’t working at all.

## ❗ What I need help with

I would really appreciate help understanding how to properly describe a Mecanum-based robot in the URDF (including joint directions, wheel orientation, and transmissions), and how to configure the YAML parameters for the `mecanum_drive_controller` so it behaves correctly in simulation.

## 📁 Repository structure

```
mecanum_control_debug/
├── description/
│   ├── urdf/        # Robot description files (URDF/Xacro)
│   └── launch/      # Launch file to spawn robot in Gazebo Ignition
├── controller/
│   ├── config/      # YAML config for mecanum_drive_controller
│   └── launch/      # Launch file to start ros2_control
```

## 🙏 Looking for feedback on:

- Correct URDF structure for Mecanum wheels
- Joint axis directions and positioning
- Required ros2_control transmission setup
- Expected controller parameters for correct omnidirectional movement

Feel free to open an issue or leave a comment if you spot anything wrong or have suggestions.

Thanks in advance!
