# nypd_project
Creating actionable insights for the NYPD with data modeling techniques.
- Data Imputation and Exploratory Data Analysis performed
- Algorithms explored to compare and contrast accuracy scores:
** Clustering
** K-Nearest Neighbors (KNNs)
** Random Forest
** Support Vector Machines (SVMs)


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
