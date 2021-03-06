# Stocks Database

The purpose of this project is to design a useful database for an IBKR trader with multiple accounts. 

In the first stage of the project, we create three tables that can be used to develop trading strategies. The first table ```comp_info``` contains basic information for over 5600 US listed companies. The second table named ```fin_stat```, contains historical quarterly financial statements for the companies included in the first table. This table is suitable for investors who prefer value investing In the third table ```daily_prices``` , we have stored the historical daily prices of each company. To create the two first tables, we import data from an Excel file with multiple sheets our MySQL database using Python (data source: FirstRate). The last table is created by sending API requests to Marketstack.

As we said , an IBKR trader can have multiple accounts. To every account corresponds a stock portofolio. In the second phase we create tables that keep track of the trades of different accounts. The table named ```accounts``` contains information for every existing account and the table named ```trades``` includes all the executed trades of these accounts. For the implementation of this phase, we need access to Interactive Brokers Client Portal Web API. To accomplish this task we use IBeam which provides a Docker image that makes it easy to use the above Web API.

*currently working on how to automate update tables

The entity relationship diagram is shown below :

![Alt text](/tables_samples/erd_stocks.PNG?raw=true "Optional Title")
