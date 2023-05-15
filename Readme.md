# Proposal for Semester Project

**Patterns & Trends in Environmental Data / Computational Movement
Analysis Geo 880**

| Semester:      | FS23                                     |
|:---------------|:---------------------------------------- |
| **Data:**      | Movement data of two college students    |
| **Title:**     | Understanding movement patterns of different travel modes    |
| **Student 1:** | Yelu He                                  |
| **Student 2:** | Martine Besse                            |

## Abstract 
<!-- (50-60 words) -->

Our project aims at defining, describing and identifying movement patterns for different travel modes. Movement data has been collected over a period of approximately two months and a various range of travel modes movements have been recorded: train, tram, bus, car, walking, cycling, running, kick scooter, ski, ski-lift and boat. A labeled dataset will be extracted from the collected data by filtering and segmentizing.  
The movement pattern for each travel mode will first be characterized by looking at the metrics: speed (acceleration, deceleration), sinuosity (angle, direction), and the specific environment bound to the studied travel mode: tracks, roads, slope. 
In a second step, the suitability of these characteristics for identifying travel modes will be studied. For example are characteristics of trams different enough of bus, and does our recorded data contain enough information.   
Based on the answer, a model will then attempted to be built, and applied to the collected data to detect the travel modes. The results of the identification will finally be evaluated thanks to the labeled dataset.

## Research Questions
1. Do the characteristics of movement trajectories differ beetween different travel modes?
2. Could the characteristics be used to identify travel mode?
3. How to identify different travel modes with movement trajectories? Could a identification model be built?
4. How accurate and efficient could different travel modes be identified based on the aforementioned identification model?




## Results / products
1. Characteristics summary of movement trajectories of different travel modes.
2. An identification model for travel mode based on movement tractory data.
3. Assessment of the identification model.


## Data
<!-- What data will you use? Will you require additional context data? Where do you get this data from? Do you already have all the data? -->
#### Data used 
1. Movement data collected with POSMO (mobile tracking app) and GPS trackers (external device).
2. (Option)Transport network(railway/street network, cycling/walking/skiing paths), tram/bus/train/boats stops and stations, and tram/bus/train/boats time schedules.
3. (Option) Environment and obstacles, such as lake, buildings, rivers, and terrain elevation.
#### Data source
1. Volunteered movement data of two college students
2. Open data from SwissTopo


## Analytical concepts
<!-- Which analytical concepts will you use? What conceptual movement spaces and respective modelling approaches of trajectories will you be using? What additional spatial analysis methods will you be using? -->

#### Conceptual movement spaces and respective modelling approaches
The data collected is spatio-temporal. Depending of the travel mode studied, the conceptual movement space will be different.
Most of the transportation mode evolve in a discrete network movement space, and are constrained: cars for example are bound to road, trams to tracks, etc. 
But others could be represented as continuous Euclidean space and unconstrained or limited, such as navigating, walking or skiing. 

All the travel modes can be represented with the time as the third dimension (2D + T) and are of active forms.

As for additional spatial analysis methods, classification algorithms for RQ3 will be explored.

## R concepts
<!-- Which R concepts, functions, packages will you mainly use. What additional spatial analysis methods will you be using? -->
We will use tidyverse for data handling (filter, segmentize, etc.), sf for spatial objects, and ggplot2 for visualizing. It might be interesting to plot a background map too, so we might use other libraries (such as tmap or leaflet).

Some other useful packages could be: caret, cluster and clusterR, to conduct supervised or unsupervised machine learning to try and test the identification model.

## Risk analysis
<!-- What could be the biggest challenges/problems you might face? What is your plan B? -->
For certain travel modes, we might not have enough data to do an accurate analysis and then test the model (for example boat or skiing). A solution could be to ask for labeled data from our fellow colleagues for the missing travel modes movements.

## Questions? 
<!-- Which questions would you like to discuss at the coaching session? -->
- Do these goals seem feasible based on the knowledge acquired in class, and in the timeframe of the remaining weeks of work?
