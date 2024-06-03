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

![image](https://github.com/aysannazarmohamady/Modified-SIR-Model/assets/30371881/217156ef-4b81-45b2-afea-52f5a9666a2d)

Here, 𝛽 represents the transmission rate per contact and 𝛾 is the recovery rate.


**Methodology**

**1. Model Definition:** Includes setting up the basic structure and equations based on epidemiological data.

**2. Parameter Estimation:** Uses real-world data to estimate parameters like 𝛽, 𝛾, and 𝑝(𝑡) through optimization techniques.

**3. Model Translation:** Converts the ODE model to a Continuous Time Markov Chain (CTMC) for stochastic analysis using PRISM model checker.

**4. Simulation and Analysis:** Conducts stochastic simulations and model checking to evaluate the impact of different intervention strategies and predict future disease spread.


**Data Requirements**

The model requires daily updated data on COVID-19 cases, including the number of new infections, recoveries, and active cases. The data format should be structured to enable efficient processing and integration into the simulation environment.


**Evaluation Metrics**

The performance of the model is evaluated using:

**- Accuracy of Fit:** How well the model predictions align with observed data.
**- Predictive Power:** Ability to forecast future trends under different scenarios.




