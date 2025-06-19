Problem Statement:
 

Key Factors Influencing Demand:
Demand for bus journeys is influenced by a range of factors, including holiday calendars, wedding seasons, long weekends, school vacations, and exam schedules. Additionally, regional holidays can affect different areas differently, and day-of-week effects further shape booking patterns. However, not all holidays significantly impact demand, making it a complex and non-trivial problem to model.

 
The Hackathon Challenge:
In this hackathon, your task is to develop a model that accurately forecasts demand for bus journeys. We will provide historical booking data from our platform, including the following:

Seats booked: Historical demand data.
Date of journey: The actual travel date.
Date of issue: The date when the ticket was booked.
Search data: The number of users searching for a particular journey date on a given booking date.
Your goal:

Predict the demand (total number of seats booked) for each journey at the route level, 15 days before the actual date of journey (doj).
Example: For a route from Source City "A" to Destination City "B" with a date of journey (doj) on 30-Jan-2025, you need to predict the final seat count for this route on 16-Jan-2025, which is exactly 15 days prior to the journey date.

You can download the training and testing datasets at the bottom of the Problem Statement.

Evaluation Metric:
 

The evaluation metric for this hackathon would be RMSE (Root Mean Squared Error).


Public-Private Split
 

Data Division:

The test data for the competition is divided into two parts:
Public Data (30%): Used for initial evaluation.
Private Data (70%): Used for final evaluation.
Scoring and Leaderboard Updates:

During the competition, your initial responses will be checked and scored based on the Public Data.
The scores obtained will be displayed on the Public Leaderboard, reflecting your progress in real-time.
The leaderboard will reflect the participants’ standings in real-time based on the scoring metric mentioned in the problem statement.
Final Rankings:

Once the competition concludes, the Private Data will be used to compute the final scores.
The final rankings will be based on the Private Score, which will be revealed only after the competition ends.
External Data Usage
 

Participants are not allowed to use the following external data:

Any similar dataset from publicly available repositories or sources.
Seat booking information from any other aggregator or source across the globe.
Other external data, such as holidays, events, and holiday calendars (regional and national) that are publicly available and relevant to the problem statement, are allowed.

Modelling Tools 
 

The only allowed programming language is Python.
Open-source libraries and frameworks are allowed.
Ethics and Compliance
 

Plagiarism or any other unethical behaviour will lead to disqualification.
Fair play is expected throughout the event.
Data dictionary
 

 

The following table provides a comprehensive data dictionary, outlining the structure and description of each variable used in the given dataset.

 

1. train.csv

 

Variable

Description

doj (Date of Journey)

The date on which the bus journey is scheduled to take place.

srcid (Source City ID)

Unique identifier for the source city of the journey.

destid (Destination City ID)

Unique identifier for the destination city of the journey.

final_seatcount

Total number of seats booked at the end of the journey date (Target Variable).

 

 

2. test.csv

 

Variable

Description

route_key

Unique identifier for each row in the test set.

doj (Date of Journey)

The date on which the bus journey is scheduled to take place.

srcid (Source City ID)

Unique identifier for the source city of the journey.

destid (Destination City ID)

Unique identifier for the destination city of the journey.

 

 

3. transactions.csv

 

Variable

Description

doj (Date of Journey)

The date on which the bus journey is scheduled to take place.

doi (Date of Issue)

The date when the ticket was booked.

dbd (Days Before Departure)

The number of days remaining until the journey date from the date of issue, for a given srcid, destid, doi and doj combination.

srcid (Source City ID)

Unique identifier for the source city of the journey.

destid (Destination City ID)

Unique identifier for the destination city of the journey.

srcid_region

The region (state) where the source city is located.

destid_region

The region (state) where the destination city is located.

srcid_tier

The tier classification of the source city (e.g., Tier 1, Tier 2).

destid_tier

The tier classification of the destination city (e.g., Tier 1, Tier 2).

cumsum_seatcount

This represents the cumulative number of seats sold till date.

cumsum_searchcount

This will represent the cumulative number of searches till date.

 

4. submission_file.csv

 

Variable

Description

route_key

Unique identifier for each row in the test set.

final_seatcount

Total number of seats booked at the end of the journey date (Target Variable).

 

 

Data
