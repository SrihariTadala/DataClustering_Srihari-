  
This week, I worked on preparing the dataset for clustering. I looked at how it was put together, made sure there were no missing or inconsistent values, and cleaned the data. There were a lot of misspelled or inconsistent borough names in the dataset, which could make analysis and clustering less accurate. I fixed this by making all the text lowercase, removing extra spaces, and then making a mapping dictionary to fix the differences.

For example, names like “manhhattan,” “quen” or “staten isalnd” were standardized to their proper boroughs (“Manhattan,” “Queens,” and “Staten Island”). After applying this mapping, I filtered the data to include only the five official boroughs — Manhattan, Brooklyn, Queens, Bronx, and Staten Island.

I watched a Microsoft Research lecture on Clustering and Facility Location Problems and read parts of Sara Ahmadian's PhD thesis to help me understand better. Explained how to think of clustering as a facility-location optimization problem that finds a small number of centers (facilities) that can meet the needs of a lot of clients.

Using GeoPandas, I turned the dataset into a GeoDataFrame, which gave each incident a real spatial geometry. I changed the coordinates from latitude-longitude (EPSG:4326) to the New York State Plane coordinate system (EPSG:2263) so that I could accurately calculate the distance in feet. I also got the x and y values for numerical clustering. With Folium, I made a heat map that shows where incidents are most common in New York City in a way that makes sense spatially.

Once the data was cleaned, I ran initial visualizations to understand patterns and relationships between features.

