# [kraken-api](https://github.com/fraff/kraken-api)

### Simple python client to kraken api with cool bash completion

1. Go to kraken and get some [api keys](https://support.kraken.com/hc/en-us/articles/360000919966-How-to-generate-an-API-key-pair-)
2. place keys in a safe place, ex: /run/user/$EUID/kraken
3. export KRAKEN_KEYS=/run/user/$EUID/kraken
4. source etc/bash_completion/kraken
5. test public method: ./krakenapi.py Time
6. test private method: ./krakenapi.py Balance (you can pipe it to [jq](https://github.com/stedolan/jq) to get a pretty output)
7. read https://www.kraken.com/features/api

ex:
* add a simple order:
    ```krakenapi.py AddOrder pair=xbteur type=buy ordertype=market volume=0.1```

* or a complex one:
    ```krakenapi.py AddOrder pair=xbteur type=sell ordertype=take-profit-limit price=50100 price2=50000 volume=0.2 "close[ordertype]=take-profit-limit" "close[price]=49000" "close[price2]=49100 starttm=3da<tab> expiretm=2w<tab>"```

> Remember, bash completion is cool.
