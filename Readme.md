# Proposal for Semester Project

**Patterns & Trends in Environmental Data / Computational Movement
Analysis Geo 880**

| Semester:      | FS23                                                     |
|:---------------|:---------------------------------------------------------|  
| **Data:**      | Movement data of two college students                    |
| **Title:**     | Understanding movement patterns of different travel modes|
| **Student 1:** | Yelu He                                                  |
| **Student 2:** | Martine Besse                                            |

## Abstract 
<!-- (50-60 words) -->
Our project aims to better understand movement pattern of different travel modes. By first decribing and summarizing characteristics of trajectory data, an characteristics dataset with label of different travel modes will be generated. Combined with environmental data such as traffic network, an identification model will be built. Last, the model will be assessed and evaluated.


<!-- long version -->
Our project aims at defining, describing and identifying movement patterns for different travel modes. Movement data has been collected over a period of approximately two months and a various range of travel modes have been recorded: train, tram, bus, car, walking, cycling, running, kick scooter, ski, ski-lift and boat. A labeled dataset with travel modes will be extracted from the collected raw data by cleaning, filtering and segmentation.  
The movement pattern for each travel mode will first be characterized by the following metrics: speed (acceleration, deceleration), sinuosity (angle, direction), and environmental factors related to the studied travel mode: railway tracks, tram lines, road network, walking path, slope, etc. Furthermore, it will be decribed and summarized with the knowledge of previous studies on travel modes identification from GPS tracks.
In a second step, the suitability of these characteristics for identifying travel modes will be studied. Limitation of data and methods will also be discussed. For example are the difference of the aforementioned chracteristics significant between two travel modes, and does our recorded data contain enough information.   
Based on the answer, a model will then be attempted to build. We will apply it to collected data to detect different travel modes. The results of the identification will finally be evaluated with the labeled dataset.

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
2. (Option) Transport network(railway/street network, cycling/walking/skiing paths), tram/bus/train/boats stops and stations, and tram/bus/train/boats time schedules.
3. (Option) Environment and obstacles, such as lake, buildings, rivers, and terrain elevation.
#### Data source
1. Volunteered movement data of two college students
2. Open data from SwissTopo


## Analytical concepts
<!-- Which analytical concepts will you use? What conceptual movement spaces and respective modelling approaches of trajectories will you be using? What additional spatial analysis methods will you be using? -->

#### Conceptual movement spaces and respective modelling approaches
The data collected is spatio-temporal. Depending on the travel mode studied, the conceptual movement space will be different.

Most of the transportation mode evolve in a discrete network movement space, and are constrained: cars for example are bound to road, trams to tracks, etc. 
But others could be represented as continuous Euclidean space and unconstrained or limited, such as navigating, walking, running or skiing. 

All the travel modes can be represented with the time as the third dimension (2D + T) and are of active forms.

As for additional spatial analysis methods, classification algorithms for RQ3 will be explored.

## R concepts
<!-- Which R concepts, functions, packages will you mainly use. What additional spatial analysis methods will you be using? -->
We will use tidyverse for data processing (filter, segmentize, etc.), sf for spatial objects, and ggplot2 for visualization. It might be interesting to plot a background map too, so we might use other libraries (such as tmap or leaflet).

Some other useful packages could be: caret, cluster and clusterR, to conduct supervised or unsupervised machine learning to try and test the identification model.

## Risk analysis
<!-- What could be the biggest challenges/problems you might face? What is your plan B? -->
For certain travel modes, we might not have enough data to do an accurate analysis and then test the model (for example boat or skiing). A solution could be to ask for labeled data from our fellow colleagues for the missing travel modes movements.

## Questions? 
<!-- Which questions would you like to discuss at the coaching session? -->
- Do these goals seem feasible based on the knowledge acquired in class, and in the timeframe of the remaining weeks of work?
- Could we attempt to use machine learning methods to identify travel modes as comparison to our identification models?

## Literature References 
- Zeng, J., Yu, Y., Chen, Y., Yang, D., Zhang, L., & Wang, D. (2023). Trajectory-as-a-Sequence: A novel travel mode identification framework. Transportation Research Part C: Emerging Technologies, 146, 103957. doi:10.1016/j.trc.2022.103957
- Sadeghian, P., Zhao, X., Golshan, A., & Håkansson, J. (2022). A stepwise methodology for transport mode detection in GPS tracking data. Travel Behaviour and Society, 26, 159–167. doi:10.1016/j.tbs.2021.10.004
