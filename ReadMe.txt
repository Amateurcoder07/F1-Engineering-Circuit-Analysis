1\. v\_F1\_Engineering\_Master  //Tanmay //shivadey

This is the Master Connector. Imagine you have a pile of maps, a list of race times, and a list of driver names. This view takes all those separate files and glues them together into one big, organized spreadsheet.



* What it does (Technical Detail)

1. The Triple Join: It uses SQL JOIN commands to link three tables: Races (the events), Results (the performance), and Circuits (the physical location).



2\. Feature Engineering: It calculates the Overtaking Score by subtracting a driver's starting position from their finishing position.



* Why it matters (Engineering Insight)

1. It allows us to analyze how a driver's speed changes based on the Altitude of the track.



2\. It provides the Ground Truth data needed to prove that thin air at high altitudes reduces aerodynamic drag, allowing for higher velocities.



---------------------------------------------------------------------------------------------------------------------------------------------------



2\. v\_F1\_Safety\_Audit

This is a Risk Detector. In racing, cars break for many reasons—sometimes the engine blows up, and sometimes the driver hits a wall. This view filters out the mechanical stuff so we can focus strictly on crashes.



* What it does (Technical Detail)

1. Conditional Logic: It uses CASE WHEN statements to scan thousands of rows for specific keywords like 'Accident', 'Collision', or 'Spun off'.



2\. Standardization: It uses the CAST function to turn whole numbers into decimals so it can calculate a percentage called the Incident Rate.



* Why it matters (Engineering Insight)

1. As a Civil Engineer, you care about the Safety Coefficient of the road.



2\. This view proves whether Street Circuits (converted city roads) are more dangerous than Permanent Circuits (purpose-built tracks) by comparing their crash rates per 100 starts.



---------------------------------------------------------------------------------------------------------------------------------------------------



3\. v\_F1\_Geometric\_Efficiency

This is the Technicality Meter. It measures how busy a track is. If a track is 5km long and has 20 turns, it is much more technical than a 5km track with only 4 turns.



* What it does (Technical Detail)

1. Derived Metrics: It creates a new mathematical formula: Corner Count / Track Length.



2\. The Result: This gives us a number called Corner Density—the average number of corners a driver encounters per kilometer.



* Why it matters (Engineering Insight)

1. This is a study of Horizontal Alignment.



2\. It helps us prove a fundamental law of transportation: as the number of geometrical interruptions (corners) increases, the "mean operating speed" of the environment decreases, regardless of the vehicle's power.



---------------------------------------------------------------------------------------------------------------------------------------------------





Visual 1: Altitude vs. Top Speed Correlation (Scatter Chart)

The Engineering Hypothesis: We hypothesized that as the Altitude (independent variable) increases, the Average Speed (dependent variable) would increase due to a reduction in air density and aerodynamic drag.



What it Denotes

X-Axis (Topography): Represents the track's height above sea level in meters.



Y-Axis (Performance): Represents the mean peak velocity of the vehicles in KPH.



The Trend Line: A mathematical line of best fit that tracks the relationship between elevation and speed.



Key Observations

Atmospheric Impact: The upward slope of the trend line confirms a positive correlation. In civil engineering terms, this proves that site topography directly dictates the operational "speed ceiling" of a transit environment.



The "Mexico Outlier": You will notice a single dot far to the right (Autódromo Hermanos Rodríguez). While it has the highest altitude, its speed isn't the highest because its complex geometric design (many slow corners) counteracts the aerodynamic advantage of the thin air.



Visual 2: Comparative Overtaking by Track (Bar Chart)

The Engineering Hypothesis: We hypothesized that certain Horizontal Alignments (track layouts) are more "functionally efficient" for competitive racing than others.



What it Denotes

Vertical Axis (Infrastructure): A list of global racing circuits.



Horizontal Axis (Efficiency): The average number of positions gained per race. A higher number suggests a layout that facilitates passing.



Key Observations

Design for Competition: Tracks like Indianapolis or Spa-Francorchamps show high positive values. This denotes a "High-Flow" design featuring long straights and wide corner radii that allow for multiple racing lines.



The Bottleneck Effect: Tracks with negative or near-zero values (like Monaco or Zandvoort) are "Low-Flow" designs. As a Civil Engineer, this indicates that the road width and geometric constraints of the site create an infrastructure bottleneck where the starting position almost entirely dictates the outcome.



---------------------------------------------------------------------------------------------------------------------------------------------------



Visual 3: Vertical Gain vs. Infrastructure Risk (Scatter Chart)

The Engineering Hypothesis: We hypothesized that "rollercoaster" tracks with high vertical oscillation create blind corners and car instability, leading to a higher frequency of incidents.



What it Denotes: This chart plots the Elevation Change (total hilliness) against the Incident Rate (percentage of races ending in a crash or spin).



Analytical Observation: The trend line shows a positive correlation: as elevation change increases, the risk factor generally climbs.



Infrastructure Insight: For your portfolio, this proves that vertical alignment is a critical safety parameter. High-elevation tracks like Spa-Francorchamps (~102m) require more advanced runoff infrastructure than flatter tracks to maintain a similar safety coefficient.



Visual 4: Purpose-Built vs. Urban Infrastructure (Bar Chart)

The Engineering Hypothesis: We hypothesized that purpose-built tracks (Permanent) are inherently safer than converted city roads (Street) due to specialized engineering like gravel traps and soft barriers.



What it Denotes: A direct comparison of the Average Incident Rate between the two main categories of racing infrastructure.



Analytical Observation: Street Circuits show a significantly higher incident rate (nearly 16%) compared to Permanent Circuits (under 10%).



Infrastructure Insight: This is a clear lesson in Safety Infrastructure. It proves that the "forgiveness" of a track—the space available to recover from a mistake—is the primary driver of safety, regardless of the driver's skill.



Visual 5: Failure Mode Analysis (Donut Chart)

The Engineering Hypothesis: We hypothesized that while mechanical failures are common, infrastructure-related "Contact" events represent a major, distinct category of race termination.



What it Denotes: A 360-degree breakdown of Race Status—the "Why" behind every retirement in the dataset.



Analytical Observation: By viewing the full spectrum, we see that Accidents and Collisions occupy a large share of the "Failure Pie" alongside mechanical issues like Engine or Gearbox failures.



Infrastructure Insight: This provides a "Global Risk Profile." It tells a recruiter that you can perform a Forensic Audit of a system to identify where the highest probability of failure lies, which is a key skill for any engineer.



---------------------------------------------------------------------------------------------------------------------------------------------------



Visual 6: Corner Density vs. Mean Speed (Scatter Chart)

The Engineering Hypothesis: We hypothesized that Corner Density—the frequency of horizontal curves per unit of distance—acts as a natural speed governor, forcing lower mean velocities regardless of a vehicle's mechanical power.



What it Denotes: This chart plots the Corners per Kilometer against the Average Speed (KPH) for major international circuits.



Analytical Observation: The trend line shows a sharp negative correlation. Circuits with high corner density, such as Monaco (nearly 6 corners/km), show significantly lower mean speeds than high-speed "Power" circuits like Monza (under 2 corners/km).



Infrastructure Insight: This proves that the Horizontal Alignment (the curviness) of a road is the primary factor in determining its operational efficiency. For your portfolio, this shows you can quantify "technicality" into a measurable engineering metric.



Visual 7: Comparative Infrastructure Footprint (Bar Chart)

The Engineering Hypothesis: We hypothesized that the total land-use and structural scale of a racing project can be measured by its Track Length, which directly influences the logistical and maintenance complexity of the site.



What it Denotes: A comparison of the total Track Length (KM) for the four primary circuits in the study.



Analytical Observation: Spa-Francorchamps (~7km) represents the largest infrastructure footprint, being over twice the length of the Monaco street circuit (~3.3km).



Infrastructure Insight: This denotes the Scale of the Project. A larger footprint requires more extensive drainage systems, barrier maintenance, and emergency access planning. This visual helps a recruiter understand that you can analyze the physical dimensions and land-use requirements of massive civil projects.



---------------------------------------------------------------------------------------------------------------------------------------------------



Final Project Conclusion: The Engineering of Speed and Safety

Through this data-driven audit of Formula 1 infrastructure, we have mathematically proven that the physical environment is the ultimate "governor" of performance and risk.



1\. Topography as a Performance Driver

Our analysis confirms that Site Topography (Altitude) and Vertical Alignment (Elevation Change) are not just aesthetic features but active engineering variables.



Observation: Higher altitudes reduce aerodynamic drag, increasing top speeds.



Engineering Takeaway: When designing high-speed transit or racing environments, engineers must account for atmospheric density, as it shifts the "efficiency ceiling" of the vehicles using the infrastructure.



2\. The Infrastructure Safety Coefficient

The data shows a clear "Safety Gap" between different types of road infrastructure.



Observation: Street circuits (temporary urban roads) have an incident rate nearly 60% higher than purpose-built permanent tracks.



Engineering Takeaway: This proves that Forgiving Infrastructure—such as wide runoff areas, gravel traps, and energy-absorbing barriers—is significantly more effective at preventing system failures than simply relying on driver skill.



3\. Geometric Design and Operational Limits

By quantifying Corner Density, we have proven that the complexity of a road's Horizontal Alignment directly controls its mean operating speed.



Observation: There is a sharp negative correlation between the number of corners per kilometer and the average velocity achievable on a circuit.



Engineering Takeaway: In transportation planning, "technicality" acts as a natural speed regulator. Increasing the frequency of curves is a more effective method of speed control than signage alone, as it forces physical limits on the vehicle's trajectory.



Portfolio bs

This project demonstrates the transition from raw historical data to Forensic Engineering Insights. By leveraging SQL for complex data cleaning and Power BI for environmental modeling, I have created a tool that allows for the scientific audit of racing infrastructure, providing a roadmap for safer and more efficient high-performance road design.
