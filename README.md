# data_1_project
This project is intended to provide a place to manipulate, modify, and view data exported as CSV from TeslaFi data logger.

The primary CSV for this project is "TeslaFi92022 (updates for project).csv".

This project was was created in Visual Studio Code V1.73.1
Required imports are:
-import pandas as pd
-import numpy as np
-import matplotlib as mpl
-import matplotlib.pyplot as plt
-import statistics


Feature of the product include:
Feature 1: Read Data in
Data read in from local CSV 'TeslaFi92022 (updates for project).csv'

Feature 2: Use built-in Pandas or Numpy functions to clean the data.
There are multiple cleanings of the data...
FIRST Cleaning: Scrubbing of data to only show when vehicle state is 'online'
SECOND Cleaning: Scrub to show when - Vehicle state is "Online"; Time to Full Charge == number; AND, Charger Actual Current == number 
THIRD Cleaning: We still have a lot of data. Use of dropna() to clear rows with null/NaN values to give us a nice workable dataset.  This dataset was saved as the variable 'clean_Tesla'.

Feature 3: Analyze your data (five required)
ONE: **statistics.mode** to find the most common State of Charge Limit in the month of September
TWO: **np.sum** to total the column "charge_miles_added_rated"
THREE: **np.median** we see the median mileage added per charge
FOUR: **np.mean** applied to charge_limit_soc tell us the average charge limit set for the entire month
FIVE: **Divided Columns** divided battery range and maximum range columns from our dataframe and multiplied that result by 100 to give us the average percentage of max range used.  These results have been added as an additional column titled "avg_percentage_used".
OTHER: **value_counts** to see how many days of the month were captured


Feature 4: Visualize your data (two required)
PLOT 1: 
PLOT 2: 
PLOT 3: 
