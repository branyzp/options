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
- Scenario: Buying a call for AAPL for strike price $150, current price is $149. If the price shoots up to $155 before expiration date, the premium of the option contract will increase depending on many factors, but in easier terms it will increase by roughly $(155-149)x100= $600.
- Other factors that will affect the price of the option besides the strike price of the underlying stock are the Implied Volatility (IV), Days Til Expiry (DTE),

2. Put
- Gives the buyer the right to sell the underlying stock at a specified price by the expiration date
- Typically purchased when the stock price is expected to go down
- Scenario: Buying a put for AAPL for strike price $145 when the current price is $150, if the price falls to $140 before the expiration date, the premium of the option contract will increase depending on many factors, but likewise it will roughly increase by -$(140-150)x100 = $1000.
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

