# Driven Damped Harmonic Oscillator Interactive Simulator

An interactive Jupyter Notebook simulation of a driven damped harmonic oscillator built in Python.
User inputs all system parameters and explores oscillation, damping, and resonance through three auto-generated plots.

## Background & Theory

A harmonic oscillator is any physical system where a restoring force pulls it back to equilibrium proportional to its displacement lik a mass on a spring, a pendulum, an electric circuit, a vibrating molecule. The same mathematics describes all of them.

**Equation of motion:**

mẍ = -kx - bẋ + F₀cos(ω_d t)

| Symbol | Meaning |
|--------|---------|
| m | mass |
| k | spring constant |
| b | damping coefficient |
| F₀ | driving force amplitude |
| ω_d | driving frequency |
| x, ẋ, ẍ | displacement, velocity, acceleration |

**Damping** : friction and air resistance drain energy from the system. The coefficient b controls how fast.

**Driving Force** : an external periodic force pumping energy in, competing against damping.

**Resonance** : every oscillator has a natural frequency ω₀ = √(k/m). When the driving frequency matches this, energy builds up continuously and amplitude grows dramatically.

Real world resonance:
- Tacoma Narrows Bridge (1940) : collapsed when wind matched its natural frequency
- MRI machines : hydrogen atoms driven at their natural frequency
- Musical instruments : strings and air columns resonating at specific frequencies
- Microwave ovens : water molecules driven at their natural frequency

## How to Run

Open in Jupyter Notebook and run all cells sequentially with **Shift + Enter**. In VS Code or Google Colab use the equivalent run command. Enter parameters when prompted.


## What the Plots Show

**Plot 1 : Position vs Time**
Oscillation of the mass over time. Amplitude grows continuously at resonance, stays small off-resonance.

**Plot 2 : Phase Space (Position vs Velocity)**
Complete state of the system at every instant.
- Perfect ellipse = undamped SHM
- Inward spiral = damping killing motion
- Outward spiral = resonance building energy
- Tangled pattern = off-resonance, two frequencies fighting

**Plot 3 : Energy vs Time**
Kinetic, potential and total energy. Shows energy conservation, dissipation, or buildup depending on parameters.

## Suggested Experiments

| Experiment | Parameters | What to observe |
|------------|------------|-----------------|
| Pure SHM | b=0, F0=0, x0=1 | Perfect ellipse, flat total energy |
| Damping only | F0=0, b>0 | Inward spiral, decaying amplitude |
| Resonance | b=0.05, F0=2, t=300, type 'resonance' | Outward spiral, energy climbing to 800+ J |
| Off-resonance | b=0.05, F0=2, ω_d=1 | Tiny amplitude, flat energy — 30-100x weaker |
| Tacoma Bridge | m=1000, k=100, b=0.1, F0=50, t=300, resonance | Catastrophic energy buildup |
| Beats | b=0.01, F0=2, ω_d=ω₀+0.5 | Rhythmic energy oscillations |


## Libraries Used
- NumPy
- Matplotlib
- SciPy

## Author
Ayush Sharma — 1st Year (25MS) BS-MS Student, IISER Kolkata
