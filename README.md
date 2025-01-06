# Double Pendulum - Chaos Theory

This project explores the dynamics of the double pendulum, a classical system known for its chaotic behavior. The notebook uses physics principles and machine learning to analyze the system and predict the lower mass's future positions using incomplete information.

---

## Key Concepts

### Kinematics of the Double Pendulum

**Positions**:  
- x1 = L1 * sin(θ1), y1 = -L1 * cos(θ1)  
- x2 = x1 + L2 * sin(θ2), y2 = y1 - L2 * cos(θ2)  

**Velocities**:  
- dx1/dt = θ1_dot * L1 * cos(θ1), dy1/dt = θ1_dot * L1 * sin(θ1)  
- dx2/dt = dx1/dt + θ2_dot * L2 * cos(θ2), dy2/dt = dy1/dt + θ2_dot * L2 * sin(θ2)  

**Accelerations**:  
- d²x1/dt² = -θ1_dot² * L1 * sin(θ1) + θ1_double_dot * L1 * cos(θ1)  
- d²y1/dt² = θ1_dot² * L1 * cos(θ1) + θ1_double_dot * L1 * sin(θ1)  
- d²x2/dt² = d²x1/dt² - θ2_dot² * L2 * sin(θ2) + θ2_double_dot * L2 * cos(θ2)  
- d²y2/dt² = d²y1/dt² + θ2_dot² * L2 * cos(θ2) + θ2_double_dot * L2 * sin(θ2)  

---

### Energies

**Kinetic Energies**:  
- T1 = 0.5 * m1 * (dx1/dt² + dy1/dt²)  
- T2 = 0.5 * m2 * [(dx1/dt² + dy1/dt²) + (dx2/dt² + dy2/dt²) + 2 * L1 * L2 * cos(θ1 - θ2) * θ1_dot * θ2_dot]  

**Potential Energies**:  
- V1 = -m1 * g * L1 * cos(θ1)  
- V2 = -m2 * g * (L1 * cos(θ1) + L2 * cos(θ2))  

---

## Machine Learning Component

The project uses the lower mass's position data to train a machine learning model. The goal is to predict future positions of the lower mass based on incomplete information, demonstrating the challenge of forecasting chaotic systems.

