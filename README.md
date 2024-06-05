# Project Name: Bike Sharing Assignment
	
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short-term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all-around and stand out from other service providers and make huge profits.
The Objective of this assignment is to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 


## Table of Contents

## General Information
  
       I have used the day.csv file to analyse the demand of the bikes in 2018 and 2019. This dataset contains factors like year, month, season, windspeed.
  Cnt is the count of the total bike rented on a day.
  
  Followed the below steps to understand the demand of the bike.
  1. Data Understanding: There are 730 rows and 16 columns provided in the day.csv file. Data dictionary is used to understand the data captured in the excel.
	 
  2. Data Cleaning & Manipulation:
	There are no missing values. The data provided is clean and complete. 
		
  3. Performed EDA and Univariate Analysis: Based on the univariate analysis
• Demand in spring season is visibly very low
• Demand has drastically increased from 2018 to 2019
• Demand is the highest in the month of Sep and Oct and lowest in the month of Dec and Jan
• Not much variation seen in the days of the week but Mon seems to have a slightly higher demand
• Demand is slightly higher on holidays and when its not a working day
• Demand is highest on Clear days and lowest on Snowy days
		
 4. Creating dummy variables: Dummy variables were created for month, season, weathersit and days of the week. Holiday, yr and working day were binaries so they were left as it is.

5. Data preparation for modelling: 
• The data was split into train and test with 70-30 ratio
• Train dataset was scaled using Min-Max scaler
• The data was fit and transformed

6. Building the model: Model was build using RFE method by giving the variable count as 20. 9 variables were removed and the model we got had 20 variables.

7. Assessing the summary data on p-values, vof, R-sq and F-stat: VIF was calculated for the 20 variables. Variables with high p-value(>0.05) and high vif (>5) has to be dropped. Following order is followed:
• High p-value and High vif: Drop the variable one at a time
• High p-value and low vif: Recheck the vif for other variables
• Low p-value and high vif: Drop the variables one at a time and recheck the vif values
Total 9 variables were manually dropped and the final model has 11 variables

## Conclusions:
	
	Based on the above analysis below conclusions are made:
	
		- Yr, workingday, Sep (mnth=9) and Mon (weekday=6) have a positive influence on the demand of the bikes
		- windspeed, light snow (weathersit=3), Mist (weathersit=2), Spring (season=1), Nov (month=11), Dec (Month =12) and Jan (month=1) have negative impact on the demand of the bikes.
		- This means that the demand will increase year on year.
		- Demand will be highest in the month of Sep and on Mondays.
		- On the days with light snow or mist or high windspeed, demand will decrease
		- Demand will drop in Spring season
		- Demand will also reduce in the month of Nov, Dec and Jan.


## Acknowledgements
	 This project is created based on the trainings provided by UpGrad Team.


## Contact
   Created by Trapti Agarwal  

