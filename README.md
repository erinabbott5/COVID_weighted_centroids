# COVID_weighted_centroids


Current version last edited on 08/09/2020

T?his is Jeff saying hi

## Authorship 

Author: Erin Abbott

Research Concept and Design: Marcia Castro, PhD.

Project Management and quality assurance: Jeff Blossom, MA. 


## Purpose
This script was developed to investigate movement of the COVID-19 case-weighted centroid in Brazil throughout the course of the pandemic. The national centroid is calculated by taking the geographic centroid of each municipality as a set of points, finding the national geographic centroid from those points, and then weighting the position of the national centroid by the case count of COVID-19 in each municipality.


### Outcome
With this script, we were able to plot the path of the COVID-19 weighted centroids with line strings and a centroid at the location of the final week's centroid. We also include a choropleth map for the case count in the last available epidemiological week using a logarithmic classification due to the wide range of case counts in the different municipalities. We also wanted a table exported containing lengths of each line connecting the centroids, the length between each centroid and the capital city, and the direction of the line. These were included to answer specific research questions. 

Example output: 

![Alt text](/Users/erin/Desktop/Harvard_NSF_REU/Brazil_COVID/github/Nation_all_weeks_animated.gif?raw=true "Title")

## Guidance
This script may be adapated to different countries by an individual comfortable with R scripting. This process will work with any sub-unit of a nation, whether it be regions, states, counties, municpalities,or census tracts, as long as there are smaller units which make up a larger unit for which you want to find the weighted centroid for. In order to adapt this script, we recommend the following files/formats and potential code changes: 

Input files: 
* Sub-unit boundary shapefile: including - 
  * Unique identifier for the sub-unit: Municipality ID (ibge_code)
  * Geographic boundaries for the shapefiles 
  * example: 
  
    < insert image of municipalities shapefile >
    
* COVID-19 cases CSV: including - 
  * Sub-unit unique identifier: Municipality ID (ibge_code)
  * Week number: (epidemiological_week)
  * Date number: (date)
  * COVID-19 case count: (daily.cases)
  * example:
  
    < insert image of cases csv table here >

* Optional: 
  * Another unit boundary shapefile: we also have a state boundaries shapefile which is only used in the visualization
  * Capital location shapefile: included to calculate the distance of each weekly weighted centroid to the capital city
    
Code changes: 
* File paths: change line numbers 22, 29, 37, 251
* Numbers for start and end week: change line number 104, 105, 133, 222, 244, 251, 281, 286
    
Visualizations/ plotting:
* Logarithmic classification: can be altered in the map creation in line number 248
* Map title, labels, etc: change in line number 248










