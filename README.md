# Ray Capstone Project - Video Games Sales Prediction Modeling



## Problem Statement

With more than 2.5 billion video gamers from all over the world, more gamers are switching towards mobile gaming compared to traditional video game consoles which are slowly moving out of phase.

Being an data analyst in game developer company, I am being tasked to create a predictive model on video gaming market revenue based on the data from VGchartz and also identify what are the most important features that affects the revenue of video games.

Additionally, through analysis, I would like to identify the console among PS, XBOX, Nintendo, Playstation is the console that will possibly generate the most sales and effectively maximising profits and minimising the cost for futher game developments. 

## Executive Summary

With the data that I have extracted from (https://www.vgchartz.com), I did some 'tidying up' on the dataset and to ensure that model is able to predict video games revenue to its best accuracy. 

Afterwhich, I went on to analyse the importantance of each features which will affect the selling price, with the help of visualisation such as Heatmap, Historgraph and Scatterplot. 

Upon identifying important features, I will use do some model preparation work for generating the predictive model.

After generating model, I will then be able to determine the sales prediction of all consoles games based input its features, for example the critic score, sales from north america, release date and genre etc.

The ultimate outcome will be, with the prediction for the sales volume, I will use the data to convince stakeholders of the company to set aside an appropriate amount of budget for future game development, focus on building games based on the most popular video gaming platforms, effectively  boost up and maximise the profit of the company while minimising the cost.


##  Data Collection

Data collection via https://www.vgchartz.com's API to collect approximately 48000 rows with 16 columns.


## EDA & Key Takeaways 

North America region plays the most important part in determining the overall sales of the video gaming industry, which contributed to 40-50% of the market share. Followed by PAL regions, primarily Europe, Australia, Brazil, and regions of Africa and Asia.

There was a shift of trend of popular genre from Sports from late 1990s and slowly evolving to Action games being popular now, we can see that there is no one genre that could well substain through the years.

There seems to be an increase of sales volume during the festive seasons October November and declining from December compared to other months.

Playstation had the most amount of sales and dominated at the top because they had licensing on exclusive distribution on certain popular games and they have been around for a long time before Xbox was launced. In addition, Nintendo and Playstation being a Japan product, many Japanese game deveoper will only launch games based on Playstation platform, resulting in Xbox being unpopular in Japan market.

There seem to be a decline in the total sales over the past 10 years. One reason could be the rise of mobile gaming is taking away sales volume from console gaming and people would prefer to play-on-the-go for the convenience.


## Modeling

### Baseline 
- The mean of total sales is used as a baseline score of around 400,000 for total sales. 
- Our objective is to create a model that has the lowest RMSE score.

### Preprocessing  
- Standard Scaler was used to scale our model.

### Evaluation
- We want to create a production model that can provide useful feature importance information
- Linear Regression, Lasso, Ridge Regression and Random Forest were considered
- Random Forest had the best score among all models 


## Summary

The important features that affect overall total sales are critic_score, release month of November followed by platform to be Playstation.

Through this model, we are able to predict the total sales with with a RMSE score of 650,000, what this means is that our model's prediction is on average off by $$650,000. Given the better performance of the model, it is clear that we achieved the objective of our project succesfully.

The ultimate outcome will be, with the details of the total sales prediction for the sales volume, I will use the data to convince stakeholders of the company to set aside an amount of budget for any new game development, focus on building games based on the Playstation and also allocating more marketing strategies and ensuring that the critics give a good score for our games. 


## Recommendation

Additional outside research found that video game downloadable contents and microtransactions to drive $4 billion in sales alone. Therefore much consideration should be made to increase content with new updates and additional features in the game. This will greatly increase the sales revenue of the game developed as well.

With the genre of Action and Sports games being popular, perhaps we can brainstorm and focus on developing a game that are based on those genre which will be of most interest to most gamers now. One of the idea could be to create a game whereby it has to deal with stock market trading, business creation be it legal or illegal sort of business and enable players get to buy luxurious ranging from cars to even purchasing a soccer team which could be a linkup business opportunities with other sports games.

Additional consideration for future game development is that we can create a game which players get to play on their main tv game consoles and at the same time have an mobile game app which is linked. So in this way, we are able to capture the upcoming trend of mobile gaming and ride the wave on the potential revenues that possible be explode in the years to come.


## Data Dictionary:

Data source: (https://www.vgchartz.com)

- Name - The games title, object
- Genre - Genre of the game, object
- Platform - Platform of the game released (i.e. PC,PS4, etc.), object
- Developer - Developer of the game, object
- Vgchartz_Score - Aggregate score compiled by Vgchartz staff, float
- Critic_Score - Aggregate score compiled by Indepdent Games Sites, float
- User_Score - Aggregate score compiled by Gamers, float
- Total_Shipped - Total shipments from manufacturers, float
- Total_Sales - Total worldwide sales, float
- NA_Sales - Sales in North America (in millions), float
- PAL_Sales - Sales in Asia, Europe, Argentina, Brazil, and Paraguay (in millions), float
- JP_Sales - Sales in Japan (in millions), float
- Other_Sales - Sales in the rest of the world, i.e. Nigeria (in millions), float
- Release Date - Date of the game's release, datetime
- Last Update - Time the game was last updated, datetime


## References:

https://www.wepc.com/news/video-game-statistics/
https://www.gamesindustry.biz/articles/2017-07-20-digital-game-sales-to-reach-usd7-8-billion-this-year-superdata
https://newzoo.com/insights/articles/the-global-games-market-will-generate-152-1-billion-in-2019-as-the-u-s-overtakes-china-as-the-biggest-market/