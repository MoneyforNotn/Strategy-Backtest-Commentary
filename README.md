![alt](develop/assets/stc.header.jpg)

## Introduction

There is an ambiguous line between what can be confidently inferred from a backtest and what is simply a reflection of random market movements. The strength of a trend is best identified through various stress testing methods applied across broad sets of data.

### Vision

The vision for this repository is to store a comprehensive annotated collection of trading systems, backtesting frameworks, strategy assessments, market theories, and ideas coded in Python Jupyter Notebook. Chapters in this repository cover various concepts, utilize multiple backtesting methods/libraries, and employ several ways to validate testing. Most trading systems are devised only from price/volume data indicators which are quantifiable, replicable, and can be measured.

 ***"Backtesting"***    
Backtesting is a technique used in trading and investing to assess the performance of a trading strategy or investment approach using historical market data. By applying specific predetermined rules and parameters, backtesting can offer traders valuable insights into profitability potentials, risks and constrains, and perfomance comparisons to alternative strategies.
 

  ***Why code it?***   
Algorithmic trading (and backtesting) offers speed, precision, and consistency beyond human capabilities. Code is an invaluable tool for defining and combining indicators into easily adjustable entry signals and creating live visualization comparison of performance metrics/benchmarks.  

## Project list
 > [!TIP]
> Find highlighted comments in every project for quick summary of concepts and analysis. Color scales indicate key findings, limitations, and improvements.

**Strategy-Backtest-Commentary**  
001-MA Crossover______Simple trend-following optimization aimed to reduce drawdowns tested on 30-year SPX daily data  
002-Random Entry______With robust risk-management and position sizing even random entries can be profitable (multi asset)  
003-London Breakout___Designed to capitalize on the high liquidity and volatility of the FOREX market during the London session  
004-Machine Learning__  
005-

### **Strategy concepts & trading ideas**


| Concept                 | Status                | Description, notes                  |
|:------------------------|--------------------------------------------------------|---------------------|
| Moving average optimization|[001-MA Crossover](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/001%20-%20MA%20Crossover%20Optimization.ipynb)| Can we validate entry parameters by optimizing across every relevant performance metric-theory, limitations  |
| Mutli-asset backtest|[002-Random Entry](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/002%20-%20Random%20Entry%20%22Coin%20Flip%22%20Strategy.ipynb)| Backtest trading a universe of assets, 1% of equity, sl - Idea; OR (if not taking signals but holding and rebalancing) rank strenght of signal and buy one or few top ranked |
| Random Entry|[002-Random Entry](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/002%20-%20Random%20Entry%20%22Coin%20Flip%22%20Strategy.ipynb)| Random entry & direction ... is it possible to beat the market with only good risk management (position sizing, atr sl) |
| Quantitative Momentum | | [The Quantitative Momentum Investing Philosophy](https://alphaarchitect.com/wp-content/uploads/2021/08/The_Quantitative_Momentum_Investing_Philosophy.pdf) by Jack Vogel, Ph.D. - ranks stocks by momentum and trend strenght, rebalanced quaterly |
| Year High or 100 Day High||Enter position (from a universe of assets) if price reaches yearly high (250/100/other period lookback), sell at 10% gain|
|London session breakout|[003-London Breakout](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/003%20-%20London%20Breakout%20FX%20Strategy.ipynb)|Capitalize on the London trading session’s high liquidity and volatility following price 'breakouts' (from the Asian session's high/low)|
| Break Out Indicator || Detect price break-outs by identifying trading range break-outs in combination with liquidity sweeps and n. of bars above/below MA|
||||

### **Backtesting libraries & tools**


| Backtestesting tool                 | Documentation | Example         | Description                     |
|:------------------------|---------|--------------------------------------|---------------------------------|
| *NumPy* (daily returns)  |  [NumPy guide](https://numpy.org/devdocs/user/index.html)    |  [001-MA Crossover](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/001%20-%20MA%20Crossover%20Optimization.ipynb)| Storing data in arrays/matrices - calculating daily returns, benchmark drawdowns, strategy performance |
| backtesting.py      |  [kernc.github.io](https://kernc.github.io/backtesting.py/)     |[001-MA Crossover](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/001%20-%20MA%20Crossover%20Optimization.ipynb), [002-Random Entry](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/002%20-%20Random%20Entry%20%22Coin%20Flip%22%20Strategy.ipynb), [003-London Breakout](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/003%20-%20London%20Breakout%20FX%20Strategy.ipynb)|Popular Python framework for inferring viability of trading strategies on historical data |
| Backtrader     |[backtrader.com](https://www.backtrader.com/)   |                | Write and reusable trading strategies, indicators, performance visualization|
| VectorBT  |   [vectorbt.pro](https://vectorbt.pro/documentation/fundamentals/)                        | | Ability to combine multiple strategy instances into a single multi-dimensional array, enabling highly efficient data processing  |
| zipline        | [zipline-trader](https://zipline-trader.readthedocs.io/en/latest/backtest.html) |                                             | Backtesting/trading program compatible with Interactive Brokers and Alpaca |
| *build your own?* | | | Reliability, control, scale, independence,  Possible starting point;[algotrading101blog](https://algotrading101.com/learn/build-my-own-custom-backtester-python/)   |
|||||


### **Testing methods & approaches**


| Testing method                | Documentation? | Example         | Description                     |
|:------------------------|---------|--------------------------------------|---------------------------------|
| Single-run automated        |   |  [001-MA Crossover](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/001%20-%20MA%20Crossover%20Optimization.ipynb)| Python arrays/matrices - calculating daily returns, benchmark drawdowns, strategy performance |
| Multi-run optimization      |    |   [001-MA Crossover](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/001%20-%20MA%20Crossover%20Optimization.ipynb)  | Cross-parameter backtesting - allows for many tests with many entry signal combinations |
|Out-of-sample            |   | [002-Random Entry](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/002%20-%20Random%20Entry%20%22Coin%20Flip%22%20Strategy.ipynb), [003-London Breakout](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/003%20-%20London%20Breakout%20FX%20Strategy.ipynb) |Measures the generalization erorr by testing model on unseen data to prevent/spot overfitting|
| Walk-forward                |   |                | Finding optimal *in-sample* trading parameters and checking the performance in the following time period for out-of-sample results |
| Monte Carlo simulations  |    |                                               | Helps assess strategy's robustness by randomizing simulation parameters & inputs (trade sequence, skip n trades) |
|         |    |          |  |
| *combination ?* | | | Examine how the performance/robustness of a strategy changes across assets |



### **Indicators, signals, TA**


| Indicator                |  | Example         | Description                     |
|:------------------------|---------|--------------------------------------|---------------------------------|
| Volume |         |  | |
| Moving Average  |     |    [001-MA Crossover](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/001%20-%20MA%20Crossover%20Optimization.ipynb), [003-London Breakout](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/003%20-%20London%20Breakout%20FX%20Strategy.ipynb)|Many traders use moving averages as the basis for a trend-following trading system as a confirmation signal to another indicator |
| RSI   |   |                |    |
| (A)TR ||[002-Random Entry](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/002%20-%20Random%20Entry%20%22Coin%20Flip%22%20Strategy.ipynb)|
| Market Sessions ||[003-London Breakout](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/003%20-%20London%20Breakout%20FX%20Strategy.ipynb)|
||||
| MACD |||
| WVAP |||
| Bollinger Bands |||  
|Price breakout||[003-London Breakout](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/003%20-%20London%20Breakout%20FX%20Strategy.ipynb)|
| PSAR |||
| Beta ||[002-Random Entry](https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/002%20-%20Random%20Entry%20%22Coin%20Flip%22%20Strategy.ipynb)|
||||

# EMH & Trading Philosophy

**Market Efficiency Theory** states that market prices tend to be perfectly reflective of all information in the market, implying that asset prices are always trading at their fair value. Thus, under a 'random walk' assumption, historical market and volume data have no value in predicting future stock prices. In other words, 'technical analysis' is useless and trying to time the market is a *loser's game*.

**Adaptive Market view** suggests market efficiency isn't fixed, but it evolves with competition, conditions, and who controls the volume. 

### **Leading conclusions & assumtions:**
 
> The movement of market prices is not always completely random

> Investor psychology, time-varying investor preferences, over-reaction, under-reaction, transaction costs, informational constraints, and even widespread use of similar trading systems contribute to this nonrandomness

> Trading systems can be developed to effectively exploit deviations from the random walk. Mechanical trading systems can be profitable, in part, because they are immune to greed and fear

> Over-reaction is more prevalent for some types assets and time frames (suitable for *mean-reversion* systems), and under-reaction  is more prevalent in others (*momentum* systems)

> There are different ways to characterize risk, including volatility measured by standard deviation and the probability of experiencing a drawdown of a given size

***
## Contributing
> [!IMPORTANT]
> This repository is in early stage of production, contribution etc. to be added (open to improvement ideas, feedback, contributions)

## Credits 

Though most work is authentic, some studies employ open-source code by online traders (all scripts are credited and accompanied by author's original license)  

*create seperate file/folder to be designated for resources, learning paths, tools, references

***
# 𝕄𝕠𝕟𝕖𝕪𝕗𝕠𝕣ℕ𝕠𝕥𝕟

> "Absorb what is useful, discard what is not, add what is uniquely your own"
>
> Bruce Lee

<p align="center">
  <img src="https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/develop/assets/sbc.image.ai.jpg">
</p>
<p align="center">
  <img src="https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/develop/assets/sbc.tapattern.png">
</p>
<p align="center">
  <img src="https://github.com/MoneyforNotn/Strategy-Backtest-Commentary/blob/main/develop/assets/sbc.wb.jpg">
</p>

> "As far as we can discern, the sole purpose of human existence is to kindle a light in the darkness of mere being"
> 
> Carl Jung

> Wholeness is not something you create, it is something you notice. It's the quiet realization that nothing is actually missing, now.


### develop notes
add:  
resources, learning tools references, credits    
hide unecessary outputs in .ipynb strategies  
revisit- Algotrading: Position size – devils game

credits/resrouces  
Youtube - The art of trading  
Youtube - Benjamin  
Youtube - Quantconnect  
Rapusa blog  
Youtube  - Moon Dev  
Algotrading101 blog  
Alpha Vantage   
Youtube – CodeTrading  
Youtube – Martin Bell  
Youtube - Neuralnine  
Youtube - Chad Thrackray  
Youtube - Lit Nomad  









