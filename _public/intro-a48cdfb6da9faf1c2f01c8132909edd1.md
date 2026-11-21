# Financial Python

## 📚 Volume: Futures Markets

## 📊Fixed Income Futures

This chapter examines four different fixed income contracts: **3-Month SOFR, 1-Month SOFR, Fed Funds, & U.S. Treasury Bonds**. The short-term contracts (three and one month SOFR and Fed Funds) are, like the stock index futures, settled with cash. Not so for Treasury futures; these contracts settle with physical delivery. The contracts address different markets and, by extension, different risks. The **3-Month SOFR** contract is pointed at the broad institutional short-term funding market—most notably the desire by corporations to lock in borrowing rates with interest rate swaps. The **1-Month SOFR** and **Fed Funds** contracts reflect the basic plumbing of short-term funds and the objectives of the Fed: the liquidity that facilitates government bond offerings. The **U.S. Treasury Bonds** contract and the related **T-Note** contracts capture the medium- to long-term cost of funding debt. As is true for the equity index contracts, together these instruments span much of the risk of the fixed income market.

### **📊 Short-Term Interest Rate Contracts: The 3-Month SOFR Futures**

The first fact documented is the long liquidity tenure of the **3-Month SOFR**. That is not an accident, but the result of post-2008 regulatory clearing requirements that fundamentally changed the economics of OTC swaps. Uncleared swaps are now capital-intensive and far less profitable to hold. The capital cost of bespoke interest rate swaps is diminished by clearing them at the CME, and further offset by hedging the cleared swaps with futures. The **3-Month SOFR** is the natural offset. 

### **📊 Short-Term Interest Rate Contracts: 1-Month SOFR and Fed Fund Futures**

You might expect these contracts to closely resemble the 3-Month SOFR, but they are actually very different. The 1-Month SOFR and Fed Funds contracts price as an average over a month; the 3-Month SOFR prices as a compounded value over three months. That difference is a big tell. The average measures the demand for short-term liquidity; compounding measures the cost of funding.

The 1-Month SOFR and Fed Funds rates are highly correlated and largely under the thumb of the Fed's machinations. SOFR's tether to Fed Funds is strong but not perfect. At times it varies, and when it does, it reflects the market's view of liquidity demands. The reasons vary from high or low Treasury offerings to seasonal tax payments. These contracts, and their divergence, effectively capture the risk of short-term funding stress.

### **🔄 Bonds and Notes: The Pivot From Cash Settlement to Physical Delivery**

The final notebook changes gears but not direction. The Bond and Note contracts rely on physical delivery—an innovation that allows them to cover a market less transparent than equity indexes, SOFR, or Fed Funds. Here, we return to the cost of carry equation developed in the last chapter. Much of our effort is directed toward understanding the required nuances of physical delivery and how they affect the use of the contract. Those nuances dramatically alter the minutiae of the calculation, but *not* the underlying cost of carry concept. Contract design requires that delivery options are granted to the short, and those options make the cost of carry a moving target. Nevertheless, we are able to corral the cash and futures markets, finding the arbitrage band t discussed in the previous chap

### **🎓 Capstone Project: Finding the 10-Year Note CTD**

Following up on the results of the *Bonds and Notes: The Pivot From Cash Settlement to Physical Delivery* notebook, this Chapter Capstone asks you to determine:

1. The CTD Treasury note for the December 2026 10-Year T-Note contract.  
2. The depth of the notes that are close substitutes for the CTD note.  
3. The implied repo rate and the minimum arbitrage band ($\Delta^{min}_t$).

This collaborative capstone exercise includes hints that guide you through the workflow. A clickable link provides a step-by-step solution that you can use to confirm your work.

### 🎯 The Jupyter Book Experience

Think of this Jupyter Book as a unique hybrid learning tool. It navigates like a modern website and reads with the narrative flow of an ebook, but packs the interactive computational power of Jupyter and Google Colab. By allowing you to manipulate real-world data and execute live code directly on the page, it seamlessly bridges the gap between abstract financial theory and applied modeling.

:::{dropdown} 🪐 How to Interact with Jupyter Books (Click to Expand)
:color: primary

```{include} jupyter_instructions.md
```
:::
