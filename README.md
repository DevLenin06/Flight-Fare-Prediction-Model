# Flight Fare Prediction Model (in-progress)

## Overview
This model(in-progress) focuses on predicting flight prices based on various features such as airline, journey date, source, destination, and more. The data for this project comes from flight booking details, with information about flight routes, times, stops, and additional information.

The goal of this project is to clean the dataset, analyze the features, and build a model that can predict the price of a flight based on the given features.

## Data
The dataset used for this project is available in an Excel file: `Data_Train.xlsx.`

### Columns
1. Airline: The airline company operating the flight.
2. Date_of_Journey: The date when the flight is booked.
3. Source: The departure airport.
4. Destination: The arrival airport.
5. Route: The series of airports the flight takes during its journey.
6. Dep_Time: Departure time of the flight.
7. Arrival_Time: Arrival time of the flight.
8. Duration: The total duration of the flight.
9. Total_Stops: The number of stops during the flight (non-stop, 1 stop, 2 stops, etc.).
10. Additional_Info: Additional information about the flight.
11. Price: The price of the flight (target variable).

  ### Data Pre-processing
  1. Handling Missing Data:
     - We identified and handled missing values in the dataset.
     - In particular, the `Route` and `Total_Stops` columns had a few missing values. The row with missing `Total_Stops` was dropped to avoid any inconsistency.
  2. Data Type Conversion:
     - The columns `Date_of_Journey`, `Dep_Time`, and `Arrival_Time` were initially in string format. These need to be converted into proper `datetime` objects.
     - The `Total_stops` column is categorical (eg non-stop, 1 stop, etc.) so it needs to be converted to numeriacl format to use for a machine-learning model.       
  3. Additional Processing:
     - The `Duration` column, which contains data in hours and minutes (e.g., 2h 50m), needs to be split and converted into a numeric value (total minutes or hours).
    

