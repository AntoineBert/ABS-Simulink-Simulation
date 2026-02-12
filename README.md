# ABS Control System Simulation (Pacejka Tire Model)

This repository contains a **MATLAB/Simulink** implementation of an Anti-lock Braking System (ABS). The simulation focuses on the longitudinal dynamics of a vehicle during a hard braking maneuver, utilizing the **Pacejka "Magic Formula"** to accurately model the friction interface between the tire and the road.



## 📋 Project Overview

The goal of this system is to prevent wheel lock-up by modulating braking torque, maintaining the **Slip Ratio** ($\lambda$) within an optimal range where the friction coefficient ($\mu$) is at its peak.

### Key Features:
* **Pacejka Tire Model:** Realistic tire-road interaction using non-linear equations.
* **Hydraulic Dynamics:** Modeling of hydraulic resistance ($R_h$) and compliance ($C_h$).
* **Simulink Integration:** A modular block diagram approach for control logic testing.
* **Automated Plotting:** A Live Script (`Vars.mlx`) for parameter initialization and post-simulation analysis.

---

## ⚙️ Physical Parameters

The simulation is configured with the following default values (editable in `Vars.mlx`):

| Category | Variable | Value | Description |
| :--- | :--- | :--- | :--- |
| **Hydraulic** | $R_h$ | 0.1 | Hydraulic Resistance |
| | $C_h$ | 0.1 | Hydraulic Compliance |
| **Vehicle** | $m_v$ | 1200 kg | Vehicle Mass |
| | $v_0$ | 28 m/s | Initial Speed (~100 km/h) |
| | $R_w$ | 0.28 m | Wheel Radius |
| **Pacejka** | A, B, C, D | *Custom* | Shape factors for the $\mu$-slip curve |

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AntoineBert/GNSS-Positioning-And-Signal-Analysis.git```
2. **Initialize Variables:** Open MATLAB and run the `Vars.mlx` script. This loads all constants into the Workspace.
3. **Open Model:** Open the `ABS_Simulink_Model.slx` file.
4. **Simulate:** Click the **Run** button in the Simulink toolstrip.
5. **Analyze:** Return to the `Vars.mlx` window to view the generated subplots and performance analysis.



---

## 📊 Results and Analysis

The simulation generates four key performance indicators via `subplot`:
1. **Brake Torque:** Visualizes the pressure modulation by the ABS controller.
2. **Distance:** Compares the stopping distance of the vehicle vs. the theoretical wheel distance.
3. **Speed:** Shows the synchronization between vehicle speed and wheel speed.
4. **Slip Ratio:** Monitors the controller's ability to stay near the Pacejka curve peak.



---

## 🛠 Tech Stack
* **MATLAB** (R2020b or later recommended)
* **Simulink**
* **Control System Toolbox**

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact

**AntoineBert** - [GitHub Profile](https://github.com/AntoineBert)