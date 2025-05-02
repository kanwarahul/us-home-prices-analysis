# US Home Price Analysis (2004–2024)

### Objective
Analyze key macroeconomic and demographic factors that influenced US national home prices over the last 20 years using publicly available data.

### Target Variable
- **S&P Case-Shiller US National Home Price Index** (from FRED)

### Key Features Used
| Feature                | Description                                      |
|------------------------|--------------------------------------------------|
| `cpi_rent`             | Housing-specific inflation                      |
| `material_cost_index` | Construction cost pressure (PPI)                |
| `median_income`       | Household affordability (from Census/FRED)      |
| `unemployment_rate`   | Indicator of economic health                    |
| `pop_growth`          | Demand-side demographic signal                  |
| `fed_funds_rate`      | Interest rate policy signal                     |

### Methodology
- Data sourced via FRED API and Census data
- Time series alignment and forward-filling where needed
- Feature engineering and trend normalization
- Modeling using:
  - **OLS Linear Regression** (Best Performer)
  - Random Forest
  - Ridge & Lasso Regression

### Final Model Results
- **Model**: OLS Linear Regression  
- **R² Score**: 0.935  
- **Key Drivers**:
  - `cpi_rent` and `material_cost_index` (strong positive influence)
  - `median_income` (affordability)
  - `unemployment_rate` and `pop_growth` (negative pressure)

### Visual Output
![Actual vs Predicted](visuals/actual_vs_predicted.png)

### Project Structure
- `/data`: All raw and cleaned CSVs
- `/notebooks`: EDA, modeling and data collection
- `/visuals`: PNG exports of key plots

### How to Run
1. Clone the repository  
2. Create a virtual environment  
3. Install dependencies:  
```bash
pip install -r requirements.txt
```
4. Run notebooks in order (`data_collection → eda → modeling`)

### Insights
- Housing prices are highly sensitive to inflation, material costs, and macroeconomic cycles
- Predictive modeling works best with interpretable, time-aware features
- Non-time-aware models like Random Forest failed to generalize

---
