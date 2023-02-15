# Project_1

**Project Title: Analysis of U.S. Unemployment Rates (2018to 2022)**


Collaborators: 
1. **Crisaldry Brito** - https://github.com/Crisaldry
2. **Ivan Galeano** - https://github.com/igaleano2
3. **Angela Narag**- https://github.com/angelanarag


**Project Description:**
- Analyze the unemployment rates across the U.S. within the last 5 years by time, geography, industry including factors that have contributed to the unemployment rate. 


**How to Use the Project:**
**The project has four different codes** 
**1. bls_api_merge_CSV.ipynb**
	- This is the main code for data collection and clean up and should run first.  
	- It pulls the Unemployment Rate data from the Bureau of Labor Statistic API and puts all the data together into a CSV file called Unemployment_Rates.csv file 
	- It takes the CONVENIENT_us_confirmed_cases.csv file (U.S. daily Covid19 case count by Counties) downloaded from Kaggle.com and cleans the data to create the new_covid19.csv and Aggregated_Covid19.csv files.  
	- It takes the CPIAUCSL.csv file (Monthly CPI data) downloaded from FRED - Federal Reserve - website and cleans the data to be merged with the Aggregated Covid19 data to produce the Merged_Covid_CPI.csv file
**2. Unemployment_Analysis_Angela.ipynb**
	- This code is dependent on the output from the bls_api_merge_CSV.ipynb file and should run after that code creates the output files.  Once the output files are created, it can run independently and has no dependencies on other codes in this project.
	- Uses the Unemployment_Rates.csv file and the Merged_Covid_CPI.csv file to analyze the national Unemployment Rate, Part-Time Workers Unemployment, Full-Time Workers Unemployment, Covid19 Case numbers, and CPI
	- Produces 5 chart images: Unemployment_vs_CPI_2018-2022.png, Unemployment_vs_Covid19_2018-2022.png, Unemployment_Seas_Unadj_2018-2022.png, Unemployment_Seas_Part&Fulltime_2018-2022, Unemployment_Rates_2018-2022_BoxPlot.png
**3. Unemployment_Analysis_By_State_Crisaldry.ipynb**
	- This code is dependent on the output from the bls_api_merge_CSV.ipynb file and should run after that code creates the output files.  Once the output files are created, it can run independently and has no dependencies on other codes in this project.
	- Uses the Unemployment_Rates.csv file to analyze unemployment at the U.S. state level and creates a sample map using the statelatlong.csv file.
	- Produces several charts: Average Unemployment Rate in the United States (2018 - 2022) Bar Graph.png, Average Unemployment Rate in the United States (2018 - 2022) Scatter Plot.png, Average Unemployment Rate in the United States (2018 - 2022) line Graph.png, Average Unemployment Rate in the United States (2018 - 2022).png, Average Unemployment Rate in the United States (2018 and 2020).png, Average Unemployment Rate in the United States (2020 and 2022).png, Outlier States (2018-2022) 2.png, Outlier States (2018-2022).png, Percent Change in Unemployment Rates (2018 and 2020).png, Percent Change in Unemployment Rates (2020 and 2022).png, sample_map.png, verage Unemployment Rate in the United States (2018 - 2022) Scatter Plot.png
**4. Unemployment_Analysis_Ivan.ipnyb**
	- This code is dependent on the output from the bls_api_merge_CSV.ipynb file and should run after that code creates the output files.  Once the output files are created, it can run independently and has no dependencies on other codes in this project.
	- Uses the Unemployment_Rates.csv file to analyze unemployment rates in three industries: Healthcare, Finance, Hospitality
	- Supplements the analysis with Layoffs by Industry data 
	- Produces several charts


**Data Sources:**
1. Bureau of Labor Statistic API
	- Unemployment Rates:	https://www.bls.gov/developers/api_python.htm
2. Kaggle.com
	- Covid19 Cases:	https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university?select=CONVENIENT_us_confirmed_cases.csv
	- Layoff by Industry:	https://www.kaggle.com/datasets/salimwid/technology-company-layoffs-20222023-data?resource=download
3. FRED - Federal Reserve
    - CPI: https://fred.stlouisfed.org/series/CPIAUCSL
4. Geoapify
	- Longitude/Latitude information:	https://www.geoapify.com/geocoding-api?gclid=CjwKCAiA3KefBhByEiwAi2LDHP74Kb1XvOGeVsNzE-rpHgn4L7z9nRDROL3We5eWaXtjy_Ivktpi6hoCEMgQAvD_BwE


**Project Questions**
1. What is the national unemployment rate from 2018 to 2022?
	a.	Are there significant peaks and troughs?
	b. 	Did the Covid19 pandemic impact unemployment?
	c. 	Does the rising inflation (CPI) impact unemployment?
2. What is the unemployment rate by state and how does it compare to the national rate?
	a.	Provide outlier states
	b.	Compute statistics
	c.	Perform in-depth analysis and comparison of each states' unemployment rates
3. Look at the unemployment for three specific industries (Healthcare, Finance, Hospitality) and compare to the national rate
	a.	Provide outlier industries
	b.	Compute statistics
	c.	Perform in-depth analysis and comparison of each industry's unemployment rates  


**Project Assignment:**
1.	National Employment Rate by Time - Angela
2. 	Employment Rate by State - Crisaldry
3. 	Employment Rate by Industry - Ivan


**Analysis Results:**
**1.	National Employment Rate**
	- U.S. unemployment was at a low of 3.5% in February 2020 before a sharp increase to 14.7% in April 2020.
	- There is consensus that the Covid19 pandemic had significant impact on the labor market leading to widespread job losses.
	- Throughout 2020, unemployment steadily declined from its peak to 6.7% in December 2020 and is back to 3.5% in December 2022
	- Part-Time workers were disproportionately impacted by the Covid19 shutdowns, at the peak, the Part-Time workers unemployment rate was 24.3% compared to Full-Time workers at 12.9% and the national rate of 14.7%
	- Based on the Pearson’s Correlation, Unemployment Rates and Covid19 Cases have a correlation coefficient of less than < 0.3, which means there is no correlation, or it is very weak, even though there is consensus that the Covid19 pandemic was the main reason for the large spike in unemployment in 2020. Therefore, simply comparing the number of Covid19 cases by itself to the Unemployment Rate is not enough to show correlation. We must also look at other factors such as industry, state, number of remote workers, etc. to get an overall better picture of the cause of unemployment.
	- A well-known indicator of inflation is the Consumer Price Index (CPI), a measure of the average change overtime in the prices paid by urban consumers for a market basket of consumer goods and services. The correlation coefficient of Unemployment Rate and CPI is -0.2 which proves the negative correlation, but it is still less than < 0.3 which can mean there is no correlation, or it is very weak. However, if only look from April 2020 to December 2022, the correlation coefficient becomes stronger at -0.68.

**2. Employment Rate by State**
	- The U.S has saw dramatic changes in the unemployment rates by states in the last 5 years.
	- During 2020, the unemployment rate across all 50 states saw an increase. According to the Bureau of Labor Statistic, the spike in unemployment in 2020 was due to the Covid Pandemic that led to worldwide shut down. 
	- In 2021, the unemployment rate began to slowly decrease as business began to reopen, stimulating the economy. 
	- By 2022, the overall unemployment rate trend began to return to similar pre-pandemic rates. unfortunately, not all states have been able to return to their pre-pandemic rates, while others have been able to reach, if not lower their pre-pandemic unemployment rates. 
	-  On average between 2018 and 2020, the unemployment rate in the United States rose by 101.54 percent, with exception of Hawaii. Between these two years, Hawaii’s unemployment rate rose by 410.17 percent.
	- On average between 2020 and 2022, the unemployment rate in the United States decreased by -51.89 percent, with Hawaii displaying the greatest decrease with -67.94 percent.
	- States like Hawaii, went from being the state with the lowest unemployment rate in 2018, to the state with the highest unemployment rate in 2020. While there has been a decrease in the unemployment rate, the country has not yet returned to their pre-pandemic rate.
	- Alaska, on the other hand was the state with the highest unemployment rate in 2018 and in 2019. Since the 2020 peak, their unemployment rate has continued to decrease, reaching lower than the pre-pandemic rates. 

**3. Employment Rate by Industry: Healthcare, Finance and Hospitality**
	- Hospitality: Travel restrictions and lockdown measures have severely reduced demand for hotels, restaurants, and other related services.
	- Financial: Unemployment rates have increased, consumer spending has decreased, and businesses have struggled to stay afloat, leading to an overall reduction in demand for financial services. As a result, some companies in the finance industry have implemented cost-cutting measures, including layoffs.
	- Healthcare: While some areas, such as hospitals and urgent care clinics, have experienced a surge in demand and have had to hire more workers to keep up, other areas, such as elective surgeries, have seen a decrease in demand and have had to reduce staffing levels.
	- The COVID-19 pandemic has had a significant impact on employment around the world, with many companies and industries experiencing layoffs and job losses.
	- Unlike layoffs due to COVID-19, which have been caused by an external and unpredictable factor, layoffs due to general financial problems are often caused by broader economic trends and cycles.


