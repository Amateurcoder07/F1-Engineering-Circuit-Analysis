F1 Circuit Engineering Analysis 
SQLserver + Power BI Data Project 

Overview 

Formula 1 is one of the most complex sports in the world. 
Behind every race is a mix of vehicle engineering, track design, and environmental conditions 
that all influence performance. 
In this project, I explored Formula 1 circuits from a data and infrastructure perspective. Instead 
of focusing only on drivers or teams, I looked at how track characteristics affect speed, 
overtaking, and safety. 

Using SQL Server and Power BI, I analyzed historical race data to answer questions like: 

    1. Do high-altitude circuits make cars faster? 
    2. Which tracks allow the most overtaking? 
    3. Are street circuits more dangerous than permanent ones? 
    4. Does elevation change increase crash risk? 
    5. Do more corners actually slow cars down? 

The goal was to turn raw racing data into clear engineering insights using data analysis. 

Dataset 

The dataset used was “Formula 1 World Championship (1950–2024)” from Kaggle. 
From the full dataset, four tables were mainly used: 
    1. Circuits 
    2. Races 
    3. Results 
    4. Status 

These were imported from Excel into Microsoft SQL Server for cleaning and analysis. 

Data Preparation 

Before analysis, the dataset needed some cleanup. 
During import, SQL Server incorrectly stored several numeric fields as text (NVARCHAR). 
Columns like starting position, finishing position, and speed values were converted to proper 
numeric types so calculations would work correctly. 
Another issue was the value \N, which represents missing data in the dataset. 
These were replaced with NULL values so queries could run without errors. 
Once the data was cleaned, it was ready for analysis. 

Data Modeling 

To make analysis easier, three SQL views were created. 

1. F1 Engineering Master View 
This view combines race results with track information such as altitude, corner count, and track 
length. 
It also creates two useful metrics: 
Corner Density → number of corners per kilometer 
Overtaking Score → positions gained during a race 

2. F1 Safety Audit View 
This view focuses on race incidents. 
It scans race status descriptions and flags crash-related events like accidents, collisions, and 
spins. 
From this, an Incident Rate is calculated to compare how risky different circuits are. 

3. F1 Geometric Efficiency View 
This view measures how technically demanding a track is by calculating Corner Density. 
Tracks with many corners per kilometer are more technical and usually produce slower average 
speeds. 


Visual Analysis 

Seven Power BI visuals were created to explore different patterns in the data. 

1. Altitude vs Speed 
Tests whether high altitude reduces drag and increases speed. 
Result: altitude matters less than track layout. 

2. Overtaking by Circuit 
Shows which tracks allow the most position changes. 
Wide tracks with long straights encourage overtaking, while tight circuits like Monaco create 
bottlenecks. 

3. Elevation Change vs Incident Rate 
Tracks with larger elevation changes tend to show slightly higher incident rates.

4. Street vs Permanent Circuits 
Street circuits show noticeably higher crash rates than purpose-built tracks. 

5. Failure Mode Analysis 
Breakdown of why drivers retire from races, including accidents and mechanical failures. 

6. Corner Density vs Speed 
Tracks with more corners per kilometer have significantly lower average speeds. 

7. Infrastructure Footprint 
Compares circuit lengths to highlight differences in project scale and infrastructure 
requirements. 

What I Learned From This Project 

A few things became very clear while working on this project: 
    1. F1 is ridiculously complex. It's not just cars going fast - it's engineering, physics, and 
    infrastructure all interacting at once. 
    2. Track design matters more than you think. A circuit’s geometry can limit speed even for 
    the fastest cars. 
    3. Street circuits look cool but are risky. Less space means fewer recovery options. 
    4. Corners are natural speed limiters. More curves = slower average speed, no matter how 
    powerful the car. 
    5. Data cleaning is half the work. Fixing data types and missing values took almost as 
    much effort as the analysis itself. 
    6. SQL + Power BI is a powerful combo. SQL handles the heavy data work, while Power BI 
    makes patterns obvious. 

Tools Used 

    Microsoft SQL Server 
    SQL Server Management Studio 
    Power BI 
    Excel 
    GitHub 

Final Thoughts 

This project shows how historical motorsport data can be used to study speed, safety, and 
infrastructure design through data analysis. 
It was also a reminder that Formula 1 is not just a sport, it's a fascinating system where 
engineering decisions shape the outcome of every race. 

