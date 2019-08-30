 
[印象盐城 数创未来大数据竞赛 - 乘用车零售量预测](https://tianchi.aliyun.com/competition/entrance/231640/information)

### Competition Background

The “Thirteenth Five-Year Plan” is a new era for the development of the automobile industry. The economic situation is complex and changeable, and the automobile industry policy is frequent. Therefore, accurately predicting the sales volume of automobiles is extremely important for the government and enterprises. Sub-regional sales forecast is conducive to local governments accurately grasp the development and growth of the automotive market, timely adjust macro industry policies, and help industry regulators to monitor production capacity of auto manufacturers. For enterprises, it is necessary to fully understand the consumer's demands, anticipate the future demand of the market and possible sales trends, rationally plan production capacity, correctly formulate production plans, and implement production strategies for sales.
Most of the existing automobile sales forecasting studies are macroscopic forecasts, and the forecasting target is the overall sales volume of the entire market, and the forecasting granularity is broad. For the government, industry regulators, and automotive companies, there is a need for more granular sales forecasting solutions.


### Introduction to the preliminary contest

The preliminary competition provides data on the sales configuration of the Yancheng sub-model from January 2012 to October 2017. Participants are allowed to use any publicly available external data to assist the forecast.
The preliminary round is divided into two stages. The first stage requires participants to predict the sales data of the Yancheng sub-models in November 2017. The second stage requires participants to predict the sales figures of the Yancheng sub-models in December 2017.

The first stage evaluation time: January 15th - February 25th, 2018
The second stage evaluation time: February 26, 2018 - February 27

### Introduction to the final contest

The final contest will provide data on sales distribution of national sub-cities from January 2012 to December 2017, national overall model production data, and national macroeconomic monthly data. Participants are allowed to use any publicly available external data to aid in the prediction.
The final contest are divided into two phases. The first phase predicts the sales data of the national sub-cities in January 2018. The second stage predicts the sales figures of the national sub-cities in February 2018.

The first stage evaluation time: March 1st - March 12th, 2018
The second stage evaluation time: March 15, 2018

# Competition results
No.52 in Preliminary Contest

No.73 in Final Contest

Total 2635 teams

# Solutions
1. Go back to real date: Verified the real date with the weekend and holiday pattern. The date period of preliminary contest is 2013-01-02 to 2017-11-28, while the date period of final contest is 2013-01-01 to 2017-11-28.

2. Labelled national holidays and festivals in both lunar and gregorian calendar to generate features. Taking brand, holiday_type, day_of_week, year, month, week_of_year (1-52) as features, where brand, holiday_type, day_of_week are used as categorical variables. 

3. Separated the top10 best-selling car brands to build an isolated model

4. Utilized time series cross-validation to find structural changes while controlling the overfitting parameter. Randomly select 0.1 as the validation set and submit the results of the LighGBM and CatBoost algorithm.
