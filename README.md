# Modified SIR Model


📍 **Introduction**

This document the modified Susceptible-Infected-Recovered (SIR) model for COVID-19, incorporating governmental prevention measures into the traditional SIR framework. This modification allows the model to account for varying levels of social restrictions, which are represented by a time-dependent coefficient. This enhancement aims to provide more accurate simulations of disease spread under different policy implementations, useful for public health planning and response evaluation.


📃 **Model Overview**

The traditional S.R. model partitions the population into three categories: Susceptible (S), Infected (I), and Recovered (R). The modified SIR model introduced in this research adds a dynamic coefficient to the infection rate to reflect the impact of governmental interventions like lockdowns or social distancing measures.


🔑 **Key Components:**

- Susceptible (S): Individuals at risk of contracting the disease.

- Infected (I): Currently infected individuals who can transmit the disease.

- Recovered (R): Individuals who have recovered from the disease and are no longer infectious.


The model is governed by the following system of differential equations, where 𝑝(𝑡) modifies the infection rate 𝛽 based on intervention policies:

![image](https://github.com/aysannazarmohamady/Modified-SIR-Model/assets/30371881/217156ef-4b81-45b2-afea-52f5a9666a2d)

(Here, 𝛽 represents the transmission rate per contact and 𝛾 is the recovery rate.)

**Each equation represents the rate of change over time of different groups in the population:**

**1. Susceptible (𝑆):**

![image](https://github.com/aysannazarmohamady/Modified-SIR-Model/assets/30371881/ec9d9f18-93f5-41ae-acc4-13c3c0615e3d)

This equation describes the rate at which susceptible individuals become infected. Here, 𝛽 represents the contact rate that leads to new infections, 𝑆 is the proportion of susceptible individuals, 𝐼 is the proportion of infected individuals, and 𝑝(𝑡) is a time-dependent modification factor that represents the effectiveness of intervention measures (like social distancing or lockdowns). The product 𝛽𝑆𝐼𝑝(𝑡) is the rate at which susceptible individuals are becoming infected, and it's subtracted from the susceptible group because these individuals are moving into the infected category.

**2. Infected (𝐼):**

![image](https://github.com/aysannazarmohamady/Modified-SIR-Model/assets/30371881/3c76c6e4-ef7b-4bb6-8f6b-156f272caafb)

This equation shows the change in the infected population. It includes the same infection term as in the first equation (𝛽𝑆𝐼𝑝(𝑡)), which adds to the infected category. The second term, −𝛾𝐼, represents the rate at which infected individuals recover or die, thus leaving the infected category. The parameter 𝛾 is the recovery rate, where 1/𝛾 is the average duration of infection.


**3. Recovered (𝑅):**

![image](https://github.com/aysannazarmohamady/Modified-SIR-Model/assets/30371881/dcca2457-64e9-4f39-97cb-774819a9da63)

This equation tracks the rate of change of the recovered population. It includes only the term 𝛾𝐼, indicating the rate at which individuals are moving from the infected status to the recovered status (assuming recovery confers immunity or the individual is no longer infectious).

In summary, these equations model the dynamics of an epidemic, accounting for how interventions impact the infection rate through the modification factor 𝑝(𝑡). This allows the model to adapt to real-world scenarios where public health measures are enacted to control the spread of the disease.


⛯ **Methodology**

**1. Model Definition:** Includes setting up the basic structure and equations based on epidemiological data.

**2. Parameter Estimation:** Uses real-world data to estimate parameters like 𝛽, 𝛾, and 𝑝(𝑡) through optimization techniques.

**3. Model Translation:** Converts the ODE model to a Continuous Time Markov Chain (CTMC) for stochastic analysis using PRISM model checker.

**4. Simulation and Analysis:** Conducts stochastic simulations and model checking to evaluate the impact of different intervention strategies and predict future disease spread.


📊 **Data Requirements**

The model requires daily updated data on COVID-19 cases, including the number of new infections, recoveries, and active cases. The data format should be structured to enable efficient processing and integration into the simulation environment.


📏 **Evaluation Metrics**

The performance of the model is evaluated using:

- ****Accuracy of Fit:**** How well the model predictions align with observed data.
- ****Predictive Power:**** Ability to forecast future trends under different scenarios.


⌨️ **Implementation Details**

The implementation involves setting up a Python environment with libraries such as NumPy and SciPy for numerical operations. The CTMC model is implemented in the PRISM programming language. Detailed steps to set up and run the model are as follows:

- Install Python and required packages.
- Clone the repository from GitHub: SIR-covid.
- Execute the Jupyter Notebook included in the repository to perform parameter estimation and initial simulations.
- Set up PRISM and run the provided model scripts to perform detailed stochastic analysis.

📚 **Limitations and Future Work**
The model, while robust, has limitations due to assumptions such as a constant total population and homogeneous mixing. Future work could include refining the intervention coefficient 𝑝(𝑡) to better represent phased introductions of measures or integrating additional data sources such as mobility or demographic information.



🔗 * Original Research Article: Analysis of COVID-19 Data with PRISM

🔗 * PRISM Model Checker: [PRISM Website](https://www.prismmodelchecker.org/)
