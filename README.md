# Tesla charge report analysis - September<br>
This project is intended to provide a place to import, modify, and view data from TeslaFi data logger that is a CSV file.<br>
<br>
The primary CSV for this project is "TeslaFi92022 (updates for project).csv".<br>
<br>
This project was was created in Visual Studio Code V1.73.1<br>
Required imports are:<br>
import pandas as pd<br>
import numpy as np<br>
import matplotlib as mpl<br>
import matplotlib.pyplot as plt<br>
import statistics<br>
<br>
<br>
Feature of the product include:<br>
Feature 1: Read Data in<br>
Data read in from local CSV 'TeslaFi92022 (updates for project).csv'<br>
<br>
Feature 2: Use built-in Pandas or Numpy functions to clean the data.<br>
There are multiple cleanings of the data...<br>
FIRST Cleaning: Scrubbing of data to only show when vehicle state is 'online'<br>
SECOND Cleaning: Scrub to show when - Vehicle state is "Online"; Time to Full Charge == number; AND, Charger Actual Current == number <br>
THIRD Cleaning: We still have a lot of data. Use of dropna() to clear rows with null/NaN values to give us a nice workable dataset.  This dataset was saved as the variable 'clean_Tesla'.<br>
<br>
Feature 3: Analyze your data (five required)<br>
ONE: **statistics.mode** to find the most common State of Charge Limit in the month of September<br>
TWO: **np.sum** to total the column "charge_miles_added_rated"<br>
THREE: **np.median** we see the median mileage added per charge<br>
FOUR: **np.mean** applied to charge_limit_soc tell us the average charge limit set for the entire month<br>
FIVE: **Divided Columns** divided battery range and maximum range columns from our dataframe and multiplied that result by 100 to give us the average percentage of max range used.  These results have been added as an additional column titled "avg_percentage_used".<br>
OTHER: **value_counts** to see how many days of the month were captured<br>
<br>
<br>
Feature 4: Visualize your data (two required)<br>
PLOT 1: Available range when online, by date<br>
PLOT 2: Requested amperage for charge, by date<br>
PLOT 3: Total range added by requested charge percentage<br>
