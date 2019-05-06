# Final_Version--Individual-Project
This is the Final version of the MSIS 2629 Data Visualization individual project for spring 2019, if you want to see the first_version, please refer to [first_version](https://github.com/jacksonh2/Individual-Project-Chicago_Speed_Violation/blob/master/First_Version.md)


## Background about the dataset
The dataset is taken from [Speed_Camera_Violations-Chicago Data Portal](https://data.cityofchicago.org/Transportation/Speed-Camera-Violations/hhkd-xvj4) and each record represents the number of violations occurred on a specific day taken by a specific speed camera, starting from July 2014 to April 2019. The mayor of Chicago, Rahm Emanuel, has been extremely proactive in the automated speed enforcement in parks and schools to protect the kids. 

The Automated Speed Enforcement program's safe zone is described as below:

> The safety zone is desingated as 1/8th of a mile boundary around any Chicago parks or schools. The City ordinance establishing the Children’s Safety Zone program substantially narrows the hours and locations of automated speed enforcement that are allowed under state law

The cameras' operation hours as well as the speed limit during those hours are:

> The enforcement hours will be limited from 7 a.m. to 7 p.m. in safety zones around schools on chool days (Monday through Friday)

> 7 a.m. to 4 p.m.: 20 miles per hour (mph) speed limit when children are present; and the posted speed limit when no children are present

> 7 a.m. to 7 p.m.: The posted speed limit
> The enforcement hours around parks will be limited to only those hours parks are open (typically *6 a.m. to 11 p.m., 7 days a week) with a 30 mph speed limit

The violation fine regulation is listed below:

> Only warnings will be issued for the first 30 days after cameras are newly-established in a safety zone
The first time a vehicle owner is eligible to receive an actual ticket, they will instead receive a warning notice
Fines for violations are $35 for vehicles traveling 6-10 mph over the posted speed limit while in a safety zone, and $100 for vehicles traveling 11 or more mph over the posted speed limit.


In addition to the dataset with the violations, I have also used the dataset on [speed camera locations-Chicago Data Portal](https://data.cityofchicago.org/Transportation/Speed-Camera-Locations/4i42-qv3h), which includes the date of which camera went live, which I later used to develop a visualization/finding.

For more information about the program and about speed camera violations, please refer to [city of chicago - ASE](https://www.chicago.gov/city/en/depts/cdot/supp_info/children_s_safetyzoneporgramautomaticspeedenforcement.html) and [city of chicago - ASE FAQ](https://www.chicago.gov/city/en/depts/cdot/supp_info/children_s_safetyzoneporgramautomaticspeedenforcement/automated_speed_enforcementfrequentlyaskedquestions.html).

## Visualization #1 & Finding
Through the previous data exploration process, I was able to find that there's a decreasing trend from 2014 to 2019, and I decided to take that step further, and used the month function in tableau to develop this line chart below, where on the y axis it's the moving average of the sum of the violations, and the x axis is continous month from 2014 to 2019.
![visualization #1](https://github.com/jacksonh2/Individual-Project-Chicago_Speed_Violation/blob/master/Monthly%20sum%20violation-Final.png)

The linear trend line is statistically significant, and thus truly reflects that decreasing trend in monthly violations, which can be credited towards the automated speed enforcement (ASE) program, and it demonstrates that the program is effective, and the mayor should definitely continue enforcing program. 

In addition to the downward trend, I also found that seasonality trend of violation spikes and drops is another interesting aspect found with this visualization. We can see that in February of every year, the number of violations would reach the lowest point of that given year, where May-July tend to have the highes number of violations in that given year, and there's also an upward trend towards the end of the year near November. The mayor should definitely look into the reasons behind those seasonality trend, whether it's due to school breaks or driver behavior, and can target those months specifically.


### Making-of and improvement
The line chart was chosen in this case because I wanted to track the changes in number of violations through the years of 2014-2019, and line graph is better than other chart types in this case. In terms of data warranging, I decide to take out the last month data, to avoid any incomplete data in the end month that could have had an effect on the overall trend. In the first version of this visualization, I chose the sum of violations as the variable, and in order to improve the visual, I decided to apply moving average to the sum function to smooth the lines. Furthermore, I have also removed the gridlines, as they were unnecessary and redundant for the readers, because the after smoothing the line, the data points are more spread out and can be easily interpreted even without the gridline, and having the grid line there would only add complexity to the graph. I also added a few constant lines to highlight the month that had the lowest number of violations from 2015-2018, to highlight that seasonality effect. I am more satisfied with the revised version of the visualization as these changes make the downward trend more clear, as well as we can see that number of violations in each month is lower in comparison to the same month in the previous year.

## Visualization #2 & Finding
After seeing that the program is slowing the drivers down in the safety zones across the city, the next goal should be to tackle specific problem areas that are causing the most average violations. Since different cameras went live on different times, I created a new calculated field, which uses the sum of violations for that camera, divide by the total number of month between today (april 2019) and the first month that a violation recorded for that particular camera, to get a true average number of violations per camera. Then I ranked it base on this criteria and selected the top 10 cameras that have the highest true average. 

![visualization #2](https://github.com/jacksonh2/Individual-Project-Chicago_Speed_Violation/blob/master/top%2010%20monthly%20average%20camera%20location-Final.png)

From this visualization we can see that the distribution of the top 10 cameras is pretty centered in the northern part of Chicago. A suggestion to the mayor is to perhaps either install more cameras in the northern region of Chicago and put up more speed indicator signs. Also, as I added the household income distribution to the visualization, we can see that the most troublesome cameras are in the more affluent neighborhood in Chicago. As the new finding suggests, increasing the fines of speeding in the northern part can be a good solution to further punish this speeding behavior.  Furthermore, we can see that the majority of the top 10 cameras located near highways. Last but not least, the mayor can further lower the posted speed limit near highways and even add speed bumps to further ensure the safety of the children.


### Making-of and improvement
A map would be the best for this visualization because this way I would be able to showcase where these cameras that catch the highest average violations are located and can group them by region, and thus give better suggestions to the mayors as where to tackle next. In order to improve from the first version of this visualization, I was originally thinking merging a wealth distribution dataset into the speed camera violation dataset to add that layer of wealth distribution to the map, however, after doing some research I found that there's actually a built-in feature in tableau that can do this. Using the features in the map layers, I was able to add the household income distribution, as well as streets and highways to further enrich the map and come up with more insights to better improve the ASE program. Before adding these map features, the map looked boring and didn't have much information, but now we can see just exactly where these cameras are located (next to which street/highway) and how is the neighborhood and how that might impact the driver behavior.

## Visualization #3 & Finding
For the third finding, I decided to merge the speed camera location dataset into the speed violation dataset, and first off I found that most of the speed camera went live in 2013-2015, and a few were added in 2018, but there weren't any cameras that went live in 2016 or 2017. Therefore I graphed the average number of violations grouped by year, against the number of cameras that were live for 2014-2018. 

![visualization #3](https://github.com/jacksonh2/Individual-Project-Chicago_Speed_Violation/blob/master/count%20of%20camera%20vs%20avg%20violation-Final.png)

From the visualization, we can see that from 2014-2015, 7 new cameras are added and the average number of violations decreased at a rather steep rate. From 2015-2017 there weren't any new cameras that went live, the decreasing rate of the average number of violations became flatter. From 2017 to 2018, 11 new cameras went live. Though we didn't see a significant decrese in that year(2017-2018), the forecast suggests that even if the camera count remains at 155 through the year of 2019, we would see a steeper decrease in average number of violations through 2019. 

Therefore, I would suggest to continuously increase the number of cameras throughout the future years to further strengthen this program (within the budget), as the number of violations should decrease more rapidly with more cameras in place (after the initial upward sloping effect of more cameras = more violations).

### Making-of and Improvement
Again, the line graph was the best for this visualization because I wanted to show the changes in number of cameras and average number of violations together from 2014-2019. Previously I have used the sum of violations for each year, and the graph didn't look too satisfying because the lines were very close to each other and was hard to interpret. The trendline was also not very helpful so I have removed it from the final version of the visualization. To further strengthen my point, I also decided to include a forecast, to better illustrate my point.  




## Dashboard
![dashboard](https://github.com/jacksonh2/Individual-Project-Chicago_Speed_Violation/blob/master/dashboard-Final.png)
In terms of the dashboard, I added a few interactive features, such as a slider filter to visualization #1, map zoom-in & out as well as a search bar to visualzation #2, and last but not least a camera drop down filter to visualization #3. 



[tableau public-visualizations & dashboard](https://public.tableau.com/profile/jackson.hu8026#!/vizhome/Visualization1-individualproject/ChicagoSpeedCameraViolationDashboard?publish=yes)




## References
https://www.chicago.gov/city/en/depts/cdot/supp_info/children_s_safetyzoneporgramautomaticspeedenforcement.html
https://www.chicagotribune.com/news/watchdog/ct-speed-camera-ticket-rules-met-20151118-story.html
https://data.cityofchicago.org/Transportation/Speed-Camera-Violations/hhkd-xvj4
https://data.cityofchicago.org/Transportation/Speed-Camera-Locations/4i42-qv3h
https://www.chicagotribune.com/news/watchdog/ct-speed-camera-bad-tickets-met-20151117-story.html
https://www.chicago.gov/content/dam/city/depts/cdot/CSZ/ChildrensSafetyZoneList.pdf



