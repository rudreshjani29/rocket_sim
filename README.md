# rocket_sim
Rocket Simulator in Python
# 🚀 Rocket Flight Simulator in Python

This project is a **physics-based simulator** of a vertically launched rocket, built using Python. It models the flight trajectory using the **Tsiolkovsky rocket equation** and **numerical integration** to predict altitude, velocity, and fuel consumption over time. The simulation supports dynamic input parameters for thrust, payload, fuel mass, drag, and more.


---

## ✨ Features

- Real-time simulation of:
  - 🚀 Altitude
  - 💨 Velocity
  - ⚖️ Mass (fuel consumption)
- Numerical solution using Euler's method
- Customizable rocket configuration
- Visualized with **Matplotlib**
- Models gravity and aerodynamic drag
- Terminal velocity and descent tracking

---

## 📥 Input Parameters

The simulator accepts the following parameters via command-line input:

| Parameter              | Description                          | Default     |
|------------------------|--------------------------------------|-------------|
| Payload Mass (kg)      | Non-fuel mass excluding rocket       | `100`       |
| Dry Rocket Mass (kg)   | Rocket structure without fuel        | `500`       |
| Fuel Mass (kg)         | Propellant fuel mass                 | `1000`      |
| Thrust (N)             | Engine thrust                        | `30000`     |
| Exhaust Velocity (m/s) | Effective exhaust velocity           | `3000`      |
| Burn Rate (kg/s)       | Fuel consumption rate                | `10`        |
| Drag Coefficient       | Aerodynamic drag coefficient         | `0.75`      |
| Cross-sectional Area (m²) | Frontal area for drag calculation | `1.0`       |

> ⚠️ Note: Ensure thrust > weight for liftoff (i.e., `thrust > total_mass * 9.81`).

---

## 🧪 How It Works

The simulator uses the basic rocket dynamics equations:

- **Tsiolkovsky Equation** for ideal velocity gain.
- Newton’s second law and drag force:
  
  \[
  F = T - mg - \frac{1}{2} \cdot C_d \cdot \rho \cdot A \cdot v^2
  \]

- Numerical integration via Euler’s method to compute motion per timestep.

---

## 📊 Sample Output

- **Burn Phase:** Rocket ascends with increasing speed
- **Coasting Phase:** After burnout, the rocket continues upward
- **Descent Phase:** Rocket falls back under gravity and drag

---

## 🖼 Visualizations

The simulation generates a time-series plot showing:

1. Altitude (m)
2. Velocity (m/s)
3. Mass (kg)

You can customize or export this plot from within the code.

---

## 🚀 Getting Started

### ✅ Requirements

- Python 3.8+
- `matplotlib`
- `numpy`

### 📦 Installation

```bash
git clone https://github.com/yourusername/rocket-flight-simulator
cd rocket-flight-simulator
pip install -r requirements.txt
