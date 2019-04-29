# First_Version--Individual-Project
This is the first version of the MSIS 2629 Data Visualization individual project for spring 2019



## Background about the dataset
The dataset is taken from [Speed_Camera_Violations-Chicago Data Portal](https://data.cityofchicago.org/Transportation/Speed-Camera-Violations/hhkd-xvj4) and each record represents the number of violations occurred on a specific day taken by a specific speed camera, starting from July 2014 to April 2019. 

The mayor of Chicago, Rahm Emanuel, has been extremely proactive in the automated speed enforcement in parks and schools to protect the kids. Every year new cameras are going live in the summer, and as of today there are 162 cameras live trying to catch people speeding in these safety areas.

I have also used the dataset on [speed camera locations-Chicago Data Portal](https://data.cityofchicago.org/Transportation/Speed-Camera-Locations/4i42-qv3h), which includes the date of which camera went live, which I later used to develop a visualization/finding.

## Visualization #1 & Finding
Through the previous data exploration process, I was able to find that there's a decreasing trend from 2014 to 2019, and I decided to take that step further, and used the month function in tableau to develop this line chart below, where on the y axis it's the sum of violations, and the x axis is continous month from 2014 to 2019.
![visualization #1](https://github.com/jacksonh2/First_Version--Individual-Project/blob/master/Monthly%20sum%20violation%20trend.png)

I also decided to add a linear trend line to really reflect that decreasing trend in monthly violations, which can be credited towards the automated speed enforcement (ASE) program, and it demonstrates that the program is effective, and the mayor should definitely continue enforcing program.

In terms of data warranging, I decide to take out the first month and the last month data, to avoid any incomplete data in those two month that could have had an effect on the overall trend. 

An improvement to this graph is that next time I can perhaps smooth out the lines to get a better visual, and I can also add a forecast model to show the predicted values for the coming years, and these new additions can be benefitical to the mayor in deciding how much of the city's budget should be allocated to the ASE program.

## Visualization #2 & Finding
After seeing that the program is slowing the drivers down in the safety zones across the city, the next goal should be to tackle specific problem areas that are causing the most average violations. Since different cameras went live on different times, I created a new calculated field, which uses the sum of violations for that camera, divide by the total number of month between today (april 2019) and the first month that a violation recorded for that particular camera, to get a true average number of violations per camera. Then I ranked it base on this criteria and selected the top 10 cameras that have the highest true average. 

![visualization #2](https://github.com/jacksonh2/First_Version--Individual-Project/blob/master/monthly%20average%20top%2010%20cameras.png)

From this visualization we can see that the distribution of the top 10 cameras is pretty centered in the northern part of Chicago. A suggestion to the mayor is to perhaps either install more cameras in the northern region of Chicago or to increase the fines of speeding in the northern part to further punish this speeding behavior.

A map would be the best for this visualization because this way I would be able to showcase where these cameras that catch the highest average violations are located and can group them by region, and thus give better suggestions to the mayors as where to tackle next.

An interesting thought that came up when I was crafting this visualization is that, in order to improve on this graph, next time I can find some datasets on the wealth/income distributions throughout Chicago, and perhaps I can add those attributes to the current map visualization, and we would be able to see that whether the most troublesome areas of speed violations are located in more wealthy areas or the less affluent areas. Adding this aspect to the current visualization will add depth to it, and that aspect can later be used by the mayor to decide on how many cameras to install/how much raise in the fine.

## Visualization #3 & Finding
For the third finding, I decided to merge the speed camera location dataset into the speed violation dataset, and first off I found that most of the speed camera went live in 2013-2015, and a few were added in 2018, but there weren't any cameras that went live in 2016 or 2017. Therefore I graphed the sum of violations grouped by year, against the number of cameras that were live for 2015-2018. 

![visualization #3](https://github.com/jacksonh2/First_Version--Individual-Project/blob/master/count%20of%20camera%20vs%20total%20violation.png)

From the visualization, we can see that in 2016 and 2017 where there weren't any new cameras that went live, the sum of violations experienced steady decrease, but in 2018 when there are more cameras that went live, the slope actually becomes flatter, which makes sense because more cameras means there will be more violations that will get captured by these new cameras, and the effect of these new cameras will take some time before it appear.

Therefore, I would suggest to continuously increase the number of cameras throughout the future years to further strengthen this program, as the number of violations should decrease more rapidly with more cameras in place (after the initial upward sloping effect of more cameras = more violations).




## Dashboard
![dashboard](https://github.com/jacksonh2/First_Version--Individual-Project/blob/master/dashboard.png)



[tableau public-visualizations & dashboard](https://public.tableau.com/profile/jackson.hu8026#!/vizhome/Visualization1-individualproject/Dashboard1?publish=yes)


## Roadmap
A lot more could have been done to improve the visualizations that I have created so far. In reading the ASE program descriptions and doing research on the feedbacks on the ASE program, I found that there are some controversies about the program, suggesting that the cameras are operating at unauthorized hours and issuing tickets; for instance, the school's safety zone cameras should only opeate from monday to friday, but there have been various incidents where people were caught by the camera on the weekends. Though I attended to create a visualization on this matter, I wasn't able to finalize it because it was extremely hard to determine which cameras are in the school zone (monday-friday) and which ones are in the park zone(operates 7 days a week). I was able to find something like [list of safetyzone](https://www.chicago.gov/content/dam/city/depts/cdot/CSZ/ChildrensSafetyZoneList.pdf)but the address of the safety zone didn't exactly match the address of the cameras, thus making it difficult to merge the two datasets. For the second version, I would love to incorporate this aspect of the matter into my second visualization, to see whether these cameras with the highest average violations are located in school or park zone, and this can definitely advocate my analysis.
