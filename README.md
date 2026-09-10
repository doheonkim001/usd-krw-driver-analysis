# How Did the Drivers of USD/KRW Change After Fed Tightening?

An independent research project analyzing whether the relationships between USD/KRW and major financial-market variables changed after the Federal Reserve began raising interest rates in March 2022.

## Motivation

I grew up in Hong Kong but traveled to Korea often to visit my relatives and friends. My grandparents would give me pocket money in won each time I visited. But because the Hong Kong dollar is pegged to the US dollar, the USD/KRW rate quietly determined what that money was actually worth by the time I got back to Hong Kong. I didn't think much of it as a kid, but it's probably where my interest in currencies started.

That interest became more concrete once I got to the US and started paying closer attention to FICC markets. My father works with fixed income, and conversations with him gave me an early, informal sense of how interest rates and currencies interact — enough to make me want to actually test the relationship rather than just take it on faith. 

I chose March 2022 as the dividing point because it marked the start of the Federal Reserve’s tightening cycle. The period after saw elevated USD/KRW volatility, repeated moves above 1,300, and broader won weakness, with USD/KRW later approaching 1,550. I wanted to determine whether interest-rate differentials became more strongly associated with USD/KRW after that shift — a relationship I had previously assumed but had not tested.

## Research Question

Did the factors associated with USD/KRW change after the Federal Reserve began tightening monetary policy in March 2022, and did changes in the U.S.–Korea three-year yield differential become more strongly associated with USD/KRW movements?

## Starting Hypothesis

The US–Korea three-year government-bond yield differential would become more important for USD/KRW after the Federal Reserve began tightening monetary policy.

## Data and Variables

The analysis uses monthly market data from January 2016 through August 2026. Weekly estimates are also used as a robustness check.

- **USD/KRW:** Korean won per US dollar
- **US–Korea 3-year yield differential:** US 3-year Treasury yield minus Korean 3-year government-bond yield
- **DXY:** Broad strength of the US dollar
- **VIX:** Global risk sentiment
- **USD/CNY:** Regional currency conditions

A positive change in USD/KRW means the dollar strengthened and the won weakened.

## Method

I divided the sample into two periods:

- **Pre-tightening:** January 2016 through February 2022
- **Transition month:** March 2022, excluded from the comparison
- **Post-tightening:** April 2022 through August 2026

I estimated standardized OLS regressions with HAC standard errors. I also tested lagged yield changes, influential observations, multicollinearity, and weekly-frequency results.

## Main Findings

- The expanded monthly model’s in-sample R² increased from approximately **40% before tightening to 70% after tightening**.
- DXY showed the strongest and most consistent post-tightening association with USD/KRW.
- USD/CNY also retained a meaningful association across specifications.
- The yield-gap change became significant after tightening in the main monthly model, but its coefficient was negative.
- Related evidence from lagged yield models weakened after correcting the sample boundary and removing influential months, while the contemporaneous yield-gap relationship disappeared at weekly frequency.
- VIX showed a clearer association before tightening and became weaker afterward.

## Conclusion

The results provide partial, but not robust, support for the starting hypothesis. The estimated relationship between interest rates and USD/KRW depends on the model specification and data frequency. Broad US-dollar strength and regional currency conditions provide more consistent explanations of post-tightening USD/KRW movements than the interest-rate differential alone.

These results describe conditional associations. They do not establish causality, estimate the won’s structural fair value, or guarantee out-of-sample predictive performance.

## Potential Extension

Foreign investors’ net purchases of Korean equities are a plausible omitted variable because cross-border transactions may create currency-conversion demand. Actual investor-flow data could be added in a future extension. KOSPI returns should not be treated as a direct substitute because stock-market performance does not measure foreign buying and selling.

## Notebook

The complete analysis, code, outputs, charts, and robustness checks are available in [`USD_KRW_Driver_Analysis.ipynb`](USD_KRW_Driver_Analysis.ipynb).
