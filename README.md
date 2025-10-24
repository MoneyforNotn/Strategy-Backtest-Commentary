
## Introduction

There is an ambiguous line between what can be confidently inferred from a backtest and what is simply a reflection of random market movements. The strength of a trend is best identified by various stress testing across broad datasets.

### Vision

The vision for this repository is to store a comprehensive annotated collection of analyzed trading systems, backtesting frameworks,  concepts, and ideas coded in Python Jupyter Notebook. Chapters in this repository cover various concepts, utilize multiple backtesting libraries, and employ several ways to validate testing. Most entry signals rely on price/volume indicators and measurable technical analysis.

 ***Why code it?***  
 Algorithmic trading (or backtesting) offers speed, precision, and consistency beyond human capabilities. Code is an invaluable tool for creating and combining indicators into easily adjustable entry signals and live visualization comparison of performance metrics/benchmark. 

### **Strategy concepts & trading ideas**


| Concept                 | Status                | Description, etc.                  |
|:------------------------|--------------------------------------------------------|---------------------|
| Mutli-asset |  | Backtest trading a universe of assets, 1% of equity, sl - Idea; (if not taking signals but holding and rebalancing) rank strenght of signal and buy one or few top ranked |
| Random Entry|   | Random entry & direction ... is it possible to beat the market with only good risk management (position sizing, atr sl) |
| Quantitative Momentum | | [The Quantitative Momentum Investing Philosophy](https://alphaarchitect.com/wp-content/uploads/2021/08/The_Quantitative_Momentum_Investing_Philosophy.pdf) by Jack Vogel, Ph.D. - ranks stocks by momentum and trend strenght, rebalanced quaterly |
| Year High or 100 Day High||Buy stock from a universe if reaches yearly high (250/100/other period lookback), sell at 10% gain|


### **Backtesting libraries & tools**


| Backtestesting tool                 | Documentation | Example         | Description                     |
|:------------------------|---------|--------------------------------------|---------------------------------|
| *numpy* (daily returns)              |         |  [tryyy](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/)| Storing data in arrays/matrices - calculating daily returns, benchmark drawdowns, strategy performance |
| backtesting.py      |  [kernc.github.io](https://kernc.github.io/backtesting.py/)     ||Popular Python framework for inferring viability of trading strategies on historical data |
| Backtrader     |[backtrader.com](https://www.backtrader.com/)   |                | Write an reusable trading strategies, indicators, performance visualization|
| VectorBT  |   [vectorbt.pro](https://vectorbt.pro/documentation/fundamentals/)                        | | Ability to combine multiple strategy instances into a single multi-dimensional array, enabling highly efficient data processing  |
| zipline        | [zipline-trader](https://zipline-trader.readthedocs.io/en/latest/backtest.html) |                                             | Backtesting/trading program compatible with Interactive Brokers and Alpaca |
| *build your own?* | | | Reliability, control, scale, independence,  |


### **Testing methods & approaches**


| Testing method                | Documentation | Example         | Description                     |
|:------------------------|---------|--------------------------------------|---------------------------------|
| Single-run automated        |   |  | python arrays/matrices - calculating daily returns, benchmark drawdowns, strategy performance |
| Multi-run optimization      |    |                    | Cross-parameter backtesting - allows for many tests with many entry signal combinations |
| Walk-forward                |   |                | Finding optimal *in-sample* trading parameters and checking the performance in the following time period for out-of-sample results |
| Monte Carlo simulations  |    |                                               | Helps assess strategy's robustness by randomizing simulation parameters & inputs (trade sequence, skip n trades) |
|         |    |                                             |  |
| *combination ?* | | | examine how the performance/robustness of a strategy changes across assets |



### **Indicators, signals, TA**


| Indicator                |  | Example         | Description                     |
|:------------------------|---------|--------------------------------------|---------------------------------|
| Volume |         |  | |
| Moving Average  |     |                    |  |
| RSI     |   |                |    |
| (A)TR |||
| MACD |||
| WVAP|||
| Bollinger Bands |||  
| PSAR |||




## Contributing
> [!IMPORTANT]
> This repository is in early stage of production, contribution etc. to be added 
Interested in imporovement ideas, feedback, contributions



## Credits 

While most work is authentic, some studies employ open-source code by online traders (all scripts are credited and accompanied by original author's license)  

Seperate file/folder to be designated for resources, learning paths, tools, references


# 𝕄𝕠𝕟𝕖𝕪𝕗𝕠𝕣ℕ𝕠𝕥𝕟



> "Absorb what is useful, discard what is not, add what is uniquely your own. 
>
> Bruce Lee

![alttt](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/develop/assets/sbc.image.ai.jpg)




### to-do
add:  
credits  
resources, references
 

performance metric table+links
Backtest tool table+links
Resources, useful learning paths, credits? 




