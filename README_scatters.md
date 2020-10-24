Scatter Plot and Linear Regression Analysis 

1 - Our first approach involved the assessment of both health factors and socioeconomic factors related to access to 
healthy foods. However, our analytical approach and evaluation morphed with time. 

-For all scatter plots, to confirm that each was utilizing the most data possible, in each plot I created a separate 
	dataframe based	on all rows in common between the two desired columns.

Initial Scatter Plot Evaluations: 
- % Adult Obesity as a function of % Poverty Rate (% of county pop below the poverty line) 
- # Diabetic Medicare Enrollees Per County as a function of % Poverty Rate 
- # Deaths Per County as a function of % Poverty Rate (% of county pop below the poverty line) 
- % Adult Obesity as a function of Food Environment Index Rating
- # Diabetic Medicare Enrollees Per County as a function of Food Environment Index Rating
- # Deaths Per County as a function of Food Environment Index Rating

I then split up our dataset into two dataframe to represent counties that would be considered food deserts, or non-food 
deserts by the following logic:  

- Per USDA, approximately 10% of census tracts are food # deserts. We estimated that approximately 10% of our counties 
	would be food deserts, and got the Food Environment Index (FEI) ratings of the bottom 10% of counties.  
- For the FEI, 0 has the hardest access to health foods, while 10 has the easiest.   
- separate dataframes were created to evaluate food deserts (data for counties with bottom 10% of FEI ratings) and 
	non-food deserts (data for counties with top 90% of FEI ratings)

I then repeated each of the analyses combinations above for each group (food desert and non-food desert), and also added
the following relationship:
- % Adult Obesity as a function of Unemployment (% of County Population) 

However, in performing these analyses, I noticed that using total number counts per county (i.e. for diabetes and deaths)
was not appropriate, as a more populous county would, for example, likely have many more deaths than a less densely
populated county.  

Therefore, percents were calculated to normalize the count data to the population.  I calculcated percentages and added them
to the dataframe as follows (not all were used, but could be used in future analysis):
	data_df["% Diabetics"] = pct_diab
	data_df["% Deaths"] = pct_dead
	data_df["% Violent Crimes"] = pct_crime
	data_df["% Unemployed"] = pct_unemp
	data_df["% TractSNAP"] = pct_snap
	data_df["% LAPOP1_10"] = pct_LAPOP1_10

I reran the initial relationships that had utilized counts, replacing those series with percentages insted.     
I also attempted to reduct the number of points on plots by using a random sample function, selecting 300 
datapoints (approximately 10 to 20% of dataset).  However, the results were no more or less visually appealing.  

Interim Results Evaluation:
- The interim results of the scatter plots and linear regression analysis did not suggest a strong correlation between 
	any of the relationships. Correlation coefficients (in absolute value) ranged from 0.0 to 0.4, withe
	the lowest and highest at the folloing: 
	- The % of Deaths as a function of % Population below the poverty line in Non-Food Deserts had a correlation 
		coefficient of 0.0.  
	- The % of Deaths as a function of % Population below the poverty line in Food Deserts had a correlation 
		coefficient of 0.4.  
	- Although it appeared there were measureable differences in this relationship inside versus outside food deserts, 
		the overall correlation coefficients were not strong enough to support statistical significance.  

Alternate Analysis
Given that the results of these analysis did not seem to support a statistically significant relationship, further analysis
of these comparisons was abandoned.  After regrouping, we approached the data in a different way to further evaluate
whether any correlations existed. Additionally, we noted that in the state of Montana, the data seemed to suggest some relationship 
between % obesity, % diabetes, and demographic racial distribution inside and outside of food deserts.  Therefore, I 
utilized the original dataframe with all data (both food and non-food deserts), and focused in on comparing data the 
following possible relationships in the US overall, and in Montana: 
- % Adult Obesity as a function of Food Environment Index in the US
- % Adult Obesity as a function of Food Environment Index in Montana
- % Diabetic Medicare Enrollees as a function of Food Environment Index in the US
- % Diabetic Medicare Enrollees as a function of Food Environment Index in Montana
- (evaluation of racial distribution was performed using pie charts).  

Final Results
While possible minor trends were identified in the relationships above, again, the correlation coeffiecents (in absolute 
value) ranged only from 0.17 to 0.27, indicating that there is no statistically significant dependency of Adult Obesity or Diabetic
Medicare Enrollees as a function of the Food Environment Index.  This suggests that regardless of easy or difficult access 
to healthy food, the number of people with diabetes and number of people with obesity does not change. Therefore, we cannot
reject the null hypothesis.       

Limitations
Available health data did not parse characteristics to the census tract level, while food desert data did.  We utilized the 
Food Environment Index because it was the best indicator for ease of access to food at the county level. While our analysis
did not show statistically signifiant relationships, there were minor trends suggesting that a more detailed analysis could
provide a different result.  Heath data (e.g. for obesity and diabetes) specific to a census tract could prove more valueable 
in determining whether a relationship between health effects and food deserts exists.     




Resources:

    Health Data: https://www.countyhealthrankings.org/explore-health-rankings/rankings-data-documentation/national-data-documentation-2010-2018
    Food Desert Data: https://www.ers.usda.gov/data-products/food-access-research-atlas/download-the-data/
    County Coordinates: https://public.opendatasoft.com/explore/dataset/us-county-boundaries/map/?location=5,69.03242,-35.00244&basemap=jawg.streets

