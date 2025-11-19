# Objective

The objective of this project is to analyze airline operational efficiency focusing on passenger transport, flight distribution, and load factor performance. This analysis helps identify which carriers, routes, and time periods contribute most to business growth and where strategic optimization is required to maximize revenue and flight utilization.

# Project Highlights

The dashboard focuses on the following performance areas:

Load Factor Efficiency

Carrier-wise Passenger Transport & Load Factor

Distance-based Flight Distribution

Monthly Load Factor Trends

Top Performing Routes

Weekday vs Weekend Flight Utilization

Filter-based Dynamic Operational Insights

# Dashboard Overview

<img width="1594" height="831" alt="image" src="https://github.com/user-attachments/assets/590ad647-0263-43d2-b5f2-2f4449823f37" />


The dashboard uses KPI cards, bar charts, line graphs, a donut chart, and slicers. Key filters include:

✔ Year, Quarter, Month
✔ Destination State/Country
✔ Carrier Name

This enables drill-down capability for deeper insights.

# Dashboard Insights
🔹 Top KPIs
Metric	Value
Available Seats	244M
Total Flights	111K
Total Passengers	187M
Load Factor	76.8%
Total Distance	82M

These KPIs provide a quick high-level overview of airline operational performance.

✈ Load Factor % by Carrier Name

Carriers like Globespan Airline and Allegiant Air show the highest load factor efficiency.

Lower-performing carriers need focus on demand generation or capacity optimization.

📍 Top Routes by Passenger Count

Routes such as Chicago – Atlanta, Washington – Atlanta are among the most preferred, with consistent passenger volume.

These routes show high-demand connectivity hubs.

📊 Flight Distribution by Distance Group

Short-to-medium distance routes account for maximum flight volume.

Long-distance routes have fewer but typically higher-capacity flights.

👥 Passengers Transported by Carrier

Southwest Airlines, Delta Air Lines, and US Airways transport the highest passenger count.

These carriers significantly contribute to total business revenue.

🗓 Weekday vs Weekend Performance

Weekdays contribute ~76.8% of total flights, indicating higher business travel.

Weekends show less activity (~23.2%), showing opportunities for leisure flight promotion.

📆 Monthly Load Factor Trend

Load factor increases steadily from January and peaks during June–July, suggesting seasonal high travel.

Slight drop during September–October before stabilizing toward year-end.

📌 Combined Analysis – Total Flights & Load Factor by Carrier Group

Some carrier groups operate more flights with lower load factors.

Strategic route planning or pricing adjustments can help increase occupancy.

# DAX Formulas Used
TotalFlights = COUNT(Flights[FlightID])

TotalPassengers = SUM(Flights[PassengersTransported])

AvailableSeats = SUM(Flights[SeatCapacity])

LoadFactor = DIVIDE(SUM(Flights[PassengersTransported]), SUM(Flights[SeatCapacity]), 0)

LoadFactorMonth = AVERAGE(Flights[LoadFactor])

FlightsByDistance = COUNTROWS(FILTER(Flights, Flights[DistanceGroupID] IN SELECTEDVALUE(DistanceGroupID)))

WeekdayFlights = CALCULATE(COUNT(Flights[FlightID]), Flights[Week_Type] = "Weekday")

WeekendFlights = CALCULATE(COUNT(Flights[FlightID]), Flights[Week_Type] = "Weekend")

# Conclusion & Recommendations

✔ Focus on high-demand routes and carriers to maximize profits.
✔ Enhance marketing for weekend travel to improve occupancy.
✔ Optimize long-distance flight scheduling to increase utilization.
✔ Strengthen collaboration with top-performing airlines.
✔ Investigate low-performing months and implement seasonal promotion strategies.
✔ Ensure frequent monitoring of load factor for fleet optimization.
