# First_Version--Individual-Project
This is the first version of the MSIS 2629 Data Visualization individual project for spring 2019



## Background about the dataset
The dataset is taken from [Chicago Data Protal](https://data.cityofchicago.org/Transportation/Speed-Camera-Violations/hhkd-xvj4) and each record represents the number of violations occurred on a specific day taken by a specific speed camera, starting from July 2014 to April 2019. 

The mayor of Chicago, Rahm Emanuel, has been extremely proactive in the automated speed enforcement in parks and schools to "save the kids". Every year new cameras are going live in the summer, and as of today there are 162 cameras live trying to catch people speeding in these safety areas.

## Visualization #1
Even though there are a lot of controversies about these cameras are simply issuing tickets to people to raise revenue for the government, nevertheless the following visualization shows that violations that are caught in camera is decreasing every year.

![visualization #1](https://github.com/jacksonh2/First_Version--Individual-Project/blob/master/Monthly%20sum%20violation%20trend.png)

Thus it means that the program is effective, and the mayor should definitely continue the program.

## Visualization #2
After seeing that the program is slowing the drivers down in the safety zones across the city, the next goal should be to tackle specific problem areas that are causing the most average violations. Since different cameras went live on different times, I created a new calculated field, which uses the sum of violations for that camera, divide by the total number of month between today (april 2019) and the first month that a violation recorded for that particular camera, to get a true average number of violations per camera. Then I ranked it base on this criteria and selected the top 10 cameras that have the highest true average. 

![visualization #2](https://github.com/jacksonh2/First_Version--Individual-Project/blob/master/monthly%20average%20top%2010%20cameras.png)

From this visualization we can see that the distribution of the top 10 cameras is pretty centered in the northern part of Chicago. A suggestion to the mayor is to perhaps either install more cameras in the northern region of Chicago or to increase the fines of speeding in the northern part to further punish this speeding behavior.

## Visualization #3
For the third finding, I decided to merge the speed camera location dataset into the speed violation dataset, and first off I found that most of the speed camera went live in 2013-2015, and a few were added in 2018, but there weren't any cameras that went live in 2016 or 2017. Therefore I graphed the sum of violations grouped by year, against the number of cameras that were live for 2015-2018. 

![visualization #3](https://github.com/jacksonh2/First_Version--Individual-Project/blob/master/count%20of%20camera%20vs%20total%20violation.png)
From the visualization, we can see that in 2016 and 2017 where there weren't any new cameras that went live, the sum of violations experienced steady decrease, but in 2018 when there are more cameras that went live, the slope actually becomes flatter, which makes sense because more cameras means there will be more violations that will get captured by these new cameras, and the effect of these new cameras will take some time before it appear.

Therefore, I would suggest to continuously increase the number of cameras throughout the future years to further strengthen this program, as the number of violations should decrease more rapidly with more cameras in place (after the initial upward sloping effect of more cameras = more violations).



## Visualization Design Process


[tableau public-visualizations & dashboard](https://public.tableau.com/profile/jackson.hu8026#!/vizhome/Visualization1-individualproject/Dashboard1?publish=yes)
