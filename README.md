# Life Insurance Pricing, Reserving & Financial Modelling Engine

## Actuarial Modelling Pipeline
### 01. Data & Assumptions

Mortality tables · Interest rates · Expenses · Lapse rates · Policy details


02. Data Processing

Validation · Cleaning · Policy preparation · Mortality interpolation


03. Pricing Engine

Net premium · Gross premium · Expense loading · Risk premium


04. Cash Flow Engine

Premium income · Death benefits · Maturity benefits · Expenses · Surrenders


05. Reserving Engine

Net Premium Reserve · Gross Premium Reserve · Prospective reserves · Retrospective reserves


06. Financial Modelling

Policy loans · EMI · Outstanding balance · Interest · Principal repayment


07. Sensitivity & Scenario Analysis

Mortality shocks · Interest-rate changes · Expense inflation · Lapse scenarios


08. Reporting & Dashboard

Excel reports · Python visualisations · Power BI dashboard


### 2. Recommended technology stack
Component	Technology
Main calculation engine	Python
Data manipulation	Pandas, NumPy
Actuarial calculations	SciPy
Statistical modelling	Statsmodels
Visualisation	Matplotlib, Plotly
User interface	Streamlit
Financial reports	Excel
Dashboard	Power BI
Version control	Git & GitHub
Testing	Pytest

VBA can be added later for Excel automation.

### 3. Folder structure
```
life-engine/
├── engine/          # core Python package
├── notebooks/       # 6 notebooks (theory, validation, analysis)
├── app/             # Streamlit app (imports engine)
├── data/            # life tables, synthetic portfolio, exported results
├── powerbi/         # .pbix file + screenshots
├── tests/
└── README.md
```
### 4. Development roadmap
 6 core notebooks plus 1 optional showcase. 

1. Life table and mortality: build lx, dx, qx, ex from a standard table, fractional-age assumptions, and (optionally) mortality improvement.
2.  APVs and premiums: commutation functions, term, whole life, endowment, annuities, and net and gross premiums.
3.  Reserves: prospective vs retrospective (showing they agree), recursive reserves, and surrender or paid-up values.
4.  Profit testing: cash flow projection, profit signature, IRR, NPV, break-even year.
5.  Sensitivity and scenarios: ±20% mortality, ±1% interest, lapse and expense shocks, with a tornado-style chart of which assumption matters most.
6.  Validation: reproduce textbook examples, with unit tests showing your results match to several decimals.
7.  Optional, advanced: multi-state Markov model, or Monte Carlo with stochastic interest.



Recommendation: Start with a simple 20-year term assurance product, annual premiums, annual benefits and an assumed mortality table. Complete pricing and reserving before introducing unit-linked products or complex stochastic models.
