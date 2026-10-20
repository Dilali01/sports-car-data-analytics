# sports-car-data-analytics

#### Project Overview

This project explores a dataset of sports cars to understand the relationships between vehicle performance, powertrain type, manufacturing year, and price.

The goal is to apply Python data analysis techniques to a real-world-style dataset, identify patterns, investigate relationships between numerical variables, and communicate findings through data visualizations.

This is my first independent data analytics project, developed as part of my journey toward becoming a data analyst.

Objectives
**The main objectives of this project are to:****

- Clean and prepare the dataset for analysis.
- Explore the distribution of sports car prices.
- Investigate the relationship between horsepower, torque, acceleration, and price.
- Compare car prices across manufacturing years.
- Explore differences between car manufacturers.
- Examine price and performance patterns across powertrain categories.
- Communicate findings using statistical summaries and visualizations.

Dataset

The dataset contains information about sports cars, including their specifications and prices.

The columns used in the analysis include:

Column| Description
"Car Make"| The manufacturer that produced the vehicle
"Car Model"| The name or model of the vehicle
"Year"| The manufacturing year
"Engine Size (L)"| Engine size in litres or a non-numeric label for some vehicles
"Horsepower"| The vehicle's horsepower
"Torque (lb-ft)"| Torque measured in pound-feet
"0-60 MPH Time (seconds)"| Time required to accelerate from 0 to 60 mph
"Price (in USD)"| The vehicle's price in US dollars
"Powertrain"| An additional classification used to group vehicles by powertrain type

The original dataset is stored in "sports-car-csv.csv".

Tools and Technologies

- Python — programming language used for the analysis.
- Pandas — data manipulation, cleaning, grouping, and statistical summaries.
- Matplotlib — data visualization.
- Jupyter Notebook — interactive environment for writing and documenting the analysis.
- VS Code — development environment.

Project Workflow

1. Data Loading and Inspection

The dataset was loaded into a Pandas DataFrame.

Initial inspection involved examining the dataset's structure, column names, data types, missing values, and descriptive statistics. This helped identify data quality issues and determine which variables were suitable for analysis.

2. Data Cleaning and Preparation

The following preparation steps were undertaken:

- Inspected the dataset for missing values and inconsistent entries.
- Replaced placeholder engine-size values such as "0" and "-" with missing values where appropriate.
- Removed duplicate records identified during cleaning.
- Investigated non-numeric entries in the "Engine Size (L)" column, including labels associated with electric and hybrid vehicles.
- Created a separate "Powertrain" column to classify vehicles into combustion, electric, and hybrid categories.
- Examined missing torque values and their relationship to vehicles with non-traditional engine-size entries.

The original "Engine Size (L)" column was retained because non-numeric entries can still provide useful information about a vehicle's powertrain. Creating a separate classification column allowed these vehicles to remain available for other analyses.

Missing values were treated carefully rather than automatically replacing every missing measurement with an average. This helped avoid making unsupported assumptions about vehicles whose specifications were unavailable.

3. Exploratory Data Analysis

Descriptive statistics and grouping operations were used to investigate the dataset.

The analysis included:

- Calculating summary statistics for numerical variables.
- Examining the distribution of car prices.
- Identifying the highest- and lowest-priced vehicles.
- Comparing prices between 2021 and 2022.
- Comparing Tesla prices across those two years.
- Investigating relationships between horsepower, torque, acceleration time, and price.
- Comparing average price and horsepower across car manufacturers.
- Examining price distributions across powertrain categories.

Key Findings

1. Distribution of Sports Car Prices

The price distribution is strongly right-skewed.

The mean price is approximately $390,585, while the median is approximately $133,050. The mean being considerably higher than the median indicates that a relatively small number of extremely expensive vehicles influence the overall average.

The highest recorded price was $5,200,000, associated with Bugatti Chiron entries from 2021 and 2022. The lowest recorded price was $25,000, associated with Chevrolet Camaro entries from those same years.

This illustrates why examining both the mean and median is useful when analysing prices with extreme values.

2. Horsepower and Price

The Pearson correlation between horsepower and price was approximately 0.78.

This indicates a strong positive linear relationship: vehicles with higher horsepower generally tend to have higher prices in this dataset.

However, the relationship is not perfect. Vehicles with comparable horsepower can have substantially different prices, suggesting that performance alone does not explain vehicle pricing.

Other factors, including manufacturer, model, exclusivity, technology, and rarity, may also contribute to price differences.

3. Horsepower and Torque

The correlation between horsepower and torque was approximately 0.95, indicating a very strong positive relationship.

In this dataset, vehicles with higher horsepower tend to have higher torque as well.

Although these variables are related, they measure different aspects of vehicle performance and should not be treated as interchangeable.

4. Horsepower and Acceleration Time

The correlation between horsepower and 0–60 mph acceleration time was approximately -0.73.

The negative relationship indicates that higher-horsepower vehicles generally tend to have lower acceleration times, meaning they can accelerate from 0 to 60 mph more quickly.

However, acceleration also depends on other characteristics, including vehicle weight, traction, drivetrain, and power delivery.

5. Price and Acceleration Time

The correlation between price and 0–60 mph time was approximately -0.50.

This suggests a moderate negative relationship: more expensive vehicles tend to have quicker acceleration in the dataset.

The relationship is not strong enough to conclude that price alone determines acceleration performance.

6. Price Comparison Between 2021 and 2022

The average recorded price was approximately:

- 2021: $398,721.90
- 2022: $376,583.20

The median recorded price was approximately:

- 2021: $160,947.50
- 2022: $102,600

The 2022 median was approximately $58,347.50 lower than the 2021 median.

The mean and median comparisons show that the two year groups have different price distributions. However, these results compare the vehicles represented in each year, not the price changes of identical models over time.

Differences in the models represented in each group and the presence of extremely expensive cars may influence the results.

7. Tesla Price Comparison Between 2021 and 2022
This Tesla analysis produced a focused investigation.
it's relevance is to narrow the scope to one manufacturerand compare its prices across 2021 and 2022

The Tesla comparison produced the following summary:

Statistic| 2021| 2022
Number of records| 5| 11
Mean price| $137,092| $163,869
Median price| $139,990| $141,190
Minimum price| $131,100| $119,000
Maximum price| $141,990| $200,000

The 2022 Tesla group had a higher mean price, while the median increased by only $1,200.

The difference between the mean and median changes suggests that the distribution of prices differed between the two groups. The 2022 group also had a wider observed price range.

These findings should be interpreted cautiously because the groups contain different numbers of records and may represent different Tesla models or configurations.

8. Manufacturer Comparison

Grouping vehicles by manufacturer and calculating average price and horsepower revealed differences between brands.

In this dataset:

- Bugatti had the highest average price.
- Rimac had the highest average horsepower.

These results illustrate that the manufacturer with the highest average price is not necessarily the one with the highest average horsepower.

Brand positioning, exclusivity, engineering, and other vehicle characteristics may contribute to these differences.

9. Powertrain Comparison

The powertrain analysis compared combustion, electric, and hybrid vehicles.

The visualizations revealed that:

- Combustion vehicles represented the dominant group in the plotted data and included numerous high-price outliers.
- Electric vehicles displayed a wide spread of prices, including some very expensive, high-horsepower vehicles.
- Hybrid vehicles had fewer visible observations, making broad comparisons less reliable.
- The price distributions of the different powertrain categories overlapped in some areas.

These patterns describe the vehicles represented in this dataset. They should not be interpreted as universal statements about all combustion, electric, or hybrid vehicles.

Data Visualizations

The project includes the following visualizations, created using Matplotlib.

1. Sports Car Price Distribution

A histogram was used to examine the distribution of vehicle prices and reveal the right-skewed pattern caused by a small number of very expensive vehicles.

2. Horsepower vs. Price

A scatter plot was used to investigate the relationship between horsepower and price. The visualization showed a general positive relationship alongside substantial variation in prices among vehicles with similar horsepower.

3. Horsepower vs. Price by Powertrain

A multivariate scatter plot used different colours to distinguish combustion, electric, and hybrid vehicles. This enabled a comparison of price and horsepower patterns across powertrain categories.

4. Correlation Heatmap

A correlation heatmap was created using Matplotlib to compare the linear relationships between horsepower, torque, 0–60 mph acceleration time, and price.

The heatmap highlighted the strong positive relationship between horsepower and torque, the positive relationship between horsepower and price, and the negative relationship between horsepower and acceleration time.

5. Price Distribution by Powertrain

A box plot was used to compare the distribution of prices across powertrain categories. It helped identify differences in medians, price spreads, and potential outliers.

Limitations

Several limitations should be considered when interpreting the results:

- The findings depend on the quality, completeness, and representativeness of the supplied dataset.
- Extreme prices can influence averages and make visual comparisons difficult.
- Missing vehicle specifications may affect some calculations and comparisons.
- Powertrain categories contain different numbers of observations.
- Comparisons between years may involve different vehicle models rather than the same models measured at different times.
- Correlation measures linear association and does not establish causation.
- The analysis does not control for every factor that can influence vehicle prices or performance.

The findings therefore describe patterns in the available data rather than universal relationships across the entire sports car market.

Project Structure

The project is organized around the following files and folders:

sports-car-data-analytics/
├── sports-car-csv.csv
├── analysis.ipynb
├── visualizations/
├── README.md
└── requirements.txt

- "sports-car-csv.csv" — the original dataset.
- "analysis.ipynb" — the notebook containing data cleaning, exploratory analysis, calculations, visualizations, and interpretations.
- "visualizations/" — intended for exported chart images.
- "README.md" — project documentation and key findings.
- "requirements.txt" — Python dependencies required to run the project.

The "visualizations/" directory may remain empty while the charts are displayed directly inside the notebook.

How to Run the Project

Prerequisites

Install Python and ensure that Jupyter Notebook is available.

1. Clone or download the project

Download the repository to your computer, or clone it using Git.

2. Open the project directory

Open the folder in VS Code.

3. Install the dependencies

Run the following command in the terminal:

pip install -r requirements.txt

4. Open the notebook

Open "analysis.ipynb" in VS Code and select a Python kernel.

5. Run the notebook

Run the cells from top to bottom to reproduce the cleaning steps, analyses, and visualizations.

Future Improvements

Possible extensions to the project include:

- Exporting finished visualizations into the "visualizations/" directory.
- Investigating additional relationships between vehicle specifications and price.
- Comparing price distributions using alternative scales where extreme values compress the charts.
- Examining individual manufacturers and models in greater detail.
- Improving the handling and documentation of missing values.
- Exploring predictive modelling to investigate how well vehicle specifications can estimate price.

Conclusion

This project applied Python-based data analytics techniques to explore sports car prices and performance characteristics.

The analysis identified a strong positive relationship between horsepower and price, a very strong positive relationship between horsepower and torque, and a negative relationship between horsepower and 0–60 mph acceleration time.

Comparisons across manufacturing years, manufacturers, and powertrain categories revealed additional differences in the dataset. Visualizations helped communicate these patterns and highlight extreme values that can influence statistical summaries.

Beyond the individual findings, the project provided practical experience in data cleaning, exploratory data analysis, correlation analysis, visualization, and documenting analytical results.

The project represents an initial step in developing practical data analytics skills using Python.