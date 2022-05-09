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
To predict and classify the Crime Code depending on the vict age, loaction,time.

## Data discribtion
The dataset that will be presented in the next lines is available on the Los Angeles Open Data, for this purpose, I’ve used the dataset “Crime Data from 2020 to Present”, which covers crime incidents in Los Angeles between the years of 2020 and 2021. The original file has 28 columns and 220405 rows. The file has been pre-processed in Jupyter Notebook, to remove some rows values and columns that will be not used in the analysis.

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

## Exploratory data analysis:

With respect to crime carried out in the city of Los Angeles, five sorts have a more prominent unmistakable quality because of the quantity of events, among the violations perpetrated somewhere in the range of 2020 and 2021 the most successive are recorded:

Battery — Simple Assault, about 10.9%

Burglary from Vehicle, about 8.39%

Assault With Deadly Weapon, about 7.54%

Intimidate Partner, about 7.28%

Vandalism, about 6.44%

The Los Angeles Police Department (LAPD) has a division for the police headquarters by networks, where gives general data and help, there are 21 topographical regions citywide According to the data frame, the communities where most crimes committed are:

77th Street Area, about 6.76%

Southwest Area, about 6.28%

Central Area, about 5.97%

Pacific Area, about 5.54%

Southeast Area, about 5.46%

Time and date in which the crime percentage is high:

01/01/2020 12:00AM Above 800 crimes

03/01/2020 12:00AM 590 crimes

02/01/2020 12:00AM 580 crimes

Age classification of individuals took part in crimes:

30 Years, about 3.1%

29 Years, about 3.0%

28 Years, about 2.9%

## Data Cleanup
Though this dataset has 28 columns.I omitted 'Crm Cd 4','Crm Cd 3','Crm Cd 2','Cross Street' columns because they dont have significant information for analysis.
all the Columns which are dropped  has many nulls.Even if we do imputing, its values will be duplicated. I removed the values for the "Vict Age" column where vict age contains <1. Final dataset has 10000 rows and 24 columns. Actual dataset has ----

Feature Engineering
1.My objective is to predict sentence type.But the distribution of classes seams to be imbalanced.There are less samples for Long Split.Short Split Sentence and Long Split means offenders serving some time in prison and some time outside depending on their behaviour.Probation also serves the same purpsose.So,I merged the Short Split and Long Split into Probation and thus making the class distribution balanced and making it a binary classification
2. Most of my features are categorical and as a part of preprocessing, I have to label encode them for training.
3.Most of the features are negatively correlated to target variable "SENTENCE_TYPE".I think it is a good correlation because higher correlation might have masked the prediction.

Modeling and Classification
Since, there is a slight imbalance in the class data, I have done oversampling to negate the imbalance to some extent using SMOTE function
This dataset has almost 24324 rows.So, we alteast need 80 % of the data for training.

Conclusion
####After analyzing the three models, I think KNN Classifier can classify better compared to others.We can improve the accuracy by dealing the dataset imbalance through better modeling techniques.




## References:
https://medium.com/analytics-vidhya/los-angeles-crime-data-analysis-using-pandas-a68780d80a83

