We are simulating:
- 10 synthetic stocks
- 500 trading days
where all stocks are influenced by:
- one common market factor
- plus individual noise
This creates:
- correlated stocks
which is EXACTLY why PCA works later.

# The Model
We model synthetic stock prices using:
[
P_{i,t} = P_{i,t-1} \cdot \exp(\mu_i + \beta_i f_t + \epsilon_{i,t})
]
where:
### (P_{i,t})
Price of stock (i) on day (t).
### (\mu_i)
Small drift which represents the avg growth tendency
Typically chosen as a very small positive value.
### (f_t)
Common market factor affecting all stocks simultaneously.
This represents overall market movement.
If the market rises or falls, many stocks tend to move together because they are influenced by the same latent factor.
### (\beta_i)
Sensitivity of stock (i) to the market factor.
Higher (\beta_i) implies stronger reaction to market movements.
### (\epsilon_{i,t})
random noise specific to stock (i) independent of the overall market.

Because real financial markets are NOT independent.
Stocks move together due to:
- economy
- interest rates
- news
- market sentiment

This creates:
- covariance structure
which PCA later extracts.

# Why use libraries?
NumPy - for arrays, random number generation and matrix operations.
Pandas - for stock price tables - return calculations
Matplotlib - plots graphs
Seaborn - makes financial heatmaps(data visualization technique that uses spectrum of colors to represent density of data) looks cleaner.
- heatmaps make hidden relationship structure visually obvious

# Market_factor
represents the overall market movement.
because all stocks use this inside price eqn, when market rises, mny stocks rise together, when market crashes, many stocks fall together, creates covariance stucture.
PCA later tries to dicover this hidden common factor from returns.

# Why log returns
log - additive over time, closer to normal distribution, commonly used in stochastic modelling.
Here it gives 499 X 10 matrix which later becomes the PCA input

# correlation matrix 
- measures relationship strength
if value - +1 -> perfectly positively related
if -1 -> negatively related
- gives normalized relation
- diverging map

# Covariance matrix
measured joint variability
larger covariance - stronger co-movement
gives actual variance structure.
PCA internally uses covariance structure.
- magnitude map

