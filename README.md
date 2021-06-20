# OI-Trend-Indicator
=========================

Open Interest analysis provides significant insight into the strength of price action and momentum.

This script is based on the work done by Martin Pring in his book 'On Momentum'.

| # |Price         |       Volume           |          Open Interest      |           Market     |
|---|--------------|------------------------|-----------------------------|----------------------|
| 1 |Rising        |        Up              |           Up                |           Strong     |
| 2 |Rising        |        Down            |           Down              |           Weak       |
| 3 |Declining     |        Up              |           Up                |           Weak       |
| 4 |Declining     |        Down            |           Down              |           Strong     |

this table in turn, translates to:
Bullish :- An increasing Open Interest in a rising market. Buoyed by momentum of additional long positions
Bearish :- A declining Open Interest in a rising market. Lack of momentum
Bearish :- An increasing Open Interest in a falling market. Additional short positions being created
Bullish :- A declining Open Interest in a falling market. Existing positions are being exited and new money is poised to enter

With this as the base, we need to delve into the At The Money (ATM) Call and Put Open Interest values. 
Amongst all the strikes prices for a security, the ATM represents the most liquid, and probably most volatile price discovery point. A large chunk of the impending price movement can be guaged by observing the ATM OI activity.

A rise in ATM Call OI, represents a view that the sellers do not expect a price point to be crossed i.e. resistance. Similarly, a rise in ATM Put OI denotes a price acting as a support.

Consequently, one can deduce that when there is a pickup in OI trend, the probable direction of price movement can be determined.

| # |Call OI Trend   |    Put OI Trend   |   Probability of price movement                     |
|---|----------------|-------------------|-----------------------------------------------------|
|1  |Rising          |    Rising         |   Sellers in control. Narrow price range            |
|2  |Rising          |    Falling        |   Call sellers in control. Price tends to move down |
|3  |Falling         |    Rising         |   Put Sellers in control. Price tends to move up    |
|4  |Falling         |    Falling        |   Positions being exited. Narrow price range        |

With this is place, we will look to plot the OI trend using a Linear Regression Slope. When a change in trend is detected, it is indicative of an impending price movement

Screenshot (https://github.com/satishnarasimhan/OI-Trend-Indicator/blob/main/OITrend.png?raw=True)
