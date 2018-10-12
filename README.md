# codefundo

# Project Idea
The idea is to make a Crisis Response App that will use the details obtained through geospatial information and crowdsourcing by rescuers and the victims(if possible) to find out the best route between rescue camps and the affected site. The best route is defined as the route which minimizes the danger of being affected by the calamity throughout the route. This app will help rescuers at different rescue stations and victims to contribute for more organized and effective search operations.

# Motivation
*Some case study here which tells us why this idea is necessary and effective*
In June 2013, multi cloudbursts centered on the North Indian state Uttarakhand, caused devastating floods and landslides, creating the country’s worst disaster since the 2004 tsunami. A multi-day downpour brought early and torrential rainfall to much of the mountainous region, triggering the collapse of a glacial lake dam and causing heavy flooding and landslides that claimed upwards of 4,000 lives and affected nearly a million people. Destruction of bridges and roads left about 300,000 pilgrims and tourists trapped in the valleys. With such vast destruction transportation of relief material to locals in flooded villages and rescue of people trapped in highly affected places posed a fresh challenge to authorities in Uttarakhand. Supplying foodgrains to affected villages was proving to be an onerous task for the administration as trucks loaded with relief material are stuck at different places in the city in the absence of roads which suffered extensive damage in the floods. To make the disaster management more efficent we came up with an idea of Crisis Response App. It will help in proper routing for transportation.


# Working
*Approximate process flow , Approximate algorithm basics*
The algorithm uses geostatical information and crowd responces as inputs. We are initially given the locations of the releif camps.
Tracking the crowd's location using the telecommunication network is done at regular interval. These locations are then mapped and disaster affected hotspots are detected. The map is now seen as a Graph with set of Nodes and Edges(with weights). We identify the clusters of the affected people and treat them as nodes. We treat the path as an edge between nodes and other locations of the map. We take the geostatical and crowd(which involves both rescuers and victims) responces to detect the affected paths. This information will be updated on the server regularly to maintain the presion. The edges corresponding to affected paths are given higher weigths. The relief camp are seen as final destination. The algorithm then finds the shortest path with minimum weight from the nodes to the final destination. This way more affected paths from nodes to releif camp are eliminated due to higher weights.
The best path will be provided to the rescue team so that it is easy for them to reach the victims faster.
