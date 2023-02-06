# Options (Beginner-Friendly Guide)

## Terms
### Bullish - belief that the stock price will go up
### Bearish - belief that the stock price will go down
### Premium - the price paid for an option contract, similar to insurance premiums being the price paid for insurance contracts, easier to use this term to refer to the price of options to avoid discrepancy between referring to strike price vs option contract price
### Strike Price - the price you can buy (in the case of a call) or sell (for a put) the underlying security before the contract expires.
### Intrinsic Value - value of an option if exercised today, calculated using the difference between the option strike price and current share price (value can be calculated)
### Extrinsic Value - difference between the option premium and and its intrinsic value, which consists of other factors beside calculable value, such as Time  (measured in DTE) and Implied Volatility (IV) which I will explain later
### In The Money - refers to when an option contract possesses intrinsic value

## Option 
A contract that gives the buyer the right to buy or sell a financial product at an agreed upon price for a certain period of time. 1 contract is equal to 100 shares, thus if the listed price is $0.64 for an option, it would be worth 0.64 x 100 = $64

## Types of options
1. Call
- Gives the buyer the right to buy the underlying stock at a specified price by the expiration date
- Typically purchased when the stock price is expected to go up
- Buying a call for AAPL for strike price 150 when the current price is 149. If the price shoots up to $155 before expiration date, the premium of the option contract will increase depending on many factors, but in easier terms it will increase by roughly (155-149)x100= $600.
- Other factors that will affect the price of the option besides the strike price of the underlying stock are the Implied Volatility (IV), Days Til Expiry (DTE),

2. Put
- Gives the buyer the right to sell the underlying stock at a specified price by the expiration date
- Typically purchased when the stock price is expected to go down
- Buying a put for AAPL for strike price 145 when the current price is 150, if the price falls to $140 before the expiration date, the premium of the option contract will increase depending on many factors, but likewise it will roughly increase by -(140-150)x100 = $1000.

- Likewise, other factors affect the price of the option similar to call options

## Factors affecting options premium

1. Underlying Stock Price
- The most important thing affecting options premium is the actual current market price of the stock vs the strike price

2. Time to Expiration (DTE)
- It is expected that with a longer period of time, there is a larger window for the price of the option to increase/decrease and thus there is a higher likelihood of uncertainty which increases option premium with a longer time period
- For example, buying a 0dte option (expires same day) may cost $10 but a yearly option with 365dte may cost $5500.

3. Implied Volatility (IV)
- Refers to the market’s forecast of likely movement of the stock’s price, based on predictive factors such as standard deviation over historical data and time periods
- Higher IV leads to option premiums to increase due to the anticipation that the stock price might likely shoot up or fall drastically in the near future
- Related: IV Crush refers to when purchasing an option in periods of high volatility e.g. GME stock price going from $50 to $500 in a matter of 2 weeks, the options premium skyrocketed due to expectations of volatile price shifts, but when the price calmed down back to $50 and remained at $50 for a period of time, IV decreases over time and the options premium will then shrink drastically with it

# Theta Wheel Strategy
This strategy utilises selling covered call and cash-secured put to generate returns through premiums

## Covered Call (CC)
- Selling call options with shares ready as collateral in the case of shares being called away (100 shares per 1 call contract sold)
- We will take a look at some scenarios to better understand
- I have 500 GME shares that I just bought at $20 cost price, current price is still $20, I can sell 5 Calls as I have 500 shares.
- I sell 5 weekly Calls at Strike Price $25 at premium of $0.60 per share, thus the calculation is done as such: 0.60 x 100 x 5 = $300 USD

1. Scenario 1: Sold Call expires worthless
- In 1 week, GME share price is at $24.99, it expires worthless as nobody would want a call contract that enables them to buy 100 shares of GME at $25 when the current price is at less than $25.
- I keep the $300USD
- Continue selling Covered Calls to continue earning $300USD/week until Scenario 2 happens

2. Scenario 2: Sold Call expires ITM
- In 1 week, GME share price is at $26, it expires ITM and my 500 shares are called away (buyer exercises call contract and takes my shares for $25/share)
- I “lose” the difference of the call contract strike price vs actual price ($25 - $26)
- But if you noticed, I bought shares at $20 so I actually managed to sell them for $25, in the end it’s a net profit of $5 per share PLUS I keep the option premium of $300 USD
- PROFIT = (TOTAL EARNED) - (TOTAL COST)
                    = ((25 x 500) + 300) - (20 x 500)
                    = 12800 -  10000 
                    = 2800USD
- Once our shares are called away, we now have $$$ cash instead of shares, so we will ‘rotate’ the wheel and move to the next step which is CSP

Also if you notice, both scenarios of CC result in net win for us.

Next,

## Cash-Secured Put (CSP)
- Selling put options with cash ready as collateral to buy in the case of assignment (forced to buy shares as part of the put agreement) and also refers to 100 shares per option contract same as call option
- Let’s continue the previous scenario after CC results in being called away
- I now have 12800USD, with GME price at $25 still
- I can sell 6 weekly CSP at $20 strike price as 600 shares of GME x 20 each is $12000 which is the max (if I sell 7, in the case of assignment of shares, 700 x 20 = 14000, I only have 12800 now so this is partially naked instead of cash secured)
- 6 weekly CSP at premium of $0.60 each is $360 USD
1. Scenario 1: Sold Put expires worthless
- In 1 week, GME stays >$20, expires worthless as nobody will want to sell GME cheaper than $20 if market price is >$20
- I keep the $360USD and rinse and repeat until Scenario 2 happens, slowly I can sell more and more contracts (6 -> 7 -> 8) as my base funds build up due to this strategy

1. Scenario 2: Sold Put expires ITM
- In 1 week, GME is at $19, I get assigned to buy 600 shares at $19 = $11400 cash is gone, so I still have 600 shares and $1400 remaining cash + $360 from the premium
- Now I can start selling Covered Calls again and 1 round of the wheel is completed, repeat


