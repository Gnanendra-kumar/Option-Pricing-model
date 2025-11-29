📈 Black-Scholes Option Pricing Model (Python)

This project implements the Black–Scholes Option Pricing Model in Python to calculate the theoretical prices of European Call and Put options using real stock market data.

The notebook fetches data from Yahoo Finance, computes volatility from log returns, and applies quantitative finance theory in practice.

🚀 Features

✅ Fetch real stock data using yfinance
✅ Compute log returns
✅ Estimate annualized volatility
✅ Implement Black–Scholes formula (Call & Put)
✅ Visualize stock price movements
✅ Clean financial mathematics in Python
✅ Beginner-friendly & extendable

📂 Project Structure
Black-Scholes/
│
├── Black_scholes.ipynb     # Main notebook
├── README.md              # Documentation

📦 Requirements

Install all dependencies:

pip install numpy pandas matplotlib yfinance scipy

▶️ How To Run This Project

Clone the repository:

git clone https://github.com/Gnanendra-kumar/Option-Pricing-model.git


Open the notebook:

jupyter notebook Black_scholes.ipynb


Run cells step-by-step.

📘 Black–Scholes Formula
📈 Call Option
<p align="center"> <b>C = S · N(d₁) − K · e<sup>−rt</sup> · N(d₂)</b> </p>
📉 Put Option
<p align="center"> <b>P = K · e<sup>−rt</sup> · N(−d₂) − S · N(−d₁)</b> </p>
📐 Where
<p align="center"> <b>d₁ = [ ln(S/K) + (r + σ² / 2) · t ] / ( σ · √t )</b> </p> <p align="center"> <b>d₂ = d₁ − σ · √t</b> </p>
📋 Parameters Explanation
Symbol	Meaning
S	Current stock price
K	Strike price
r	Risk-free interest rate
t	Time to maturity (years)
σ	Volatility
N(x)	Standard Normal Distribution CDF
📊 Core Functions
🔹 Volatility Calculation
def annual_vol(df):


Calculates annualized volatility using log returns.

🔹 Call Option Price
def call_option_price(S, K, r, t, sigma):

🔹 Put Option Price
def put_option_price(S, K, r, t, sigma):

🎯 Why Log Returns?

Log returns are used instead of simple returns because:

They are time-additive

More stable for variance calculations

Suit continuous compounding

Preferred in financial modeling

⚠️ Limitations of the Model

The Black–Scholes model assumes:

Constant volatility

No dividends

Efficient markets

European-style options only

No transaction costs

Real markets break many of these assumptions.

🧠 Learning Outcomes

By completing this notebook, you will understand:

✅ Option pricing fundamentals
✅ Financial volatility modeling
✅ Risk-free discounting
✅ Probability distribution usage
✅ Theory-to-code implementation

🙌 Built With

NumPy

Pandas

SciPy

Matplotlib

yFinance

👨‍💻 Author

Hrushi
Undergraduate Student
FinTech & Quant Enthusiast

📬 Want to Improve This?

You can extend the notebook by adding:

✅ Greeks (Delta, Gamma, Vega)
✅ Monte Carlo simulation
✅ Implied volatility calculator
✅ Strategy builder
✅ Interactive dashboard
