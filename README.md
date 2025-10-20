# Predictive Carbon Cycle Modeling

## Overview
This project, part of the **MACS205** course at Télécom Paris, models the **global carbon cycle and temperature evolution** using numerical integration methods.  
The goal is to verify the consistency and stability of different solvers applied to a climate dynamics problem inspired by the IPCC model.

---

## Methods
We reformulate the system as a **Cauchy problem**:

\[
\frac{dy}{dt} = f(t, y), \quad y(t_0) = y_0
\]

Implemented methods:
- Euler (explicit)
- Heun (RK2)
- Runge–Kutta 4 (RK4)
- Adams–Bashforth (2-step)

Each method is tested on the same carbon–temperature model to compare **accuracy, stability, and global error**.

---

## Results
- **RK4**: highest precision and stable over long horizons  
- **Heun**: good trade-off between cost and accuracy  
- **Euler**: large cumulative error  
- **Adams–Bashforth**: efficient for constant step sizes  

The function \( f(t, y) \) is **non-Lipschitz**, which limits stability for large time steps.

