# DATA_SCIENTIST_Flight_Delays
This project is part of the Openclassrooms DataScientist Curriculum together with CentraleSupélec

### by Jérôme d'Harveng


## Dataset
> For this project, we used a DB of more than 5.5 Million flight records in the US during 2016. The **goal** here was knowing the parameters of a future flight predict the possible delay it could have.

## Data exploration:
> After having cleaned the data, and before moving to the regression models themselves, we first did some exploration to get a better understanding of our data.

> _Some interesting insights concerning the flights in this DB were:_
> - the big majority of the flights are leaving between 5am and 11pm.
> - 75% of the flights are covering a distance less than 1091miles.
> - 50% of the flights have less than 15 min delay at arrival and 75% less than 39 min.
> - Only 1,17% of the flights were cancelled in this DB, mainly due to weather conditions.
> - During the week there are more cancellations on Friday and Saturday.
> - January, July and December are the months with most cancellations.
> - Looking at the average delay on the arrival, we observe that July and December are the worst months.

## Variable encoding
> - Here one of the biggest difficulties at the beginning was the size of the dataset. We had to work on 5,5 million lines but with almost 733 features after One Hot Encoding 
> - Instead of OHE of the temporal variables, we used cyclical encoding.
> - For the _‘ORIGIN_AIRPORT_ID’_ and the _‘DEST_AIRPORT_ID’_, we did some feature engineering.

## Feature Engineering:
> - We replaced ‘ORIGIN_AIRPORT_ID’ and the ‘DEST_AIRPORT_ID’, by the amount of flights respective leaving and arriving there.
> - This all allowed us to decrease the amount of features from 733 features to 27.

## Regression Models
> After the different types of encoding and feature engineering, we used 2 different types of regression models with regularization:
1.Ridge
2.Lasso

> - We used the RMSE as evaluation metric of the results. We obtained a RMSE of 27.13.

