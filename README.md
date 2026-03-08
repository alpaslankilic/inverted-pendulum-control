# inverted-pendulum-control
MATLAB implementation of an inverted pendulum on a cart, featuring LQR, pole placement, and observability. Based on Steve Brunton's Control Bootcamp.

# Inverted Pendulum on a Cart - Control Systems

[Insert an image or GIF of the inverted pendulum simulation here]

## About the Project
This repository contains MATLAB simulations and control algorithms for the classic "Inverted Pendulum on a Cart" (Cart-Pole) system. 

The mathematical modeling and control approaches in this code are based on Prof. Steve Brunton's **Control Bootcamp** series. The primary objective of the system is to balance the pendulum in its unstable upright position.

## File Structure

This repository consists of MATLAB scripts covering various stages, from system dynamics to advanced control and observer designs:

* **`cartpend.m`**: The core function containing the non-linear differential equations (equations of motion) of the system.
* **`sim_cartpend.m`**: Simulation script used to observe the open-loop dynamic behavior and free fall of the pendulum.
* **`linearize_cartpend.m`**: Linearizes the non-linear system around the target equilibrium point (upright position) using Jacobian matrices to obtain the State-Space $A, B, C, D$ matrices.
* **`poleplace_cartpend.m`**: Implements closed-loop control of the system using the Pole Placement method.
* **`lqr_cartpend.m`**: Optimal control simulation designed using a Linear Quadratic Regulator (LQR).
* **`obsv_cartpend.m`**: Tests the observability of the system and includes an Observer design for full-state feedback.
* **`drawcartpend.m` & `drawcartpend_bw.m`**: Animation functions used to visualize the simulation results, rendering the motion of the cart and pendulum.

## Control Methods Used
This project primarily utilizes the state-space representation:

$$\dot{x} = Ax + Bu$$
$$y = Cx + Du$$

To stabilize the system, **Pole Placement** and a more optimized approach, **LQR**, are applied. The concept of **Observability** is also explored for real-world scenarios where not every state variable can be directly measured by sensors.

## How to Run
1. Clone the repository to your local machine.
2. Open MATLAB and navigate to this folder, setting it as your `Current Folder`.
3. To test the control algorithms, type `lqr_cartpend` or `poleplace_cartpend` in the Command Window and hit Enter. The simulation and animation will start automatically.

## Acknowledgments & References
The concepts and code architecture in this project are based on the excellent **Control Bootcamp** educational series by Prof. Steven L. Brunton (University of Washington).
