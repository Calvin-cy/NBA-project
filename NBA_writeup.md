# NBA Players Examination and Salary Prediction
## Abstract
The goal of this project is to examine NBA players' performance based on the stats like points, win/share, plus/minus, etc., and use these stats to create a machine-learning algorithm to predict players' salaries. The datasets I used are mainly scraped from basketball-reference and the advanced stats datasets are from Kaggle. I have done data wrangling in jupyter notebook. I converted the data type, filled up the missing values, and merged the datasets into one big dataset. After wrangling the data, I used Chatgpt to help me write a function that trains the machine learning models and selected the best model and make predictions on the full dataset. I stored the result and used the result to create three interactive dashboards in tableau.

## Design
The project is separated into two parts - machine learning and data visualizations. I assume the players' stats have a direct relationship contributing to their salary, and I would like to prove if my assumption is correct or not. Also, I have done three dashboards for people who are interested in knowing how well the players are in certain fields. 

## Data
- 6225 rows with 58 columns
- feature highlight: WS, Salary, VORP, Predicted Salary, eFG%, Height, Weight, 3P%

## Algorithm 
1. Import the modules that will be used later in the project (requests, BeautifulSoup, and pandas)
2. Use Chatgpt to write a code to scrape the NBA players' stats from 2007-2008 to 2021-2022 into a dataset
3. Used the NBA salary dataset found in Kaggle, this dataset only contains player salaries up to 2020-2021, so the salary prediction algorithm will be focusing from 07-08 to 20-21
4. Merged the previous datasets, and wrangle them by converting the data type, filling up the missing values, and cleaning some columns to make the dataset stabilized
5. Merged the players' bio dataset that I found on Kaggle into one big dataset, and convert the height column into centimeters
6. Scraped the advanced dataset from basketball-reference and merge it into the big dataset that I am working with
7. Removed unused columns and convert datatype into float type, so I can work with them better
8. Used Chatgpt to create a function that takes most of the features in the big dataset in the count, trains the machine learning models with the features, and returns the best model along with the predictions generated by this model in a new column of the original dataset, and return the dataset

<img width="896" alt="Screen Shot 2023-03-03 at 4 23 44 PM" src="https://user-images.githubusercontent.com/63031028/222859792-b89b8423-3902-4ea2-a137-e5e82cddd6e9.png">

9. Stored the results in xlsx format and opened it in tableau to work on the visuals

10. Examined the features and created three interactive dashboards using different stats

![Dashboard 1](https://user-images.githubusercontent.com/63031028/222863446-9e82adc8-607e-4648-9dcf-8787eaeb1003.png)

![Dashboard 2](https://user-images.githubusercontent.com/63031028/222863508-fa393742-152e-459d-8948-762ef1fc75d3.png)

![Dashboard 3](https://user-images.githubusercontent.com/63031028/222863522-54157d87-c1d5-4417-aa28-d15baf1ff797.png)

## Tools
- Python (Pandas, Numpy, Beautifulsoup, sklearn): data wrangling, web-scraping, machine learning
- Chatgpt : Code assistant
- Tableau: Data Visualizations 

## Communication
The salary prediction function takes all the player features and bio into count to generate an estimated salary based on performance, however, NBA contracts are not signed per year, so players may not play up to the standard for the salary they're making. Also, rookies have rookies contracts, so a player like Luka Doncic, is playing phenomenally and he should deserve to get more money, but he will only get it after he renews his contract. The Dashboards that I have created are interactive, and viewers can filter them by years to see how players' performances are different from years. 
## Further steps
The machine learning model can only explain 63% of the variance, I think to boost this result, I have to take the marketing values of the players. Since NBA is a business league, the players' products that they are selling should be taken into count as a business decision that affects the salaries. Therefore, if I can get the NBA marketing dataset, I am confident that the machine learning model can improve the predictability by 10%.