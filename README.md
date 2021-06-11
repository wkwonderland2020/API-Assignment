# U of T Fin Tech BootCamp Class Unit 5 Assignment #

## API

By: Ivan Kin-Ngai Fung

Date: June 10, 2021

**Objective**

The objective of this assignment was to perform a Personal Financial Planning application to 
and to develop a tool which can assess indivdual's financialhealthiness based on his savings and investment portfolio.  Furthermore, the developed application should able to forecase a good retirment strategy based on the investment in crytocurrency, stocks and bonds.   

By using the tools we learned from the class, we were required to retrieve financial data from Alpaca and Alternative Free Crypto APIs and to perform the anaylsis based on these data.  
WE had to filter out the unneccessary data and left with the closing price of the financial instruments to perform the analysis.  The instrutments included cyrtocurrency, stocks, and bonds.  

First part of the assignment was to develop a tool to visualize the savings by the investments in crytocurrency and the traditional securities, and to verify if the savings were sufficient to meet the emergency fund level.

Second part of the assignment was to run simulation on the historical closing for the bonds and stocks in the retirement portfolio, and to project the financial performance of the portfolio in 30 years.  The descriptive statistics data were adopted to calculate the expected portfoio return given a specific initial investment over the specified time horizon.



**Results and Discussion**

*Part I - Saving vs Emergency Fund*

Saving Health Anaylsis

After fetching the financial data from Alpaca and Alternative Free Crypto APIs, we can use the data to calculate the total monetary value for each asset group and to determine the total monetary value in the portfolio.  A pie chart was plotted to illustrate the distribution of different asset group. About 60% of the portfolio is composed of cryptocurrency and 40% in tradtional securities.

The results shown that the total monetary value of the portfolio is abou $112,819 which are well above the emergency fund level of $36000 (3 times of the monthly income).

As in part 2 of the assignment, the Monte Carlo simulation was adopted to forecast the expected outcome of the investment based on the histrical prices.  We were asked to used 5 years' historical pricing data and forecast the expected cumulative return for an inital investment of $20,000 in 30 years time horizon.  

Number of Simulation for each trading day is 500 and time frame is 30 years X 252 days = 7560 days.  


From the results of simulation, the descriptive statistics were calculated using the build-in functions within MCSimulation library.  

The descriptive statistics as shown below:
count           500.000000;
mean             18.438077;
std              12.821357;
min               2.100021;
25%               9.223469;
50%              14.710407;
75%              23.193524;
max              98.592079;
95% CI Lower      4.606749;
95% CI Upper     50.749579;

So, the expected mean was 1843% with standard deviation of 1282%.  The 95% confidence levels was computed as 461% and 5075% in the 30 years time horizon.  As a result, the expected portfolio return with 95% confidence level based on $20000 initial investment would be in the range of $92,135 to 
$1,014,991.


To tackle the optional challenge, the weight in the portfolio was adjusted to capture more return in a shorter time horizon.

5-year horizon:  weight in portfolio (30% in bonds and 70% in stocks)

10-year horizon: weight in portfolio (20% in bonds and 80% in stocks)

The descriptive statistics 5-year time horizon as shown below:

count           500.000000;
mean              1.761536;
std               0.551369;
min               0.628063;
25%               1.342592;
50%               1.686786;
75%               2.097803;
max               3.918757;
95% CI Lower      0.930336;
95% CI Upper      3.049248;


The expected mean was 176% with standard deviation of 55%.  The 95% confidence levels was computed as 93% and 3049% in the 5 years time horizon.  As a result, the expected portfolio return with 95% confidence level based on $60000 initial investment would be in the range of $55820 to $182,955.

The descriptive statistics 10-year time horizon as shown below:

count           500.000000;
mean              3.551979;
std               1.819031;
min               0.640512;
25%               2.251610;
50%               3.088179;
75%               4.426607;
max              11.267047;
95% CI Lower      1.302492;
95% CI Upper      8.511505;


The expected mean was 355% with standard deviation of 182%.  The 95% confidence levels was computed as 130% and 851% in the 10 years time horizon.  As a result, the expected portfolio return with 95% confidence level based on $60000 initial investment would be in the range of $78150 to $510690.

Based on the results from 5-year and 10-year retirement plan, the portfolio mix of bonds and stocks could not overly weighted to stock since it would affect the standard deviation of the portfolio and further undermine the value of the 95% lower confidence level.  In other words, the "lowest" expected portfolio return value would be much lower than that of portfolio with higher proportion in bonds.  As a result, we must make a judgement to balance return vs risk to meet the ultimate financial goal.  

To conclude, the 10-year portfolio had a better performance than that of 5-year portfolio with higher expected return based on the same initial investment.  The expected return was in the range of 
$78,000 to $510,000 with 95% confidence level.



 


