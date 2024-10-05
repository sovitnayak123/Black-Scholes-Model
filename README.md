Black-Scholes Option Pricing Model 📈
This project demonstrates how to implement the Black-Scholes Model for option pricing in Python. The model calculates the theoretical price of European-style options using inputs such as the current stock price, option strike price, time to expiration, risk-free interest rate, and volatility.

Features
European Call Option Pricing: Calculate the price of a call option.
European Put Option Pricing: Calculate the price of a put option.
Greeks Calculation: Compute important metrics such as Delta, Gamma, Theta, Vega, and Rho to assess sensitivity to market factors.
Requirements
To run this project, you need to install the following dependencies:

NumPy: For numerical operations.
SciPy: For statistical computations (e.g., cumulative distribution functions).
Matplotlib: For visualizing the results.
Jupyter Notebook: To run and explore the code interactively.
You can install all the required packages using:

bash
Copy code
pip install numpy scipy matplotlib jupyterlab
Usage
1. Clone the Repository
bash
Copy code
git clone https://github.com/your-username/black-scholes-option-pricing.git
2. Open the Jupyter Notebook
Navigate to the project folder and open the Jupyter Notebook:

bash
Copy code
cd black-scholes-option-pricing
jupyter notebook Black-Scholes-Model.ipynb
3. Run the Notebook
The notebook will guide you through implementing the Black-Scholes Model step-by-step, including:

Pricing European Call and Put options.
Computing the Greeks for better insights into option price sensitivity.
Visualizing how different parameters affect option prices.
How It Works
The Black-Scholes Model uses the following inputs:

S: Current stock price.
K: Option strike price.
T: Time to expiration (in years).
r: Risk-free interest rate.
σ (sigma): Volatility of the underlying asset.
The formula for the Black-Scholes price is based on two key values: d1 and d2, which are used in the cumulative normal distribution functions.

Call Option Price = 
𝑆
𝑁
(
𝑑
1
)
−
𝐾
𝑒
−
𝑟
𝑇
𝑁
(
𝑑
2
)
SN(d1)−Ke 
−rT
 N(d2)
Put Option Price = 
𝐾
𝑒
−
𝑟
𝑇
𝑁
(
−
𝑑
2
)
−
𝑆
𝑁
(
−
𝑑
1
)
Ke 
−rT
 N(−d2)−SN(−d1)
Where:

𝑁
(
𝑑
1
)
N(d1) and 
𝑁
(
𝑑
2
)
N(d2) are the cumulative distribution functions of the normal distribution.
Example
Here is an example of how to use the code to calculate the price of a European call option:

python
Copy code
S = 100    # Current stock price
K = 100    # Strike price
T = 1      # Time to expiration in years
r = 0.05   # Risk-free rate
sigma = 0.2 # Volatility

call_price = black_scholes_call(S, K, T, r, sigma)
print(f"Call Option Price: {call_price:.2f}")
License
This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgments
Ryan O’Connell’s Step-by-Step Guide
Black-Scholes Model documentation and resources.
