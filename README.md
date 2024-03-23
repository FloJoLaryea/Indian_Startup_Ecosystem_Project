
# **Exploring the Indian Startup Ecosystem**: *A Data Driven Analysis of Funding Trends and Industry Sectors*

The project's goal simulates an initial scenario when my team, say Bloomtech is trying to venture into the Indian start-up
ecosystem. As the data expert of the team, the goal is to
investigate the ecosystem and propose the best course
of action.


## Overview

The project delves into exploring and analysing datasets from 2018 to 2021 ranging from the typical amounts of funding, the typical investors, the hotspot locations for establishing a headquarter of a business start-ups in India as well as the various stages of funding in order to gain insights of sweet spots for future exploration.
 The project utilised the **CRISP-DM** framework approach 
## ✍️Data Understanding
The data was pulled from the following various sources:
- 2018 data from a Github repository
- 2019 data from a OneDrive 
- 2020 and 2021 data from a SQL database

The major libraries used for this project were:
 1. Data manipulation: NumPy, pandas
 2. Data visualisation : Matplotlib, Seaborn, Plotly

 
The common columns contained information of at least:
- Company or brand
- Stage of funding
- Description of company's objective
- Headquarter of company
- Investors
- Industry or sector
- Year company was founded
- Founders of the company
- Amount of funding

From a quick screening of EDA, it was evident the datasets needed to be cleaned and preprocessed for further analysis. There were a huge number of null values, mismatched columns, different column names and wrong datatypes just to name a few. Their corrections were implemented further in the data cleaning process.
## 🔅Hypothesis

Initial exploration on the data gave insight to a **null hypothesis** which believes the funds a company receive does not depend on the sector. and its **alternative hypothesis** which believes the inverse.
This influenced the example questions below which guided the analysis:

- Which particular sector received the most funding over the time frame?
- What is the distribution of fundings based on locations?
- What was the impact of COVID-19 pandemic on startup funding in 2020?

For the hypothesis testing, the method choice was ANOVA.

## 🔎Assumptions
⭕India ususally deals with USD dollar as its currency for business and as such, all other currencies will be converted.

⭕Amount of funding for 2020 is in USD dollar although there is no currency attached.

⭕The founded year for 2018 will be assumed to be 2018.

⭕ All locations just stating the state will take the capital as headquarter.

⭕ Nulls of columns such as the stage or investor were to be filled with “undisclosed” under the assumption that source of such knowledge was classified, some companies had not yet received funding, and some companies were self funding with their own capital in order to maintain the data unbiased.
## 🏋️‍♀️Data cleaning and preparation

The first phase of the cleaning aspect checked for duplicates and nulls in the individual datasets and focused on the amount column as well as the stage column. 

Key highlights of the cleaning involved:

- Converting to right datatypes and formatting. for eg.by converting to the right currency used if necessary, removing character such as the dollar sign.
- Renaming column names to be coherent with each year.
- Stripping unwanted characters in the dataset to prevent errors in calculations. 
- Replacing categoricals such as “Undisclosed” with null value where necessary.
- Swapping the wrong column value with the right column value for a given row.
- Appending a year of funding to each column to track them after concatenating.
- Stripping of mutliple values in a column and maintaining the required one.
- Filling null values by various methods based on the column eg.mean, median etc.
- Redefining and regrouping similar or almost equal values in some columns eg. stage into general names based on research





The stage column was cleaned on research with the dedicated website for the Indian startup ecosystem. There were mapped onto the existing stage column to give a more summarized version of the different names of the stage of funding:
After Research on the stages of startup from the , we decided to regroup the stages into these categories based on the stage of a start-up:

1. Ideation - Source of funfing relies heavily on savings, family and friends and grant money.

2. Validation - Funding usually comes from government loan schemes, angel investors, incubators or crowdfunding.

3. Early Traction - Sources of funding include venture capital funds, bank debts, and venture debt funds

4. Scaling - Sources of funding include venture capitals especially when the startup has gained major market attention. Some private equity or investment funds may provide funds for startups with consistent growth record.

5. Exit Option - In this stage, the investors may decide to merge the company with another, list the companies in the stock market(for those with impressive record of profits), sell shares to other private equity firms or the founders may even buy back their shares in order to gain back control of the company.

6. Others for these stages: Private Equity, Corporate Round, Non-equity Assistance, Debt, Bridge, Edge, Upspark

7. Undisclosed for all values of "Undisclosed",None and Null Values


After the stage was filled, it was used to group the amounts based on the various stages to fill the amount with the median. The choice of the median was done to influence of outliers on mean. 
## 🔅Exploratory Data Analysis
The Exploratory Data Analysis phase delved deep into the cleaned and preprocessed datasets of the Indian Startup Ecosystem from the 2018-2021 funding records. Through a series of analytical techniques and visualizations, key insights were uncovered, shedding light on various aspects of the startup landscape. The following are some of the key insights gained from the EDA process:
- trends in average funding amounts over the years, showcasing whether there was a growth or decline in investment in the Indian startup ecosystem.
- outliers skewing the distributions
- understanding the distribution of startups across different sectors and regions provided insights into the areas of focus and potential opportunities for growth.
- exploration of investor data highlighted the key players in the funding landscape, their investment preferences, and the sectors they were most interested in.
- metrics such as funding rounds, success rates, and funding sources were analyzed to identify factors contributing to the success of startups in securing funding.
- startup locations and funding distribution geographically helped visualize regional disparities and identify areas with high startup activity.
## 📉Data Analysis 
Visualisations were produced based on the analytical questions asked. These visuals were paramount to providing a solid foundation for analysising any trends or hitting patterns in this time series analysis such as how the variables affected the success of a startup securing funding.

Although executed separately in jupyter notebook, these visualisations were deployed in PowerBI and the results are as shown in the dashboard below.

![Screenshot 2024-03-22 233208](https://github.com/FloJoLaryea/Indian_Startup_Ecosystem_Project/assets/134957633/828c9b39-1a71-4b52-99ea-52b88ff173f9)
[Link to PowerBI dashboard](https://app.powerbi.com/groups/me/reports/2e9567cf-ba66-4d52-beb2-dd93bc02be45/ReportSection?experience=power-bi)

## 👀Observations
🗝️It was proven that the amount of funding does indeed depend on the sector involved.

🗝️It was also evident that when it came to sectors, the top 3 sectors were Financial Services, Retail and IT and Technology respectively.

🗝️In India, Mumbai and Bangalore were the two city that received the most funding. However, interestingly enough, Bangalore had the most number of startups.

🗝️The ability to secure funding for a business soared after 2019 through 2021 and further investigations detected an influence from the effects of the Covid-19 pandemic on India in 2020. India being a tech dominated country had the upper hand in 2020 as most services were moved to online platforms. These technologies extended to other fields especially the finance domain which boomed the year after the pandemic probably in order to stabilise the economy

🗝️Although the study was able to detect top investors in start up business in India, the greater percentage were undisclosed, probably due to anonymosity or classified information. 

🗝️A great portion of funding falls in the traditional scaling and exit option stages as well as a significant portion of private equity firms investing at this stage. This implies most investors are willing to fund once businesses have survived the initial stages and proved high chance of success and profit returns.




## ✍️Conclusion and Recommendations
From the study, it can be concluded that Financial Services is the heart of start-up businesses in India with majority of these services combined with digital or technological services.

India is one of the world leaders in Technology and IT and it's no surprise when combined with finance, it translates to the Financial Services which looking at the timeline, were funded massively in a bid to stabilise the economy after the 2020 pandemic.

In addition, location favors the amount of funding one receives. If business are set up in Mumbai or Bangalore, the probability of getting funding is high. 

It is also safe to say that the more funding of a given year, the more startups would spring up. Recommendations are therefore, to branch in finance in either of top 2 headquarters. More analysis has to be carried out on the origin of investors.

It is also recommended that the younger the startup, the more work has to be done in terms of innovation, marketing and networking in order to attract investors quickly. Otherwise, the main source of funding is self-fund, family and friends and government.


It is also recommended to enhance analysis in the future with machine learning models to predict a projection of the current years as well as integrating with real time data to monitor market trends and analyse factors influencing startup business metrics. The likelihood of success of a business or the rate of growth depending on the sector could also be studied.

Overall, a majority of startups in India seem to thrive as India is a digital/tech dominated country and about the greater portion of startups are in this sector. The Indian startup ecosystem has growm rapidly over the recent years and even more growth can be anticipated in the coming years.
## 🙋‍♀️Authors

- Florence Josephina Laryea
- florencelaryea88@gmail.com
- [Link to my article on Medium](

  **Co-authors**
- Members of Team Selenium: Bright Abu Kwarteng Snr, Success Makafui
Kwawu, Ikeagwuchi Andrew, and Abraham Worku Woldeselassie.


## 🤗Acknowledgements
Much of our sincere gratitude goes to our instructors Racheal Appiah-Kubi and Violette Naa Adoley
Allotey for their exceptional guidance, unwavering support, and invaluable mentorship throughout the course of this project. 

Their expertise, dedication, and commitment to our learning journey have been instrumental in shaping our understanding and skills in data
analysis.



## 📚References and bibliography
[Indian startup ecosystem](https://www.startupindia.gov.in/content/sih/en/funding.html)

[Restructing column sectors](https://www.businessinsider.in/business/startups/news/top-10-industries-for-new-startups-in-india-as-per-hurun-list/articleshow/105651758.cms)

[Currency exchange rate](https://www.poundsterlinglive.com/history/USD-INR-2018)
