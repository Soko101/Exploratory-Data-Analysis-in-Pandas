# Exploratory-Data-Analysis-in-Pandas
Exploratory Data Analysis (EDA) in Pandas
In this notebook, I explored a global population dataset using pandas, seaborn, and matplotlib to uncover 
trends across countries, continents, and decades, spanning from 1970 all the way to 2022.

I started by loading a comprehensive dataset containing yearly population data for nearly every country, as well as attributes like continent, capital, area size (km²), density, and growth rate.

Cleaned & formatted it

- To make the dataset more readable, I used pd.set_option() to format large numbers with commas. I also performed basic checks with .info() and .describe() to inspect the data types, spot null values, and understand the scale of the dataset.

Grouped by Continent

- Using groupby() and .mean(), I calculated average population figures for each continent across multiple decades.
- This helped me quickly identify that Asia and Africa have had the largest population growth over time, while continents like Oceania and Europe have experienced relatively slower growth.

Visual Insight: I created a bar chart to compare average 2022 population by continent.

- Observation: Asia dominated with the highest population, followed by Africa — whose average growth rate was significantly higher than Europe’s.

Visualized Key Relationships
  
- To dig deeper into how features relate, I used seaborn.heatmap() to build a correlation matrix between population, area, density, and growth rate.

Correlation Heatmap Observation:

There’s a strong correlation between population across decades (as expected).

Interestingly, population size had a weak correlation with area, but moderate correlation with population density, suggesting population concentration rather than land mass.

Sorted & Filtered for Insights

I used sort_values() to rank countries and identify outliers and patterns:

Which countries had the highest growth rates (e.g., many African nations)?

Which had declining populations (notably some island nations)?

Which regions were densely populated despite small land size (like Bangladesh, or city-states like Singapore)?

I also used conditional filtering to isolate interesting subsets — like countries with over 100M people in 2022, or nations with <1% growth despite large land areas.
