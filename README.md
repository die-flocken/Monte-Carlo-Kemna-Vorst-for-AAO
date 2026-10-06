# monte-carlo-arithmetic-asian-options
Written in C++ (at least C++20), uses Eigen (at least Eigen 3.4.0).
Code includes only the main class.
Self-financing delta hedging portfolio for arithmetic asian options, using Kemna Vorst geometric control variates method.
Additionally, antithetic variates are used to reduce variance.
Achieved portfolio value withing 9% of the option payoff on the Amazon (AMZN) stock price, for a year long option (1st Jan 2024 - 1st Jan 2025)
Simulation takes following parameters: 
final expiration time (double), number of simulation steps (int), number of simulations (int), risk-free interest rate (double), volatility (double), strike price (double), initial stock price (double), vector of real stock prices over the testing period (Eigen::RowVectorXd), seed (unsigned long long).
Main method sim_run() returns the final portfolio value.

As is, only works with a full list of real stock prices, but can be easily modified to take incoming prices.
