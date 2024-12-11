# Quantitative Trading Notes

📕 Title: Quantitative Trading

👨‍💻 Authors: Ernest P. Chan

📚 Publisher: Wiley

🎯 Edition: 1st Edition

💾 Topics: Trading, Finance

📄 Pages: 204

## 📝 Table of Contents

- Ch1. The Whats, Whos and Whys of Quantitative Trading
- Ch2. Fishing for Ideas
- Ch3. Backtesting
- Ch4. Setting Up Your Business
- Ch5. Execution Systems
- Ch6. Money and Risk Management
- Ch7. Special Topics in Quantitative Trading
- Ch8. Conclusion: Can Independent Traders Succeed?

## 🛠️ Resources



## Preface

Why am I reading this book? Because I want to know *How to build my own algorithmic trading business*.

[WileyFinance.com](https://wileyfinance.com) for more books like this.

Can an individual with limited resources and computing power backtest and execute strategies over thousands of stocks and challenge the powerful industry participants? He can.

Who this book is for? Aspiring independent ("retail") traders who are looking to start a quantitative trading business.

This is a possible route to riches as well as intellectual accomplishment.

Having a profitable track record as an independent trader is an invaluable experience in itself. The experience forces you to focus on simple but profitable strategies, and not get sidetracked by overly theoretical or sophisticated theories. Most importantly, it forces you to focus on *risk management*.

What kind of background do you need?

Basic knowledge of statistics, familiarity with Excel. MATLAB or similar tools are also a great skill for backtesting.

What will you find in this book?

This is a book that teaches you how to find a profitable strategy yourself. This book teaches you:

- The characteristics of a good strategy
- How to refine and backtest a strategy to ensure it has good historical performance
- How to ensure that it will remain profitable in the future
- How to scale up or wind down strategies depending on their performance
- How to implement an automated execution system
- Basics of risk management
- Some psychological pitfalls to avoid

The focus of the book is in **statistical arbitrage trading of stocks**.

Steps to set up a quantitative trading business:

- Find a viable trading strategy
- Backtesting the strategy
- Setting up the business and technological infrastructure
- Building an automated trading system to execute the strategy
- Managing the money and risk involved in holding positions with this strategy

Then the book follows with important advanced concepts and how independent traders can find their niche and grow their business.

[Author's website](https://epchan.com/)
[Author's blog](https://epchan.blogspot.com/)

## Ch1. The Whats, Whos and Whys of Quantitative Trading

Quantitative trading or algorithmic trading, is the trading of securities based strictly on the buy/sell decisions of computer algorithms. The computer algorithms are designed and perhaps programmed by the traders themselves, based on the historical performance of the encoded strategy tested against historical financial data.

Algorithmic trading includes more than just thecnical analysis. Many traders incorporate fundamental analysis data. The important thing is that it's quantifiable.

### Who can become a quantitative trader?

Complex derivative instruments are not the focus of this book. This book focuses on **statistical arbitrage trading of stocks**, and one does not need an advanced degree to trade with these (stocks, futures, currencies).

It helps to have both a prior appreciation of risks and some savings to lean on. It is important not to have a need for immediate profits to sustain your daily living, as strategies have intrinsic rates of returns that cannot be hurried.

But also fear, the love of thrill and danger or an incredible self-confidence are dangerous emotions to bring to independent quantitative trading.

**Instant wealth is not the objective of quantitative trading.**

So the ideal quant trader is:

- Someone with prior experience with finance or computer programming
- Who has enough savings to withstand the inevitable losses and periods without income
- Someone whose emotion has found the right balance between fear and greed

### The business case for quantitative trading

Lots of people are in quant trading because it is exciting, intellectually stimulating, financially rewarding, etc.

But a quantitative trading business is very different from other small businesses

#### Scalability

Quant trading is very scalable up to a point. Scaling up often means only adjusting your leverage.

But quant trading is not a get-rich-quick scheme, you should hope to have small steadily increasing profits, instead of a 200% return a year that you could get with a SaaS or a software firm.

#### Demand on time

If you learn to automate your quant business it may take you very little time.

The author is in the middle in the automation spectrum and he describes his day like this:

- Before market opens: Run programs to download and process latest historical data
- Read company news
- Run programs to generate the orders for the day
- Launch a few baskets of orders before the market opens
- Launch a program that will put orders automatically throughout the day
- Update the spreadsheet which the previous day's P&L.

All this takes about 2 hours.

The urge to intervene manually is strong but is strongly disencouraged. Instead of just staring at your trading
screen, engage in more healthy activities.

You will also need to spend time doing research and backtesting new strategies.

**If you treasure your leisure time or if you need time and financial resources to explore other businesses, quantitative trading is the business for you**

#### The Nonnecessity of Marketing

Self-explanatory. Focus on the strategy and the software and not on selling to people.

#### The way forward

"When I first started as an independent trader, it took me only three months to find and backtest my first new strategy,
set up a new brokerage account with $100,000 capital, implement the execution system, and start trading the strategy. The strategy immediately became profitable in the first month."

## Ch2. Fishing for Ideas

Finding a trading idea is actually not the hardest part of building a quantitative trading business.

Increasingly, however, I have found that many strategies described by academics are either too complicated, out of date, or require expensive data to backtest.

(Ver Table 2.1 for sources of trading ideas)

You can find other sources of ideas in trading forums, sometimes these ideas may have worked only for a little while, or they work for only a certain class of stocks, or they work only if you don’t factor in transaction costs. However, the trick is that you can often modify the basic strategy and make it profitable.

[Wealth Lab](https://www.wealth-lab.com/)

Sharpe ratio: a measure that indicates the average return minus the risk-free return divided by the standard deviation of return on an investment.

*One of the best ways to gather and share trading ideas is to start your own trading blog.*

### How to identify a strategy that suits you

Working hours: Try to automate your strategies so that they run on autopilot and alert you only when problems occur.

Key factors:

- Your available time
- Your programming skills
- Your trading capital

In general, I would not recommend quantitative trading for an account with less than $50,000 capital. Let’s say the dividing line between a high- versus low-capital account is $100,000. Capital availability affects many choices.

With a low-capital account, we need to find strategies that can utilize the maximum leverage available.

Finally, capital (or leverage) availability determines whether you should focus on directional trades (long or short only) or dollar-neutral trades (hedged or pair trades).

Here, we just need to know that historical
stock data without survivorship bias are much more expensive than
those that have such a bias. Yet if your data have survivorship bias,
the backtest result can be unreliable. 
**Nota sobre esto de arriba, oportunidad de startup: historical trading crypto data without survivorship bias**

It seems that the only people I know who are willing and able to afford survivorship bias–free data are those who work in money management firms trading tens of millions of dollars.

**As long as you are aware of the limitations of your tools and data, you can cut many corners and still succeed.**

The more regularly you want to realize profits and generate income, the shorter your holding period should be.

**In reality, maximum long-term growth is achieved by finding a strategy with the maximum Sharpe ratio, provided that you have access to sufficiently high leverage.**

### A Taste for plausible strategies and their pitfalls

Quick checks you can do to a strategy before you invest time in thoroughly backtesting it:

- How does it compare with a benchmark and how consistent are its returns? (the benchmark is usually the market index to which the securities you are trading belong)

A strategy with good Sharpe ratio is better than a strategy with better returns because the one with a higher Sharpe ratio can be leveraged more.

If a strategy trades only a few times a year, chances are its
Sharpe ratio won’t be high. This does not prevent it from being
part of your multistrategy trading business, but it does disqualify
the strategy from being your main profit center.

If a strategy has deep (e.g., more than 10 percent) or lengthy
(e.g., four or more months) drawdowns, it is unlikely that it will
have a high Sharpe ratio.

**As a rule of thumb, any strategy that has a Sharpe ratio of less than 1 is not suitable as a stand-alone strategy.**

For a strategy that achieves profitability almost every month, its (annualized) Sharpe ratio is typically greater than 2. For a strategy that is profitable almost every day, its Sharpe ratio is usually greater than 3.

- How Deep and Long Is the Drawdown?

A strategy suffers a drawdown whenever it has lost money recently.

Then comes a complex mathematical formula to calculate the drawdown.

You have to ask yourself, realistically, how deep and how long a drawdown will you be able to tolerate and not liquidate your portfolio and shut down your strategy? Would it be 20 percent and three months, or 10 percent and one month? **Comparing your tolerance with the numbers obtained from the backtest of a candidate strategy determines whether that strategy is for you.**

- How Will Transaction Costs Affect the Strategy?

Everytime you buy or sell you incur a transaction cost. On top of that **when you buy and sell securities at their market prices, you are paying the bid-ask spread. If you buy and sell securities using limit orders, however, you avoid the liquidity costs but incur opportunity costs.**

Finally, there can be a delay between the time you place an order and the time it gets executed. This delay can cause a "slippage" *the difference between the price that triggers the order and the execution price*.

- Does the Data Suffer from Survivorship Bias?

Backtesting a strategy using data with survivorship bias can be dangerous because it may inflate the historical performance of the strategy.

Survivorship bias means not taking into account the stocks that have disappeared due to bankruptcies, delistings, mergers, etc.

- Does the Strategy Suffer from Data-Snooping Bias?

In general, the more rules the strategy has, and the more parameters the model has, the more likely it is going to suffer data-snooping bias. Simple models are often the ones that will stand the test of time.

The author goes on to say that he doesn't believe in complex AI algorithms that find small patterns work for financial markets, like they do for credit card fraud prevention and marketing.

For the author, an AI algorithm that could work in finance has these properties:

- They are based on a sound econometric or rational basis, and not on random discovery of patterns.
- They have few parameters that need to be fitted to past data.
- They involve linear regression only, and not fitting to some esoteric nonlinear functions.
- They are conceptually simple.
- All optimizations must occur in a lookback moving window, involving no future unseen data. And the effect of this optimization must be continuously demonstrated using this future, unseen data.

- Does the Strategy "Fly under the Radar" of Institutional Money Managers?

You should look for strategies with low *capacity* (that can't absorb millions of dollars) which fly under the radar of big firms.