## Why Yahoo Finance API ?
Yahoo finance have large datasets of historical financial dataset. It not only contains stocks prices but also other calculated metrics like beta that measures the voltality of a stock compare to the volatality of the entire stock market. Thats why it is great python module.

## How to Install Yahoo Finance API ?
If you are beginners and not have installed it in your system, then you install it you pc using the pip command.

For Python 3.xx version
```pip3 install yfinance```

For python 2.xx verison
```pip install yfinance```

## Step by Step Guide to use Yahoo Finance API in python

### Step 1: Import all necessary python libraries.

In our example I will use two python modules one is yfinance and pandas. Lets import all of them.

```
import pandas as pd

import yfinance as yf
```

### Step 2: Download the data from Yahoo Finance API
To download the data you have to use download() method . Inside the download method you have to pass the tickers(stock name) and date range. Date range is not necessary but for learning purpose I am setting date from last 60 days from the date of writing this post.

Execute the following code (yahoo finance python)

```
df_yahoo = yf.download('FB',
start='2020-09-15',
end='2020-11-15',
progress=False
```

It will start downloading the data for the Facebook Stock. Here you can see I am passing FB Facbook ticker with start and end dates. To keep compatibility with older versions, auto_adjust defaults to False when using mass-download.

Please note that you are able to download data since 1950.

The output of the above code contains time-series data with open,close e.t.c of Facebook Stock.

![image](https://user-images.githubusercontent.com/100597998/177763854-896deba4-c5f9-494c-9fcb-7da19b41f225.png)

## Other Features of Yahoo Finance API Python
The above example was simple implementation of Yahoo Finance API. You can also do many other things using it. Some of them are.

### Use of Multiple Tickers
You can also download two or more ticker simultaneously. Just pass the ticker as a list.

```
df_yahoo = yf.download(['FB',"AAPL"],
start='2020-09-15',
end='2020-11-15',
progress=False)
```
You will get Open,High,Low,Close e.t.c for each Symbol.

![image](https://user-images.githubusercontent.com/100597998/177763987-b607cda5-9a01-4c68-914a-8294fd1a2465.png)
