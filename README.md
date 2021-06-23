# Predicting Voter Turnout in Texas

Chloe Burns, Jack Olson, Lucy Tai

## Overview

### Part 1: Problem Statement & Data Collection
- Reasons to Investigate Voter Turnout in Texas
- Texas Demographics and Voting History

### Part 2: Modeling to Predict Turnout and Election Results
- Predicting Voter Turnout using LASSO Regression
- Predicting Election Results by Expected Party Turnout

___

### Problem Statement

The DNC wants to investigate factors influencing voter turnout and election results. Texas is of particular interest because of its size, demographic changes, and fluctuating voting laws.

---

### Changing Demographics and Voter Laws in Texas

Demographics
- State Demographers predict Hispanics will become the state’s largest population group by mid-2021
- Texas is trending younger
- Despite demographic changes pointing toward a blue shift, 2020 election results discouraged belief for a blue shift in Texas

Voting Laws
- 05.31.21: SB 7 passes, including new ID requirements for mail-in ballots and early voting restrictions
  - Proponents of SB 7 argue it improves voting standardization and security. Opponents argue it is more restrictive on voting methods historically used by minority groups.
- 10.11.20: Texas Counties Blocked from offering multiple mail-in ballot drop-off locations
- 9.23.20: Texas Republicans sue to stop Gov. Greg Abbott's extension of early voting period during the pandemic 

---

### LASSO Regression to Predict Voter Turnout 

We used a LASSO Regression Model trained on 2012 and applied to 2016 & 2020.

- We chose LASSO because:
   - Easy interpretation
   - LASSO outperformed other regressors (KNeighbors, Random Forest) on RMSE and R2 metrics
   
The most signifigant coefficeints of the LASSO model were Hispanic population measures.

LASSO Results:
- 2020 R2 of .9855
- For 2020 we were able to reduce error from baseline models a minimum of 86%
- Our model performed much better at predicting small county voter turnout. This model could be useful in predicting turnout on a smaller scale
- For both 2016 and 2020 Democrat turnout was underprecicted by more the Republican turnout
- For both 2016 and 2020 Republican turnout was predicted to be highest, mirroring actual statewide election results

---

### Logistic Regression to Predict County Victories

Unlike LASSO, Logistic Regression allows for a binary prediction such as which party had the highest turnout in a county. For this section, we made the assumption that whichever party has higher turnout in a county will win that county. Predicting at the county level is useful for stakeholders.

In both 2016 & 2020 our model was better at predicting Republican counties. For example, 23% of Democratic counties were predicted to be Republican in 2020. For comparison, only 6.5% of Republican counties were incorrectly classified.

---

# Conclusion

- Our Goal
  - Identify features influencing voter turnout
  - Use them to predict county results
- We Chose to Study Texas Because
  - Large Size
  - Demographic Changes
  - Voting Law Controversy
- Lasso Regression to Predict Turnout
  - Accurate, especially for small counties
  - Worse at predicting Democratic Turnout
- Logistic Regression to Predict County Victories
  - Model was conservative and overpredicted Rep. majority in counties
  - Useful for identifying swing counties




  

 

  









