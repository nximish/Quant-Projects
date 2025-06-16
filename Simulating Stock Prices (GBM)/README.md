# 📈 Geometric Brownian Motion (GBM) Stock Price Simulation

This project demonstrates how to simulate stock prices using **Geometric Brownian Motion**, a widely used stochastic model in quantitative finance. The simulation incorporates statistical modeling, Monte Carlo techniques, and data visualization to build intuition around how asset prices evolve under uncertainty.

---

## 🧠 Project Overview

The Geometric Brownian Motion (GBM) model is defined by the stochastic differential equation:

<div align="center"><code>
dS = μSdt + σSdz
</code></div>

Where:
- **S** is the stock price
- **μ** is the drift (expected return)
- **σ** is the volatility (standard deviation of returns)
- **dz** is a Wiener process (Brownian motion)

The solution to this SDE gives the analytical expression used for simulation:

<div align="center"><code>
S(t) = S₀ · exp[(μ - 0.5σ²)t + σW(t)]
</code></div>

---

## 💻 What's Implemented

The Jupyter notebook walks through a structured and intuitive implementation of the simulation:

### ✅ Step-by-Step Workflow

1. **Initialize Parameters**
   - Stock price, drift, volatility, time horizon, time steps, and number of simulations.

2. **Create a Time Grid**
   - Discretize the time interval using `np.arange` or `np.linspace`.

3. **Simulate Brownian Motion**
   - Generate random normal values to simulate Wiener processes for multiple paths.

4. **Compute GBM Paths**
   - Use the analytical solution to compute stock prices across the time grid.

5. **Plot a Single GBM Path**
   - Visualize one realization of the stochastic process.

6. **Monte Carlo Simulations**
   - Generate and plot hundreds of GBM paths to assess randomness and spread.

7. **Histogram of Final Prices**
   - Analyze the distribution of terminal prices at the end of the time horizon.

8. **Mean Path and Confidence Band**
   - Plot the average trajectory with a shaded 10th–90th percentile confidence interval.

---

## 📊 Visualizations

The notebook contains several visual insights:

- 📈 Single-path GBM plot
- 🌐 Multiple-path Monte Carlo simulation
- 🧮 Histogram of final stock prices
- 📉 Mean and percentile band plot

> Some animations or GIFs (e.g., `gbm_simulation.gif`) are also referenced in the full LaTeX report and visual summary.

---

## 📝 Report

A detailed **LaTeX report** is provided, including:
- Mathematical background
- GBM derivation
- Intuition behind each parameter
- Visual explanations with figures
- Clear separation of theory and implementation

The final output is suitable for academic or professional presentation.

---

## 📦 Dependencies

To run this project, install the following:

```bash
pip install numpy matplotlib
