# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data(weather prediction in aus) 

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import zipfile
import pandas as pd
import matplotlib.pyplot as plt

# Step 1: Extract the ZIP file
with zipfile.ZipFile("weatherAUS.csv.zip", "r") as zip:
    zip.extractall("weather_data")

# Step 2: Read the CSV file
df = pd.read_csv("weather_data/weatherAUS.csv")

# Step 3: Convert Date into datetime format
df['Date'] = pd.to_datetime(df['Date'])

# Step 4: Select weather data for Albury
df = df[df['Location'] == 'Albury']

# Step 5: Plot Maximum Temperature
plt.plot(df['Date'], df['MaxTemp'])

plt.title("Maximum Temperature in Albury")
plt.xlabel("Date")
plt.ylabel("Maximum Temperature (°C)")
plt.grid()
plt.show()

```

# OUTPUT:

<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/ef3e6f54-425b-4c3b-9441-2081a060b96e" />






# RESULT:
Thus we have created the python code for plotting the time series of given data.
