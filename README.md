# Trading bot - BINANCE - python - Docker

### This readme will be written in both Serbian and English.

## Kako koristiti - How to use

* Napravi rezultate testiranja za strategiju u određenom vremenskom intervalu. /<br>
* Create a backtest result based on some strategy for a ceratin time interval.
```
freqtrade backtesting --strategy <SampleStrategy> -i <time>
```

* Pokreni skriptu koristeći strategiju. /<br> Run a trade script using a strategy.
```
freqtrade trade --strategy <SampleStrategy>
```

* Preuzmi podatke o kripto valutama u prethodnih X dana u intervalu. / <br>
* Download data for crypto pairs in the last X days in a time interval.
```
freqtrade download-data --pairs ETH/BTC --days 5 -t 1h
```

* Preuzmi podatke o kripto valutama u prethodnih X dana u intervalu u nekom vremenskom periodu. / <br>
* Download data for crypto pairs in the last X days in a time interval in a certain time period.
```
freqtrade download-data --days 5 -t 1h (--timerange YMD(-YMD))
```

* Plotuj (napravi dijagram) podatke o nekom paru u nekom intervalu. / <br>
* Create a plotting diagram for certain pairs in a time interval.
```
freqtrade plot-dataframe --strategy SampleStrategy -p DOGE/USDT -i 1d --no-trades
```

* Napravi novu strategiju. / <br>
* Create a new strategy.
```
freqtrade new-strategy --strategy <NAME>
```

* Eksportuj podatke od backtest-a. / <br>
* Export data from backtesting.
```
freqtrade backtesting --datadir user_data/data/binance --export trades --stake-amount 25 -s BBandsRSI -i 15m
```

* Hiperoptimizacija za strategiju. / <br>
* Hyper-optimization for your strategy.
```
freqtrade hyperopt --hyperopt BBRSIHyperopt --hyperopt-loss SharpeHyperOptLoss --strategy BBandsRSI -i 15m
```

## Značenja - Meanings

stake amount
* unlimited sluzi u sustini za runovanje u testu <br>
* EN - used for running in test

dry_run_wallet
* ono sto imamo (ovo se deli sa max open trades) <br>
* EN - what we actually have (divided by max open trades)

ROI - return of investment <br>

```"minutes" = "profit"```

* Znaci npr. ako posle 1h imamo profit od 1%, prodaj
* EN - e.g. if after 1h profit is greater than 1%, sell

stoploss

* kada da proda ako smo na gubitku.
* EN - when to sell if we are losing.