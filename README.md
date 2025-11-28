Ideation for the Thesis on “Quantamental study” aimed at identifying more timely and robust signals specifically for “value investing”/ "shopt term trading" on stocks listed in Indian Market (NSE) (subset_count ~ 750). 

The objective I am targeting at is to shorten the typical holding period for value stocks while maintaining the fundamental basis of the strategy and benefitting from the noise. So in a way it translates into a conditional approach for trading/investing. But, it helps in understanding if the relationships between segments can provide excess returns when implemented using Graphs.

**Ouline of Thesis** 

- I am proposing to use “daily/ weekly price data” (so we filter-out out noise to certain levels) for “Technical Analysis” and “Quarterly financial Reporting” for “Fundamental Parameters” of companies.
  This data I want to train using Graphical Neural Networks with Grapgh Attention Network as companies are related by sectors, and they also tend to have Customer Relationships, along with having a same parent company        listed   under different segments.
  
  (Challenge with using wekly data is the implemention of daily signals due to Macro Events, Earnings Release, Dividend Payouts, Stock Splits etc.) -> So may go ahead with daily data.
  
  (Customer Relationships -> Value Chains data is not consistent on Eikon... trying to get data through Bloomberg) ... in case not possible or not avialable, will go ahead with Relationship data for (Sectors, Complementary Product Market, Seasonal Product Segments (can be captured inherently in Grapgh too),  Parent/ Group Holdings, Mutual Funds Holdings, Bulk Trades over time with different companies (buy/sell).)
   
-	Graph Nodes - StockNames | Sectors | Companies in Value Chains*, all will be connected through a network-graph structure based their relationship status.

**Objective**

Merge the “_slow-moving fundamentals_” with “_faster-moving market and sentiment variables_” to generate **signals**, which can then be evaluated over different holding periods 
  
  The period needs to be evaluated 
  
  For Daily Prices 
  (5day ahead)  |  (10day ahead)  |  (30day ahead)  |    (60 day ahead)
  
  I plan to compare the results with other ML models using Random Forests/ XGBOOST/ LightGBM.

**Prominent Data Sources**
#####  National Stock Exchange India - bulk_deals data
#####  LSEG-Refinitive-Eikon         - Company Fundamentals and Technical Price (OHLC) Data
#####  yfinance                      - Pricing Data (validation)
