# Data Analysis Applied to Mineral Comminution

This project aims to demonstrate technical skills in data analysis applied to the comminution process, using an artificially generated dataset. It covers the complete stages of a data science workflow, from data cleaning and exploration to predictive modeling.

## Project Objectives

- Apply data cleaning and exploratory techniques within a mining and metallurgical context.  
- Visualize relationships between operational variables and process outcomes.  
- Develop a predictive model to estimate output P80 based on key process parameters.  
- Integrate tools such as `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn` professionally.

## Variables Considered for the Predictive Model

- **P80_Input_microns**  
- **Solids_Percentage**  
- **Mineral_Type**  
- **Hardness_BWI**  
- **Mill_RPM**  
- **Operating_Hours**  
- **P80_Output_microns** (target variable)

## Conclusions

- Technical proficiency in data analysis and modeling tools was demonstrated.  
- A well-founded data cleaning and treatment strategy was applied.  
- Although the data lacked real correlations (due to its artificial origin), relevant hypotheses about the comminution process were explored.  
- Relationships such as reduced specific energy consumption with increased throughput were observed.  
- Operating with 66%-70% solids was identified as beneficial for size reduction in mixed minerals.  
- A `RandomForestRegressor` model tuned with `RandomizedSearchCV` was implemented but performed poorly due to the lack of relationships in the data.  
- The exercise serves as a solid demonstration of data science skills applied to mining.

## Author

**Bastián Albornoz**  
Metallurgical Civil Engineer | Junior Data Analyst  