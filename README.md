# bay-wheels
This repo inlcudes the file used to analyze Lyft Bike Rental Bay Wheel's ride data from the San Francisco Bay Area.
A regression model to is implemented to predict ride times depending on ride distance, start and end stations and bike type.

# Data Used
I pulled data from https://s3.amazonaws.com/baywheels-data/index.html which includes trip duration, start and end timestamps and start and end stations as well as coordinates for each Bay Wheel bike trip in the Bay Area.

# Process
First, I used start and end station ID's to keep only the rides which started and ended in San Francisco. 

