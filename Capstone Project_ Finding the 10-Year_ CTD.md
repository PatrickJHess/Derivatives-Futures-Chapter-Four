# **🎓 Capstone Project: Finding the 10-Year Note CTD**

**The Scenario:** The 10-Year Treasury Note futures contract  is the most liquid benchmark in the world. It's November 9, 2026 and the December 2026 delivery window for the 10-Year Treasury note contract (ZN) is approaching. The trading desk needs to know exactly what bond to buy in the cash market as a short against the contract.

Unlike the Long Bond basket we studied previously, the 10-Year contract has narrower eligibility rules: the CBOT requires delivered notes to have a remaining maturity of at least 6.5 years, but not more than 10 years, from the first day of the delivery month.

---

**Your Mission:** Using the tools in the `financial_quant` package and the arbitrage mathematics of this chapter, you must:

1. **Access the Bond Data:** You need to access the eligible bond data and current price data.  
2. **Calculate Total Invoice Price:** You need the settlement price on November 9, 2026, the conversion factors, and the accrued interest of the eligible bonds on the delivery date.  
3. **Calculate Forward Cash Prices:** Recall that the Forward Cash Price is the dirty price and the cost of carry (borrowing costs net of accrued coupons).  
4. **Determine CTD Note:** Calculate the Net Basis for each and find the minimum value. Recall that the Net Basis is the Forward Cash Price less the Principal Invoice Price.  
5. **Implied Repo And $\Delta^{min}_t$:** Use the current SOFR rate.  
6. **Demonstrate Alternative Bonds:** Determine the yield to maturity, duration, and convexity for the three bonds with the lowest Net Basis.

---

---

**Hints**

1. **Access the Bond Data:**  
   * Use `static_futures_data` to access the eligible bond data from `CME_Data_10Y_CTD_DEC_2026`.  
   * Use `FEDInvest` to access bond price data from FEDInvest  
   * Determine if any eligible bonds are missing in the FEDInvest data.  
   * Clean up the DataFrame.  
2. **Calculate Total Invoice Price:**  
   * Use FredReader to access SOFR Rate for the settlement day.  
   * Use the `timing_option` function of *Notes And Bond Futures* notebook to calculate necessary values.  
   * Use MASSIVEReader to get the settlement price.  
   * Get accrued interest on potential delivery dates.  
3. **Calculate Forward Cash Prices:**  
   * Forward Cash Price for first delivery date  
   * Forward Cash Price for last delivery date  
4. **Determine CTD Note:**  
   * Calculate Net Basis for the first and last delivery dates  
   * The minimum Net Basis of each bond is the optimal delivery date  
   * The CTD note has the lowest minimum Net Basis.  
5. **Implied Repo And \$\\Delta^{min}\_t\$:**  
   * Use SOFR and Net Basis of the CTD note  
6. **Demonstrate Alternative Bonds:**  
   * Create a DataFrame from the three bonds.  
   * Use the functions `create_payoff_df` and `calc_bond_metrics_2d`

:::{dropdown} 🔑 Here Is A Solution (Click to Expand)

```{include} Chapter_Four.md

:::
