# Advanced DCF Valuation Model

This project is a fundamental financial analysis tool built with Python and `yfinance` to calculate the intrinsic value of large-cap equities and determine if an asset is fundamentally overvalued or undervalued by the market.

## The Objective
To build a dynamic 5-year Discounted Cash Flow (DCF) model that automatically adjusts to real-time macroeconomic conditions. Instead of relying on static, hardcoded discount rates, this model programmatically engineers a live Weighted Average Cost of Capital (WACC) using the Capital Asset Pricing Model (CAPM).

## How It Works
1. **Dynamic WACC Calculation (CAPM):** Pulls the live 10-Year Treasury Yield (^TNX) to establish a risk-free rate, retrieves the target equity's real-time Beta, and calculates the precise Cost of Equity to dynamically discount future cash flows.
2. **Financial Data Ingestion:** Automatically aggregates real-time corporate financial statements (Free Cash Flow, Total Debt, Cash Equivalents, Shares Outstanding) via the Yahoo Finance API.
3. **Future Cash Flow Projection:** Projects Free Cash Flow 5 years into the future using conservative growth assumptions and discounts it back to Present Value using the dynamically calculated WACC.
4. **Intrinsic Value Calculation:** Calculates Terminal Value and Enterprise Value to derive the precise intrinsic value per share, outputting an automated pricing verdict (Undervalued vs. Overvalued) compared to the live trading price.
