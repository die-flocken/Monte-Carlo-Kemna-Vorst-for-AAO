# monte-carlo-arithmetic-asian-options
Written in Python, uses Numpy.
Code includes only the main class.
Self-financing delta hedging portfolio for arithmetic asian options, using Kemna Vorst geometric control variates method.
Additionally, antithetic variates are used to reduce variance.
Achieved portfolio value withing 9% of the option payoff on the Amazon (AMZN) stock price, for a year long option (1st Jan 2024 - 1st Jan 2025)
Simulation takes following parameters: 
final expiration time (int), number of simulation steps (int), number of simulations (int), risk-free interest rate (int), volatility (int), strike price (int), initial stock price (int), vector of real stock prices over the testing period (numpy row vector).
Main method f_test_recur returns the final portfolio value.

As is, only works with a full list of real stock prices, but can be easily modified to take incoming prices.