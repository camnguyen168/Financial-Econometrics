# The Ego Empire: CEO Narcissism and Corporate Expansion

In Merge and Acquisition, Narcissism can be understood as the overconfidence of the executive, when they don’t make rational M&A decisions. Empirical research shows that most M&A deals deliver only small returns or negative long-run post-acquisition performance for acquirers. Prior research suggests that such characteristics significantly influence CEOs’ strategic decision-making and, consequently, organizational outcomes. 
This study will try to answer whether narcissistic executives more likely to pursue aggressive M&A activities, prioritizing size and status over operational efficiency.

We constructed a final panel dataset for regression analysis by joining the following sources:

  -Interview dataset: from this course Financial Econometrics

  -M&A outcomes: M&A transaction data ( Capital IQ - WRDS ), aggregated to firm–year.

  -Financial & Executive controls: Firm fundamentals ( Compustat - WRDS ), executive controls ( ExecuComp  - WRDS ).

The narcissism is calculated by using the word count in the CEO interview:

  $$SRR_ = \frac{\text{First-Person Singular}}{\text{First-Person Singular} + \text{First-Person Plural}}$$

## Methodology:
a panel dataset having narcissism proxies (normalized SRR), M&A “empire building” outcomes, firm financial controls, and CEO characteristics for regression analysis.

- TobinQ : growth opportunity, high growth opportunities firms are more potential to expand their size and do more deals.
- EBIT_Margin: Profitable firms (high EBITDA margin) have stronger internal funds for deals
- Leverage: high debt can limit new acquisitions.
- log_revt_lag: Sales power
- log_at_lag: acquiror’ total asset last fiscal year, Larger firms have more resources for M&A

- tenure_years, gender, age: influence risk tolerance and deal initiation; older/tenured CEOs may be more conservative
- shrown_excl_opts_pct: stock ownership
- log_stock_awards:  compensation package of CEO
- log_option_awards : compensation package of CEO

We build different regression model: Simple model, model with controls, models with controls and fixed effect
Industry * SRR : interaction term
Fixed effect : firm, sector, year

The full model is estimated using the following specification:

<img width="650" height="77" alt="image" src="https://github.com/user-attachments/assets/8541123b-afc2-40b7-a4fc-ebf7447e5785" />

where
- $i$ denotes the firm/individual.
- $t$ denotes the fiscal year.
- $\alpha_i$ and $\delta_t$ represent entity and time fixed effects respectively.
- $Controls_{it,k}$ represents the k-th control variable for firm/individual i at time t.
- $\epsilon_{it}$ is the error term.

## Result:


- According to our model transaction next year, we find a positive relationship between the level of CEO narcisism (SRR normalized mean and median) and the transaction size (significant at level 5%). The significance hold under 5% in single regression, muliple regression and also when putting fix effect to control for time invariant variables or when remove 0.1% outlier in the data


- The model same year regression and next 2 year regression show the relationship between SRR and transaction size is not significant

- SRR is statistical significant and positive associated with the acquisition activity next year


In the regression, we also find that some control factor are significantly with firm acquisition
Three variables emerge as highly significant predictors:
1. Organizational Scale: Lagged total assets (log_at_lag) confirms that a firm’s existing balance sheet capacity is the strongest anchor for future deal size or large firm are about to conduct more merge and aquisition 
2. Operating Efficiency: The EBIT_Margin shows a robust positive association. This suggests that highly profitable firms leverage their superior cash-flow generation to execute larger-scale acquisitions.
3. Growth Opportunities: Tobin’s Q remains a significant positive driver, indicating that firms with high market-to-book valuations—often interpreted as having a "mandate for growth"—consistently pursue larger targets.

Interaction effect of SRR and sector show that The coefficent is significantly more positive in `Industrials`, `Consumer Discretionary`, `IT`, `Communication Service`, `Real Estate`, `Healthcare`. As SRR increases, the change in transaction size is higher for Industrial, Comsumer Discretionary, IT, Real Estate and Healthcare than Energy as base Sector


The model demonstrates that traditional governance and demographic variables have negligible predictive power regarding transaction size
1. CEO Characteristics: Neither gender nor tenure_years impact the scale of transactions.
2. Compensation Structures: The magnitude of stock awards and option awards does not appear to incentivize larger deal tickets.
3. Capital Structure: Current leverage does not act as a statistically significant constraint on the following year's acquisition size.

Further Research:
just in short of time, this study still maybe has some limitation on merging the ceo data set, at this point it will need more further check to make sure that the data is merged correctly and consistently.






