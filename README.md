# Crime-Data-Analysis
Los Angeles Crime Data Analysis
# Data link -
https://data.lacity.org/api/views/2nrs-mtv8/rows.csv?accessType=DOWNLOAD

## Abstract:
A subject with conversations about crime analysis in the city all over the planet. After some investigates to observe open information, I've chosen to investigate the information in Los Angeles city. Confined in the south of California, it's the subsequent more inhabited city in the United States (just behind New York), it's the focal point of the film and media business.
Although crimes are committed at unexpected times, crime is a difficult topic for analytics and prediction, and therefore no actual crime prediction model could ever be as accurate as "Minority Report." 
Evaluating criminal background information to predict illegal acts could made in decreasing crime rates as well as preventing future losses. 
This crime report recommends the least and also most dangerous areas by evaluating the dataset.

## Objective:
To predict and classify the victim sex depending on the location,date,time,DR_NO,Area,crime code,vict age,The type of weapon used in the crime,vehicle, or location where the crime took place.

## Data discribtion
The dataset that will be presented in the next lines is available on the Los Angeles Open Data, for this purpose, I’ve used the dataset “Crime Data from 2020 to Present”, which covers crime incidents in Los Angeles between the years of 2020 and 2021. The original file has 28 columns and 360341 rows. The file has been pre-processed in Jupyter Notebook, to remove some rows values and columns that will be not used in the analysis.

## Below are all the variables in the dataset, followed by its description:
DR_NO - Division of Records Number: Official file number made up of a 2 digit year, area ID, and 5 digits.

DATE OCC - Date of crime occurrence(YYYY-MM-DD)

AREA - The LAPD has 21 Community Police Stations referred to as Geographic Areas within the department. These Geographic Areas are sequentially numbered from 1-21.

AREA NAME - The 21 Geographic Areas or Patrol Divisions are also given a name designation that references a landmark or the surrounding community that it is responsible for.

Rpt Dist No - Code that represents a sub-area within a Geographic Area.

Crm Cd - Indicates the crime committed.

Crm Cd Desc - Defines the Crime Code provided.

Vict Age - Indicates the age of the victim.

Vict Sex - F: Female M: Male X: Unknown

Vict Descent - Descent Code: A - Other Asian B - Black C - Chinese D - Cambodian F - Filipino G - Guamanian H - Hispanic/Latin/Mexican I - American Indian/Alaskan Native J - Japanese K - Korean L - Laotian O - Other P - Pacific Islander S - Samoan U - Hawaiian V - Vietnamese W - White X - Unknown Z - Asian Indian

Premis Cd - The type of structure, vehicle, or location where the crime took place.

Premis Desc - Defines the Premise Code provided.

Weapon Used Cd - The type of weapon used in the crime.

Weapon Desc - Defines the Weapon Used Code provided.

LOCATION - Street address of crime incident rounded to the nearest hundred block to maintain anonymity.

LAT - Latitude Coordinate. 

LON - Longitude Coordinate.

## Data Cleanup

Though this dataset has 28 columns.I omitted 'Crm Cd 4','Crm Cd 3','Crm Cd 2','Cross Street' columns because they dont have significant information for analysis.
all the Columns which are dropped  has many nulls.Even if we do imputing, its values will be duplicated. I removed the values for the "Vict Age" column where vict age contains <1 these values are not usefull for my analysis. Final dataset has 52880 rows and 24 columns I took limited amount of data for my modeling and classification.

## Exploratory data analysis:

With respect to crime carried out in the city of Los Angeles, five sorts have a more prominent unmistakable quality because of the quantity of events, among the violations perpetrated somewhere in the range of 2020 and 2021 the most successive are recorded:

Battery — Simple Assault, about 5800

Burglary from Vehicle, about 3600

Assault With Deadly Weapon, about 3700

Intimidate Partner, about 3400

The Los Angeles Police Department (LAPD) has a division for the police headquarters by networks, where gives general data and help, there are 21 topographical regions citywide According to the data frame, the communities where most crimes committed are:

Southwest Area, about 8700

Central Area, about 8400

Rampart, about 6300

harbor, about 6000

Time and date in which the crime percentage is high:

01/01/2020 12:00AM Above 250 crimes

02/14/2020 12:00AM 180 crimes

02/01/2020 12:00AM 190 crimes


## Feature Engineering:

1.My objective is to predict victims sex. the column 'Vict Sex' has three values 'M' , 'F' and 'X' where X means unknown gender so we don't need the X values for the modeling and classification so i dropped those values and thus making the class distribution balanced and making it a binary classification.
2.My features count of categorical and numerical are almost equal.


## Modeling and Classification

Since, there is a balance in the class data, after cleaning This dataset has almost 44494 rows.So, we alteast need 80 % of the data for training.
Training examples: 35595
Test examples: 8899

# Results
Classification using Logistic Regression
Hyperparameters Used: Used 0.001, 0.1,1,10 as penalty strengths for grid search.
Accuracy of 64% can be considered a good discrimination.
For this classifier, ROC_AUC score is 69% which has the best value compared to other classification.

Classification using Decision Tree Classifier
Hyperparameters Used: Used 3,5,6,8,10 as max_depths for grid search.
This model has 64% accuracy which is same compared to Logistic Regression.
Even the ROC_AUC score has been increased to 67%, but that's not enough for a good classification.

Classification using Kmeans
Hyperparameters Used:  0.001, 0.1,1,10 
It seems like Kmeans has 59% accuracy cannot be considered a good classification.
Also, the ROC_AUC score for Kmeans has also increased to 62%.

Classification using K-Nearest Neighbors Classifier:
Hyperparameters Used: Used 4,8,10 as number of neighbors for grid search
It seems like K-Nearest Neighbors has 60% accuracy cannot be considered a good classification.
Also, the ROC_AUC score for Kmeans has also increased to 64%, but that's not enough for a good classification..

Classification using Random Forest:
Hyperparameters Used:  5, 8, 10 
It seems like Random Forest has 59% accuracy cannot be considered a good classification.
Also, the ROC_AUC score for Random Forest has also increased to 61%. Random forest have the least accuracy compare to other models.

## Conclusion
####After analyzing the three models, I think Logistic Regression Classifier can classify better compared to others.We can improve the accuracy by dealing the dataset imbalance through better modeling techniques.




## References:
https://medium.com/analytics-vidhya/los-angeles-crime-data-analysis-using-pandas-a68780d80a83
https://github.com/appliedecon/data602-lectures/blob/main/regression/linear-regression-and-regularization.ipynb
https://github.com/appliedecon/data602-lectures/blob/main/unsupervised/clustering.ipynb
https://github.com/appliedecon/data602-lectures/blob/main/dimension-reduction/dimension-reduction.ipynb
https://github.com/appliedecon/data602-lectures/blob/main/trees/trees.ipynb

