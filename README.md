# monte-carlo-arithmetic-asian-options
Self-financing delta hedging portfolio for arithmetic asian options, using Kemna Vorst method.
Additionally, antithetic variates are used to reduce variance.
Achieved portfolio value withing 9% of the option payoff on the Amazon (AMZN) stock price, for a year long option (1st Jan 2024 - 1st Jan 2025)
Simulation takes following parameters: 
final expiration time, number of simulation steps, number of simulations, risk-free interest raet, volatility, strike price, initial stock price, vector of real stock prices over the testing period.
Main method f_test_recur returns the final portfolio value.

As is, only works with a full list of real stock prices, but can be easily modified to take incoming prices.