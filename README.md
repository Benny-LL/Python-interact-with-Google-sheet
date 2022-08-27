# Python-interact-with-Google-sheet
obtain per min data through market data api in google sheet

With the google sheet api credential JSON file, the code could interact with a google sheet file with "market data" api installed (more info.: https://www.marketdata.app/). 
"market data" api allows the user to input add-in formulas to obtain the basic price and volume data of a specified stock in a specified time interval and period. Each of the data point (datetime, price, volume) will automatically show in each of the blanks in the sheet. 
However, this api could only generate the data in 60 consecutive days every time, so the formula will need to be updated for certain times when the specified period exceeds 60 days.
In this case, pygsheets updates the formula inside the cell A1 repeatedly and captures the data generated afterwards as a dataframe, then multiple dataframes will be consecutively generated and integrated to be a single completed dataframe by pandas, eventually pandas makes the dataframe into a csv file. 

