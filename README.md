# Determining the Permittivity of Materials via an Equivalent Circuit Model

This project models a coaxial transmission line as a radiating antenna to retrieve the complex permittivity of materials such as methanol (CH₃OH) and sodium chloride (NaCl).

Using theoretical models based on Marsland and Evans’ methodology, the admittance of the system is determined through reflection coefficients, and compared with conventional equivalent circuit approaches. The code implements this using Python, and results are compared against theoretical values.

## Features

- Calculation of real and imaginary parts of complex permittivity
- Comparison between experimental and theoretical data
- Visualization of accuracy and residuals via matplotlib
- Uses `pandas`, `numpy`, and `matplotlib` for data handling and plotting

## Method Summary

The coaxial line is modeled with an equivalent circuit that includes:
- Radiation conductance G₀
- Fringing capacitance C₀ and C_f
- Two admittance models depending on frequency regime

Using calibration reflection coefficients from short, water, air, and methanol, the experimental reflection data is transformed to retrieve permittivity using:
ε_m = -[(Δ_m2 Δ_13 ε_3 + Δ_m3 Δ_21 ε_2) / (Δ_m1 Δ_32)]
