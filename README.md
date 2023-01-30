# bay-wheels
This repo inlcudes the file used to analyze Lyft Bike Rental Bay Wheel's ride data from the San Francisco Bay Area.
A linear regression model is implemented to predict ride times depending on ride distance, start and end stations and bike type.

# Data Used
I pulled data from https://s3.amazonaws.com/baywheels-data/index.html which includes trip duration, start and end timestamps and start and end stations as well as coordinates for each Bay Wheel bike trip in the Bay Area.

# Process
First, I used start and end station ID's to keep only the rides which started and ended in San Francisco. I changed each ride's start and end coordinates to be the mean coordinates of their start and end station in order to track the frequency of each station as a start and end destination. I used these frequencies to plot the start and end stations on a map with larger dots representing stations with higher frequencies of rides. Next, I used the haversine distance formula and the start and end coordinates of the rides to find the distance of the ride. In order to make my regression model more effective, I removed the largest outliers and kept only the rides where the average seconds/mile was within two standard deviations of the mean. Finally, I made graphs plotting the distance versus time of rides and trained my linear regression model to predict ride time based off of ride distance, bike type, start and end station and user type.

# Results

Scatter plot of ride start locations (larger dot means higher frequency)

![image](https://user-images.githubusercontent.com/122834710/214666727-33a511e3-8004-4242-90db-bd541255fac6.png)

Scatter plot of ride end locations (larger dot means higher frequency)

![image](https://user-images.githubusercontent.com/122834710/214666660-1fde2285-e2ee-4584-95db-d1aefe2fd033.png)

Distance vs. Ride Time (without outliers removed)

![image](https://user-images.githubusercontent.com/122834710/214666074-71eb19f7-8bff-4a0a-a4a0-747b2379a737.png)

Distance vs Ride Time (outliers removed)

![image](https://user-images.githubusercontent.com/122834710/214666314-86307c0a-3a04-442d-a186-4bcbbf8bcf63.png)

Finally, results of my logistic regression model:

Coefficient of Determination: 0.7144931901646129
Intercept: 268.993173760169


