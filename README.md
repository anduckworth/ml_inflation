# Building a Resilient Portfolio
## Mala Sharma, Alexander Narvaez-Duckworth, Louis Donofrio, George Mihalopoulos, Matt Szoke



## Proposal / Hypothesis

We have used machine learning and stock analysis to study market trends from the early 2000s to 2021. We believe that a multifaceted machine learning approach would allow us to analyze various businesses, commodities, and macroeconomic metrics to discern the investments that may be most resilient to inflation. We have also focused on company specific financial parameters and distinct outcomes as compared to large-cap closing prices.

### Lou: Automated Stock Selection Using KMEANS

### Findings <br>
![caption](image)<br>

### Matt: Machine Learning on Macro Economic Metrics and Commodities

### Findings <br>


![caption](image)<br>

### Alex: Machine Learning on Company Financials

We used [Polygon](https://polygon.io/stocks) as the primary source of company financial information. This was a useful API for testing because of its speed and easy access to information through Get requests. We pulled in all of the financial data for our respective companies to the notebook and created a dataframe from it with a datetime index. Then we set a return period for the amount of time we would lag the dataset in order to perform training and testing, and scaled/preprocessed the data using standard scaler. To visualize the data, we utilized a correlation matrix. To dial in on the data that we were using in our X variable we decided to utilize the selectKbest method from sklearn. This helped us narrow down the valuable columns to 10, using the selectkbest top 10 scores. After this, we set our X variable dataset to these 10 columns and proceeded with determing the best models to use for this data. The lowest errors for the testing data the Linear Regression, Elastic Net, and Lasso models from sklearn. We graphed these threee different models and the predicted was extremely similar to the actual for all three. 

### Findings 

We found that marketCapitalization,	sharePriceAdjustedClose, priceSales, priceToSalesRatio, enterpriseValueOverEBITDA, priceToEarningsRatio, priceEarnings, enterpriseValueOverEBIT, dividendYield, issuanceEquityShares were the pieces of a companies financial statement that contribute the most to predicting the enterprise value. This makes sense because the [Enterprise value includes in its calculation the market capitalization of a company, short-term and long-term debt as well as any cash on the company's balance sheet.] Enterprise value is basically a more robust form of the market capitalization because if you were to completely takeover the company, the enterprise value tells you the debt you would have to pay off and the total amount of cash on hand that is able to pay that debt off and any other parts of the acquisition. To take this part of the project a step further, I beleive it would be useful to connect the beginning of the company financials to the KMEANS automated stock selection and perform the financial analysis based off of those companies. In addition to this we would also be able to tie the performance of these company's enterprise values to inflation to create an automated, machine learning generated, portfoloio selector to compete with an inflationary environment.

