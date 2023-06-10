# SOLVING-TSP-WITH-BRUTE-FORCE
Finding the shortest distance on earthquake coordinates using the coordinates of the Kahramanmaraş earthquake on February 6, 2023, including the main earthquake and aftershock coordinates.

In this project, a seismologist aims to conduct a geological survey in earthquake-prone areas based on the earthquake that occurred on February 6, 2023, with its epicenter in Kahramanmaraş, and its aftershocks. The researcher's goal is to find the shortest route using the Traveling Salesman Problem (TSP) algorithm.

In this project, although there are other algorithms that can be used to potentially reach a solution faster than brute-force, the decision has been made to use the brute-force algorithm. Despite its time complexity, brute-force can provide a guaranteed solution for the Traveling Salesman Problem. It exhaustively explores all possible routes to find the shortest one. While other algorithms may offer more efficient approaches, the specific requirements or constraints of the project have led to the selection of the brute-force algorithm.

The documents included in this project are as follows:

1. Python file created using Jupyter Notebook.
2. A .csv file obtained from Kaggle, containing the coordinates of earthquakes and aftershocks.
3. A sample of ten entries from the aforementioned .csv file, used in the Python file.
4. Similarly, within the Python file, there is an .html file that showcases the shortest distances between the ten coordinates using the brute-force algorithm.

The Python libraries used in this project:

1. itertools: This library allows me to perform various iteration and combination operations when working with data. It enables me to create iterators, combine data, filter duplicates, and more.

2. math: I use this library to perform mathematical operations. It includes functions for trigonometric calculations, logarithms, exponentiation, factorial calculations, and other mathematical operations.

3. random: I rely on this library to generate random numbers and make random selections. It helps me with tasks such as generating random numbers, creating random sequences, and making random item selections.

4. folium: This library is helpful when I need to create interactive maps. Built on Leaflet.js, Folium allows me to visualize map data using Python. It provides functions to manipulate various map elements like data layers, markers, lines, and shapes.

5. pandas: I utilize this library for data analysis and manipulation. Pandas enables me to store and process data in tabular structures called DataFrames. It includes a wide range of functions for reading data, filtering, merging, grouping, summarizing, and more.


The steps I took while writing the code and their explanations are as follows:


1. I imported the required libraries: I started by importing the necessary libraries, including itertools, math, random, folium, and pandas.

2. I defined the City class: I defined a class called City to represent a city with x and y coordinates. It has methods to calculate the distance between cities and a custom representation method to print the city's coordinates.

3. I defined the generate_cities() function: I created a function called generate_cities() that takes a DataFrame of coordinates as input and generates a list of City objects based on the latitude and longitude values in the DataFrame.

4. I defined the read_cities() function: Similar to the generate_cities() function, I implemented a function called read_cities() that takes a DataFrame of coordinates and creates a list of City objects.

5. I defined the path_cost() function: I implemented a function called path_cost() that calculates the total distance/cost of a given route by iterating over the cities in the route and summing up the distances between consecutive cities.

6. I defined the visualize_tsp() function: I created a function called visualize_tsp() that generates an interactive map using the Folium library. It takes a title and a list of cities as input, converts the city coordinates to a format suitable for Folium, creates a map centered on Turkey, adds a polyline connecting the cities, and places markers at each city location. Finally, it saves the map as an HTML file.

7. I defined the BruteForce class: I created a class called BruteForce that represents the brute force approach for solving the Traveling Salesman Problem (TSP). It takes a list of cities as input, and the run() method finds the optimal solution by generating all possible permutations of the cities and selecting the one with the minimum path cost.

8. I read the CSV file: I used the pandas library to read the CSV file containing earthquake coordinates. I selected the 'Latitude' and 'Longitude' columns from the DataFrame.

9. I generated a list of cities: I called the generate_cities() function to create a list of City objects based on the latitude and longitude coordinates from the CSV file.

10. I ran the brute force algorithm: I created an instance of the BruteForce class with the city list and called the run() method to find the optimal TSP solution.

11. I visualized the TSP solution: I called the visualize_tsp() function to generate an interactive map, showing the TSP solution found by the brute force algorithm. The map was saved as an HTML file.

These steps outline the process of the code, from importing the required libraries to visualizing the TSP solution using an interactive map.
