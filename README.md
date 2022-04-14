# crime-data-analysis
Los Angeles Crime Data Analysis
# data link - https://data.lacity.org/api/views/2nrs-mtv8/rows.csv?accessType=DOWNLOAD

## Abstract:
a subject with conversations about crime analysis in the city all over the planet. After some investigates to observe open information, I've chosen to investigate the information in Los Angeles city. Confined in the south of California, it's the subsequent more inhabited city in the United States (just behind New York), it's the focal point of the film and media business.
Although crimes are committed at unexpected times, crime is a difficult topic for analytics and prediction, and therefore no actual crime prediction model could ever be as accurate as "Minority Report." 
Evaluating criminal background information to predict illegal acts could made in decreasing crime rates as well as preventing future losses. 
This crime report recommends the least and also most dangerous areas by evaluating the dataset.



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

Vict Descent - Descent Code: A - Other Asian B - Black C - Chinese D - Cambodian F - Filipino G - Guamanian H - Hispanic/Latin/Mexican I - American Indian/Alaskan Native J - Japanese K - Korean L - Laotian O - Other P - Pacific Islander S - Samoan U - Hawaiian V - Vietnamese W - White X - Unknown Z - Asian Indian Premis Cd - The type of structure, vehicle, or location where the crime took place. Premis Desc - Defines the Premise Code provided. Weapon Used Cd - The type of weapon used in the crime. Weapon Desc - Defines the Weapon Used Code provided. LOCATION - Street address of crime incident rounded to the nearest hundred block to maintain anonymity. LAT - Latitude Coordinate. LON - Longitude Coordinate.

## exploratory data analysis:

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




References:
https://medium.com/analytics-vidhya/los-angeles-crime-data-analysis-using-pandas-a68780d80a83

