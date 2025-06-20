# Full-State Trajectory Tracking for a Coupled Quadrotor-Manipulator System using Sliding Mode Control

## Overview

This repository contains a Python-based simulation for the dynamic modeling and control of a 6-DOF aerial manipulator, which consists of a quadrotor UAV equipped with a 2-DOF rigid robotic arm. The primary goal of this project is to design and implement a robust nonlinear controller capable of achieving high-precision trajectory tracking for all 8 degrees of freedom (6 for the quadrotor, 2 for the manipulator).

The dynamic model is based on the Newton-Euler formulation presented in the paper "A New Quadrotor Manipulation System: Modeling and Point-to-Point Task Space Control". The work explores the significant challenges of controlling such systems, particularly the strong, nonlinear dynamic coupling between the manipulator's motion and the stability of the aerial platform.

## Key Features

- **Full 16-State Dynamic Model:** A comprehensive simulation of the coupled dynamics involving the quadrotor's translational/rotational states and the manipulator's joint states.
- **Robust Nonlinear Control:** A Sliding Mode Controller (SMC) was designed from first principles to ensure robust and stable tracking performance, even with the system's complex internal dynamics.
- **Full-State Trajectory Tracking:** The controller successfully tracks complex, time-varying trajectories for all 8 degrees of freedom simultaneously, including the quadrotor's 3D path and the manipulator's joint movements.
- **Python Implementation:** The entire simulation and control logic are implemented from scratch in Python using NumPy and Matplotlib.

## Simulation Results

The controller's effectiveness is demonstrated through a challenging trajectory where the quadrotor follows a circular path while the manipulator arm performs a sinusoidal motion.

#### 3D Trajectory Tracking
The following plot shows the quadrotor successfully converging to and tracking the desired circular path at a constant altitude.

![3D Trajectory Plot](https://github.com/MirMikael/Full-State-Trajectory-Tracking-for-a-Coupled-Quadrotor-Manipulator-System-using-Sliding-Mode-Control/blob/main/3D.png?raw=true)


#### Manipulator Joints Tracking Performance

This plot demonstrates the controller's high-performance tracking for the two manipulator joints. It is important to note that the joints (θ₁ and θ₂) are accurately following their desired sinusoidal trajectories simultaneously as the quadrotor base executes its own complex path. This highlights the controller's ability to effectively manage the system's coupled dynamics and reject disturbances caused by the base's motion.

![8-Panel State Plot](https://github.com/MirMikael/Full-State-Trajectory-Tracking-for-a-Coupled-Quadrotor-Manipulator-System-using-Sliding-Mode-Control/blob/main/manipulator.png)


## How to Run

1.  Ensure you have Python 3, `numpy`, and `matplotlib` installed.
2.  Clone this repository.
3.  Run the main Python script:
    ```bash
    python Aerial Manipulator usingSliding Mode Control.ipynb
    ```

## Future Work & Research Interests

This project establishes a strong foundation in the dynamics and model-based control of aerial manipulators. My current research interest is to extend this framework to address the next generation of aerial manipulation challenges, perfectly aligning with the objectives of the **DOMINANTS project**.

Future research directions include:

-   **Transitioning from Rigid to Soft Robotics:** Replacing the rigid manipulator model with a **continuum model** (e.g., using Cosserat rod theory or FEM) to investigate the benefits of compliance, safety, and adaptability in aerial grasping.
-   **Model-Based Design & Optimization:** Developing **optimization strategies** for the structural parameters of a soft manipulator to enhance its dexterity, reach, and payload capacity.
-   **Advanced Control Strategies:** Exploring adaptive and learning-based control techniques to handle the high nonlinearities and uncertainties inherent in soft robotic systems.

---
