# DCF Model

## Purpose of the code
- This script calculates the intrinsic value of a stock using the Discounted Cash Flow (DCF) model. The intrinsic value represents the present value of all future cash flows a company is expected to generate, discounted back to today's dollars. Investors use the DCF model to estimate the value of an investment based on its expected future cash flows.
 
## The DCF Model
- The Discounted Cash Flow model is a valuation method used widely in finance and investment. It calculates the value of a company, stock, or asset based on its future cash flows, adjusted or 'discounted' to reflect the time value of money. The DCF model assumes that a dollar received in the future is worth less than a dollar received today.

## How the Script Works
1. The script first fetches the company's cash flow statement using the Alpha Vantage API. It retrieves the free cash flow for the last fiscal year and estimates the growth rate of the free cash flow using the CAGR formula.
2. Next, it calculates the present value of future cash flows for the first five years, and the terminal value (the present value of all future cash flows beyond the five-year period).
3. The script then retrieves the balance sheet data to get the total debt and cash equivalents.
4. Using the overview function of the Alpha Vantage API, it obtains the number of shares outstanding.
5. Finally, the script calculates the intrinsic value of the stock by subtracting the total debt and adding cash equivalents to the sum of discounted cash flows, and dividing this by the number of shares outstanding.

## Packages Used
```python
import requests
import numpy as np
```

## Example Result
In our example, we use Apple Inc. (AAPL) as the target company for our DCF model.
We set the discount rate `DISCOUNT_RATE` to 0.1 or 10%. This rate is used to bring future cash flows back to present value, acknowledging that money today is worth more than the same amount in the future due to its potential earning capacity.

We also set the terminal growth rate `TERMINAL_GROWTH_RATE` to 0.02 or 2%. This is the rate at which we expect the company's free cash flows to grow indefinitely after our five-year projection period.

After running our DCF analysis with these parameters, we obtain an estimate of the intrinsic value per share for Apple Inc. The intrinsic value of the AAPL stock computed by this model is approximately $121.26.

Please note that this result is based on many assumptions and is only one of many possible outcomes. The actual future cash flows and the actual intrinsic value could be different based on various factors not included in this model.

Remember, this script is a tool for financial analysis and not a definitive guide to buy/sell decisions. Always do your research and consider seeking advice from qualified professionals before making investment decisions.

## Potential Limitations and Errors
- API Limitations: Alpha Vantage imposes a limit on the number of API calls that can be made within a certain period. For free users, this limit is typically set at 5 API requests per minute and 500 requests per day. Exceeding this limit may cause the API not to return the expected data, which can result in the script failing or producing inaccurate results.
- API Errors or Changes: The structure of the API response might change, or the API might return an error. Our script expects certain keys to be present in the API's response. If these keys are not included in the response due to an error or change on the API's side, a KeyError will be triggered, causing the script to stop.
