![Final_presenattion_Group_3](https://user-images.githubusercontent.com/97453175/175821940-4e60d45d-2a73-4ef0-b586-d2cf20b69967.jpg)


# Urban-Artefacts
Urban-Artefacts AI Studio

The repository is for our final studio project called "Urban Artefacts", created for the Artificial Intelligence seminar at the IAAC for the masters in advanced computation in architecture course. The repository contains steps and guide for recreating the project in other cities.  Our project presents itself as a response to a very simple question.  How can we make better use of our public pedestrian space and improve the quality of the outdoors in Vienna by finding and filling these voids with the necessary and required amenities?  Our proposed solution will be to augment and optimize the streets by planting the necessary amenities where required; A bench, a vending machine, bicycle parking and so on.  All of these will be calculated depending on the existent conditions, then acted upon for optimisation.

STEPS
1.	Get data about cities amenities, land-use and demographics
Data about the city can be gathered from open sources such as Open Street Maps and government websites like in the case of this project.  Data could further be collected about amenities for example through manual collection or through image segmentation of street images to collect counts of certain amenities.

2.	Tiling the city and counting amenities
The selected city will then be tiled according to an official tiling system or by a defined squared area.  Within these grids the amenities, land-uses and demographics are counted and then analysed as in the notebook provided.

3.	Clustering the city tiles to zones
Using the the K-MEANS algorithm provided in the notebook, cluster the tiles based on population density, landuse and amenities.  Through manual analysis of the K-MEANS clusters visually through charts and other evaluation methods such as the K-MEANS elbow graph determine the ideal number of clusters to describe the city.  The amenities then are averaged based on which cluster they land.  

4.	Calculating excess or lack of amenities
Create all the data frames as shown in the notebook, and perform the same basic calculations to determine the distribution of amenities in the city.   By taking the average count for all of the tiles within the  created clusters and deducting them from the currently existing amenity tile count  depending on which cluster they are located, we are presented with a number showing how far from the cluster average the current count is.  This number does not give an absolute truth but more of an indication of what the amenity situation is within each select tile.   These numbers could be further augmented in the future though district policies such as targets in certain areas to increase recycling.

5.	Identify the voids within the tiles and recommendations
The final step then involves overlaying the voids collected from the early stages with the tiles holding the new recommendation values.  If the void intersects with the tile, then the amenity differences are shown within that void.  Through this method each void will receive a list of numbers for each of the amenities. Using the script in the notebooks, these values can be exported to a html file for an interactive web interface.


