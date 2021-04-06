# kraken-api

### simple python client to kraken api with cool bash completion

1. Go to kraken and get some api keys https://support.kraken.com/hc/en-us/articles/360000919966-How-to-generate-an-API-key-pair-
2. place keys in a safe place, ex: /run/user/$EUID/kraken
3. export KRAKEN_KEYS=/run/user/$EUID/kraken
4. source etc/bash_completion/kraken
5. test public method: ./krakenapi.py Time
6. test private method: ./krakenapi.py Balance
