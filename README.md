# **Deep Collocation Method for Solving Differential Equations**
This repository contains an implementation of the **Deep Collocation Method (DCM)** for solving **Ordinary Differential Equations (ODEs)** and **Partial Differential Equations (PDEs)** using **PyTorch**.

## **📖 Overview**
Deep Collocation Methods (DCM) are neural network-based approaches for solving differential equations by enforcing the governing equation and boundary/initial conditions as constraints in the loss function. This implementation includes:
- **Solving an ODE** using deep collocation.
- **Solving the 1D Heat Equation (PDE)** using a neural network.

## **📜 Implemented Problems**
### ✅ **Ordinary Differential Equation (ODE)**
Solves the simple first-order ODE:

\[
$\frac{dy}{dx} = y, \quad y(0) = 1$.
\]

The exact solution is:

\[
$y(x) = e^x$.
\]

### ✅ **Heat Equation (PDE)**
Solves the one-dimensional **heat equation**:

\[
$\frac{\partial u}{\partial t} = \alpha \frac{\partial^2 u}{\partial x^2}, \quad x \in [0,1], \quad t \in [0,1]$.
\]

with boundary conditions \( $u(0,t) = u(1,t) = 0$ \) and initial condition \( $u(x,0) = \sin(\pi x)$ \).  
The exact solution is:

\[
$u(x,t) = e^{-\alpha \pi^2 t} \sin(\pi x)$.
\]

## **🚀 Installation & Running**
1️⃣ **Install dependencies:**
```bash
pip install torch numpy matplotlib
```


## **📊 Results**
- The **Deep Collocation Method (DCM)** approximates the solution using a neural network.
- The predicted solutions are compared with **exact solutions** for validation.
- **3D surface plots** are generated for the PDE solution over time.

## **📚 Reference**
This implementation is inspired by the following paper:

- **Deep Collocation Methods: A Framework for Solving Integro-Differential Equations with Neural Networks**  
  [arXiv:2502.17203](https://arxiv.org/abs/2502.17203)
