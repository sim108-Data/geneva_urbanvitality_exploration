# Exploring "Urban intensity/vitality" with Open Data, and 15-minute action space

This repository contains the following main folders and files :
* **Data** : regroups all the Data used in this project 

* **Figures**: regroups all outputs of the plots used in the code. (**png** : access to all plots / **map_html**: acces to all the interactive map)

* **1.Analysis_OpenData.ipynb**: analysis of Urbain Vitality and 15-minute action space on a jupyter notebook

* **2.Analysis_demand_Domotopie.ipynb**: analysis of the Domotopie dataset in order to observe how Geneva citizen are moving (demand) and see if it is consistent and what was found in the previous analysis

* **Graphs**: folder containing all the graphs (bike,walk and all type) for each subsectors saved from network.ipynb. It is used to increase compute the security factor.

* **network.ipynb**: download all graph from osmnx library and save it into graphs 

## Data
For the first part of the project, two type of Open Data are used:
* **1. [Open Street Map Data (OSM)](https://github.com/gboeing/osmnx)**: Sets of valuable geospatial components such a the geolocation of
different types of icons, routes or building footprints. Those components can be extracted from the
OpenStreetMap Overpass API. This project use the python library ”OSMnx”  in order to access to the
API. Note that this sets is generated by the citizen themselves. Hence, the accuracy of the location point
may be wrong. Nevetheless, a method to check the feasibility of Osm points is presented below.

* **2. [General Transit Feed specification (GTFS)](https://opentransportdata.swiss/en/group)** : Sets of transit data published by public transit agencies as a accumulated database in GTFS format ”. It provides valuable geographical information, such as locations of stops and number of transfers. Due to the origin of the data, a stricter control than for Osm datasets is assumed to have been performed before publication.

* **3. Domotopie dataset**: This dataset provides for 2'283 subject the five places where most of their time have
been spend. All mode of transport to make those trips are also provided. This is a private dataset collected using a survey. A sample of the question used can be found in the report.

* **Data**: regroup others datasets added or created during the study 

## Getting Started

First, you will need to have " git " install on your computer to be able to clone the repository on your computer. You will also need to have python and jupyter notebook installed. If this is not the case you can download it from here: Python: https://www.python.org/downloads/  and for jupyter notebook the easiest is to download Anaconda: https://docs.anaconda.com/anaconda/install/index.html and open it from there.

## Dependencies and Installing

The code is using some external libraries: "Numpy", "Pandas" and "Geopandas" to analyze data, "Matplotlib" and "Seaborn" to visualize the output of the analysis, ["Keplergl"](https://anaconda.org/conda-forge/keplergl) to visualise the maps, ["OSMnx"](https://github.com/gboeing/osmnx)to analyse Open street map data , ["gtfs_functions"](https://github.com/Bondify/gtfs_functions) in order to deal with GTFS datas, "networkx" to import the networks length in the calculation of the security factor.

If you are completely new to those libraries. The easiest way is to use "conda" command in your terminal, once you have downloaded Anaconda. Those can also be downloaded in some other way. More information is provided on their websites

If you are using anaconda, you can simply  copy those code lines on the same order into your terminal.

* Osmnx :
```
conda config --prepend channels conda-forge
conda create -n ox --strict-channel-priority osmnx
```
* Enter the environment  :
```
conda activate ox
```
* pandas : 
```
conda install -c anaconda pandas
```
* matplotlib :

```
conda install matplotlib
```
* numpy : 
```
conda install -c anaconda numpy
```
* geopandas
```
conda install -c conda-forge geopandas
```
* Kepler
```
conda install -c conda-forge keplergl
```

* Networkx
```
conda install -c anaconda networkx
```

* GTFS Function
```
pip install gtfs-functions
```

### Executing program

To execute the program you need to follow the steps described below:
* Clone the repository on your computer
* Get the Python libraries needed
* Enter in the repository with this command (Windows) or equivalent code line for Mac and Linux
```
cd geneva_urbanvitality_exploration
```
* Run jupyter lab as follow in the command line:
```
jupyter lab 
```

* Another way to open the repository that you have cloned is to open Anaconda Navigator and open it from there.

## Authors

Simon Dayer

## License
Copyright © 2021 Simon Dayer. All rights reserved.
