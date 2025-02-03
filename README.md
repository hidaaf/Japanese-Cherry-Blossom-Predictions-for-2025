# Japanese-Cherry-Blossom-Predictions-for-2025

! Note : this page will be updated in the spring to compare our forcasts with the blooming dates in 2025 :) 

## Motivation and Background

Cherry blossom trees, or "Sakura" in the Japanese language, are a distinct species of trees that have become a staple for spring all over the world. Every year, the blossoming of new flowers captivates both locals and tourists, and in most places this natural event officially marks the beginning of the spring season. However, planning holidays and trips in order to witness the Japanese unofficial national flower in its full bloom have shown to be quiet a challenging task. Different factors such as regional climate conditions and yearly weather variations, have made it harder to accurately make these predictions. 

This project is going to be an attempt to analyze and model the hidden trends present in historical data about the blooming of Sakura flowers. Our final goal is to provide accurate forecasts for the full blooming of Cherry blossoms in the coming year of 2025. While multiple attempts have been done in the past to achieve this goal, our project offers a unique approach where we gathered datasets from multiple sources, and produced an in-depth analysis that helps understand this natural process and the factors around it in more detail.

## Data collection 

The data collection process relayed heavily on web scrapping techniques, which were used to gather data from the Japan Meteorological Agency website. The picture below shows how the original format of our data looked like on the website.

(insert the image here)

The original dataset was structured with each row representing a different location, covering a total of 58 cities across Japan. The columns on the other hand indicate the years of observation, with the values representing the peak blooming dates (month and year) for each location. The source website also only displays the data for 10 years at a time, which meant that the collection process needed to be done over multiple web pages to compile a comprehensive dataset. Additionally, the dataset also includes information about whether the location is still currently under observation.
The data processing phase included several steps that allowed us to transform the unstructured output from the JMA website into a structured dataset ready for analysis, key steps included: 

- 	**Turning lines of text into a data frame**
- 	**Standardizing the representation of missing dates to replace the ‘-’ symbol**
- 	**Dropping unnecessary columns**
- 	**Translating the text from Japanese to English**
- 	**Processing special symbols in the data**
The data contained symbols like ‘#’, which indicated what was observed in the previous year; in other words, if we are observing the year 1992, a value of 24/12# refers to 24/12/1991 and not 24/12/1992. Our processing code also successfully fixed these data points
- 	**Final reshape of the data**
- 	**Dealing with missing values**
Our dataset had several observations with missing values, these were nothing other than the rows representing locations that are no longer under observations. As a result, data for these locations was only available up to a certain year and considering that the locations that fall under this category are quite a few, simply disregarding these rows would’ve significantly affected our final results. Therefore, we decided to keep the information regarding these locations but only up until the point where we have observable information.



