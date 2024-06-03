# Modified SIR Model

**Introduction**

This document the modified Susceptible-Infected-Recovered (SIR) model for COVID-19, incorporating governmental prevention measures into the traditional SIR framework. This modification allows the model to account for varying levels of social restrictions, which are represented by a time-dependent coefficient. This enhancement aims to provide more accurate simulations of disease spread under different policy implementations, useful for public health planning and response evaluation.


**Model Overview**

The traditional S.R. model partitions the population into three categories: Susceptible (S), Infected (I), and Recovered (R). The modified SIR model introduced in this research adds a dynamic coefficient to the infection rate to reflect the impact of governmental interventions like lockdowns or social distancing measures.


**Key Components:**

- Susceptible (S): Individuals at risk of contracting the disease.

- Infected (I): Currently infected individuals who can transmit the disease.

- Recovered (R): Individuals who have recovered from the disease and are no longer infectious.


The model is governed by the following system of differential equations, where 𝑝(𝑡) modifies the infection rate 𝛽 based on intervention policies:
\begin{align*}
\frac{dS}{dt} & = -\beta SI p(t) \\
\frac{dI}{dt} & = \beta SI p(t) - \gamma I \\
\frac{dR}{dt} & = \gamma I
\endart{align*}
