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
Phase	What to build	Priority

1	Mortality data and assumptions	Essential

2	Term insurance pricing	Essential

3	Policy cash-flow projections	Essential

4	GPR and NPR calculations	Essential

5	Loan amortisation	Important

6	Sensitivity analysis	Important

7	Streamlit interface	Important

8	Excel and Power BI reporting	Later

## 5. It's a modular engine, not one giant Python file.

For example:
- premium.py calculates premiums.
- projections.py calculates future cash flows.
- reserves.py calculates reserves.
- amortization.py calculates loan schedules.
Each module should be independently testable.

Recommendation: Start with a simple 20-year term assurance product, annual premiums, annual benefits and an assumed mortality table. Complete pricing and reserving before introducing unit-linked products or complex stochastic models.
