# Full-State Trajectory Tracking for a Coupled Quadrotor-Manipulator System using Sliding Mode Control

## Overview

This repository contains a Python-based simulation for the dynamic modeling and control of a 6-DOF aerial manipulator, which consists of a quadrotor UAV equipped with a 2-DOF rigid robotic arm. The primary goal of this project is to design and implement a robust nonlinear controller capable of achieving high-precision trajectory tracking for all 8 degrees of freedom (6 for the quadrotor, 2 for the manipulator).

The dynamic model is based on the Newton-Euler formulation presented in the paper "A New Quadrotor Manipulation System: Modeling and Point-to-Point Task Space Control" by Khalifa & Fanni (2017). The work explores the significant challenges of controlling such systems, particularly the strong, nonlinear dynamic coupling between the manipulator's motion and the stability of the aerial platform.

## Key Features

- **Full 16-State Dynamic Model:** A comprehensive simulation of the coupled dynamics involving the quadrotor's translational/rotational states and the manipulator's joint states.
- **Robust Nonlinear Control:** A Sliding Mode Controller (SMC) was designed from first principles to ensure robust and stable tracking performance, even with the system's complex internal dynamics.
- **Full-State Trajectory Tracking:** The controller successfully tracks complex, time-varying trajectories for all 8 degrees of freedom simultaneously, including the quadrotor's 3D path and the manipulator's joint movements.
- **Python Implementation:** The entire simulation and control logic are implemented from scratch in Python using NumPy and Matplotlib.

## Simulation Results

The controller's effectiveness is demonstrated through a challenging trajectory where the quadrotor follows a circular path while the manipulator arm performs a sinusoidal motion.

#### 3D Trajectory Tracking
The following plot shows the quadrotor successfully converging to and tracking the desired circular path at a constant altitude.

![3D Trajectory Plot](URL_TO_YOUR_3D_PLOT_IMAGE)

#### State-wise Tracking Performance
These plots illustrate the high-precision tracking for each of the 8 degrees of freedom. Notably, the roll (phi) and pitch (theta) angles are automatically adjusted by the controller to generate the necessary lateral forces for circular motion, demonstrating the controller's correct physical behavior.

![8-Panel State Plot](URL_TO_YOUR_8_PANEL_PLOT_IMAGE)

*(**نکته برای شما:** لطفاً عکس‌های نمودارهای موفق خود را در گیت‌هاب آپلود کرده و URL آن‌ها را در دو خط بالا جایگزین کنید.)*

## How to Run

1.  Ensure you have Python 3, `numpy`, and `matplotlib` installed.
2.  Clone this repository.
3.  Run the main Python script:
    ```bash
    python Aerial Manipulator usingSliding Mode Control.py
    ```

## Future Work & Research Interests

This project establishes a strong foundation in the dynamics and model-based control of aerial manipulators. My current research interest is to extend this framework to address the next generation of aerial manipulation challenges, perfectly aligning with the objectives of the **DOMINANTS project**.

Future research directions include:

-   **Transitioning from Rigid to Soft Robotics:** Replacing the rigid manipulator model with a **continuum model** (e.g., using Cosserat rod theory or FEM) to investigate the benefits of compliance, safety, and adaptability in aerial grasping.
-   **Model-Based Design & Optimization:** Developing **optimization strategies** for the structural parameters of a soft manipulator to enhance its dexterity, reach, and payload capacity.
-   **Advanced Control Strategies:** Exploring adaptive and learning-based control techniques to handle the high nonlinearities and uncertainties inherent in soft robotic systems.

---
