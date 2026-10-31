# TSA-Ex-1a
# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```
from matplotlib import pyplot as plt
import pandas as pd

# Read the dataset
df = pd.read_csv("/content/ice_cream.csv")

# Display first five rows
print(df.head())

# Convert DATE column to datetime
df['DATE'] = pd.to_datetime(df['DATE'])

# Check data types
print(df.dtypes)

# Set DATE as index
df.set_index('DATE', inplace=True)

# Plot the time series data
df['IPN31152N'].plot(
    kind='line',
    label='Ice Cream Data',
    color='black'
)

# Add title and labels
plt.title('Time Series Plot of Ice Cream Data')
plt.xlabel('Date')
plt.ylabel('IPN31152N')
plt.legend()
plt.grid(True)
plt.show()
```










# OUTPUT:

<img width="722" height="352" alt="image" src="https://github.com/user-attachments/assets/86c4cbf9-552c-4f3c-988d-7c6dc45487a1" />





# RESULT:
Thus we have created the python code for plotting the time series of given data.
