# Designing a resource plan for the NYPD

<p align="center">
  <img/>
<img src="https://images.law.com/contrib/content/uploads/sites/389/2017/10/nypd-car-Article-201710062015.jpg"/></div>
</p>


## Overview
Looking at historical NYPD data, *only* 7% (on average) of suspected criminals were arrested. This means 90%+ of the police force's time is wasted. Using data science, I help the NYPD identify factors that would likely lead to arrest and ultimately, help them use their time more efficiently.

## Summary of Results
- **Powerpoint presentation:** [LINK](https://github.com/jacksonfd8/nypd_project/blob/master/JAu_NYPD.pdf)

## Project Design
- Define the problem: Can we utilize historical data to discover *better* strategies for the NYPD?
- Dig into the data: I perform exploratory data analysis for initial insights
- Develop a solution: I create multiple models to predict arrests. I build clusters for criminals who make up most of the arrests.
- Deploy solution: I provide the solution to the NYPD, which will increase their 7% efficiency to 82%.

## Data Description

| Column Name | Description                                                | Data Type |
|-------------|------------------------------------------------------------|-----------|
| pct         | PRECINCT OF STOP (FROM 1 TO 123)                           | Nominal   |
| ser_num     | UF250 SERIAL NUMBER                                        | Nominal   |
| datestop    | DATE OF STOP (MM-DD-YYYY)                                  | Nominal   |
| timestop    | TIME OF STOP (HH:MM)                                       | Scale     |
| recstat     | RECORD STATUS                                              | Nominal   |
| inout       | WAS STOP INSIDE OR OUTSIDE ?                               | Nominal   |
| trhsloc     | WAS LOCATION HOUSING OR TRANSIT AUTHORITY ?                | Nominal   |
| crimsusp    | CRIME SUSPECTED                                            | Scale     |
| typeofid    | STOPPED PERSON'S IDENTIFICATION TYPE                       | Scale     |
| explnstp    | DID OFFICER EXPLAIN REASON FOR STOP ?                      | Nominal   |
| othpers     | WERE OTHER PERSONS STOPPED, QUESTIONED OR FRISKED ?        | Nominal   |
| arstmade    | WAS AN ARREST MADE ?                                       | Nominal   |
| offunif     | WAS OFFICER IN UNIFORM ?                                   | Nominal   |
| frisked     | WAS SUSPECT FRISKED ?                                      | Nominal   |
| searched    | WAS SUSPECT SEARCHED ?                                     | Nominal   |
| ac_proxm    | ADDITIONAL CIRCUMSTANCES - PROXIMITY TO SCENE OF OFFENSE   | Nominal   |
| rf_attir    | REASON FOR FRISK - INAPPROPRIATE ATTIRE FOR SEASON         | Nominal   |
| cs_cloth    | REASON FOR STOP - WEARING CLOTHES COMMONLY USED IN A CRIME | Nominal   |
| ac_incid    | ADDITIONAL CIRCUMSTANCES - AREA HAS HIGH CRIME INCIDENCE   | Nominal   |
| repcmd      | REPORTING OFFICER'S COMMAND (1 TO 999)                     | Nominal   |
| revcmd      | REVIEWING OFFICER'S COMMAND (1 TO 999)                     | Nominal   |
| sex         | SUSPECT'S SEX                                              | Nominal   |
| race        | SUSPECT'S RACE                                             | Nominal   |
| age         | SUSPECT'S AGE                                              | Nominal   |
| ht_feet     | SUSPECT'S HEIGHT (FEET)                                    | Scale     |
| ht_inch     | SUSPECT'S HEIGHT (INCHES)                                  | Nominal   |
| height_in   | SUSPECT'S HEIGHT (INCHES)                                  | Nominal   |
| weight      | SUSPECT'S WEIGHT                                           | Nominal   |
| haircolr    | SUSPECT'S HAIRCOLOR                                        | Scale     |
| eyecolor    | SUSPECT'S EYE COLOR                                        | Nominal   |
| build       | SUSPECT'S BUILD                                            | Nominal   |
| city        | LOCATION OF STOP CITY                                      | Nominal   |
| addrpct     | LOCATION OF STOP ADDRESS PRECINCT                          | Nominal   |

### Exploratory Data Analysis + Baseline 
Data cleaning, and fun visualizations to summarize the data
- file_name: [EDA](https://github.com/jacksonfd8/nypd_project/blob/master/Exploratory%20Data%20Analysis.ipynb)

**Technical Scope:**
- Exploratory data analysis is performed with the use of **Python** libraries: *Pandas, Seaborn, Matplotlib*

<p align="center">
  <img/>
<img src="https://i.imgur.com/PPLUfMP.png"/></div>
</p>

<p align="center">
  
  <img/>
<img src="https://i.imgur.com/KmgXQiE.png"/></div>
</p>

<p align="center">
  <img/>
<img src="https://i.imgur.com/qUqh2hR.png"/></div>
</p>

### Modeling (Classification Task)
- file_name: [Classification](https://github.com/jacksonfd8/nypd_project/blob/master/Classification.ipynb)

#### Technical Scope
- Explored Logistic Regression, Random Forests, k-Nearest Neighbors algorithms 
- Utilized Gradient Boosting to discover feature importance

<p align="center">
  <img/>
<img src="https://i.imgur.com/YpvPtAV.png"/></div>
</p>


### Further modeling (Clustering, PCA)
Cluster analysis segments data into groups, so the NYPD understands what criminal “profiles” can look like.
I use dimension reduction technique, PCA, to summarize features in the data.
- file_name: [Clustering_PCA](https://github.com/jacksonfd8/nypd_project/blob/master/Clustering_PCA.ipynb)

#### Technical Scope
- Clustering for segmentation
- Principal Component Analysis (Dimension Reduction) for further segmentation analysis

<p align="center">
  <img/>
<img src="https://i.imgur.com/6zEu7Nt.png"/></div>
</p>

<p align="center">
  <img/>
<img src="https://i.imgur.com/q54bQgP.png"/></div>
</p>

<p align="center">
  <img/>
<img src="https://i.imgur.com/tJBfHG5.png"/></div>
</p>

## Summary of Results
- **Powerpoint presentation:** [LINK](https://github.com/jacksonfd8/nypd_project/blob/master/JAu_NYPD.pdf)

## Future Work
- I intend on mining other cities' police department data to discover if there is a trend amongst crimes
- It would be worthwhile to evaluate my recommendations by looking at future arrests post-deploy of strategies
