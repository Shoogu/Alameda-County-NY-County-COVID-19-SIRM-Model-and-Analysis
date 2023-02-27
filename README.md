# Alameda-County-NY-County-COVID-19-SIRM-Model-and-Analysis

# SIRM COVID-19 Model - README

This repository is home to two MATLAB code files that document a Susceptible-Infected-Recovered (SIR), with an additional mortality proportion (SIRM), compartment model for predicting the spread of COVID-19 in Alameda County and New York. 

## File 1: Alameda & NY Fitting, Regression, and Presentation.mlx
This file imports the COVID-19 data for testing, deaths, hospitalizations, and vaccinations from October 2020 to January 2021 in Alameda and New York counties using the data stored in the file `ENGR_25_COVID_DATA_2.xlsx`. It then converts row data back into column vectors and then row vectors by week to make the data easier to interpret. Null values are eliminated in the hospitalization data and each category, positive tests, deaths, hospitalizations, and vaccinations are plotted separately for both counties. 

Linear and logarithmic fits were then calculated using polynomial, exponential, and power fits on the COVID-19 data for the weekly death counts. The results were then plotted with the original data for both. 

## File 2: SIRmodel.mlx
This file models the Susceptible-Infected-Recovered (SIR) model for Alameda County and New York County to predict the spread of COVID-19. 

The SIR model consists of three compartments:
1. Susceptible (S)
2. Infected (I)
3. Recovered (R)

The variables `beta` and `mu` represent the contact and recovery rates, respectively.

Euler's method is used to numerically solve the system of differential equations. The estimates for the S, I, and R outputs at each time step are computed by multiplying the step size by the rate of change, then adding the result to the previous value.

The results are then plotted for each county using a delta t of 10 and 1 to observe the differences. 

For each county, ode45 was used to plot the SIR Model as well. The output of the infected population was taken to find the maximum over the region of interest. 

## Dependencies
- MATLAB
- The data file `ENGR_25_COVID_DATA_2.xlsx` required for File 1

## How to Run
- Download the repository and all required files
- Open 'ENGR_25_COVID_DATA_2.xlsx', 'SIRmodel.mlx', 'SIRmodel2.mlx', 'SIRM.mlx' in MATLAB
- Run the files remaining: 'Alameda & NY Fitting, Regression, and Presentation.mlx' and 'SIRM and Beta vs Peak Infection Models.mlx'
- The plots will appear once each file has been executed.

## Conclusion
In conclusion, the MATLAB code files in this repository provide a detailed insight into the spread of COVID-19 in Alameda County and New York County. The SIRM model predicts the spread of COVID-19 taking into consideration the susceptible, infected, recovered, and deceased populations. The model uses real-world data for both counties which are imported, segmented and visualized. The model's predictions depict the change in the rates of infection, recovery, and death, as well as vaccination over the given time period. The plots enable an intuitive understanding of the changes in each population group in each county. The model would be useful in the decision-making process of government officials and healthcare workers, to quickly evaluate the likely impacts of different mitigation strategies on COVID-19 spread. Overall, this repository serves as a powerful tool to understand and analyze the spread of COVID-19 in a county-level compartment model approach.

## Sources:
% https://www.healthdata.org/covid/covid-19-vaccine-efficacy-summary 
% https://academic.oup.com/cid/article/52/7/911/299077
% https://plus.maths.org/content/maths-minute-r0-and-herd-immunity
% https://covid19.who.int/
% https://www.nytimes.com/interactive/2021/us/covid-cases.html
