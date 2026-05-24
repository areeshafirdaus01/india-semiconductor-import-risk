# India Semiconductor Import Risk Analysis (2013–2024)

Mapping India's structural dependency on South Korean semiconductor exports using UN Comtrade bilateral trade data.

## What this project does

- Tracks India's semiconductor imports under HS codes 8541–8542 across its top 5 origin countries: China (incl. Taiwan flows), South Korea, Singapore, Vietnam, and USA
- Quantifies Korea exposure including transshipment undercount via Vietnam and Singapore
- Models three disruption scenarios: 25% supply reduction, 30-day fab disruption, total supply chain failure
- Calculates a concentration index (Herfindahl-style) across import origins

## Key findings

| Metric | Value |
|---|---|
| Total semiconductor imports (2024) | $20.04B |
| Korea direct exposure (2024) | $3.69B |
| Concentration index (China + Korea + Singapore) | 96.0% |
| 30-day disruption cost (Korea) | $307.3M |

## Repository structure

```
├── data/
│   ├── TradeDataWhole_cleaned.xlsx   # Cleaned bilateral trade data
│   └── raw/                          # Original UN Comtrade exports
├── notebooks/
│   └── 02data_cleaning.ipynb         # Data cleaning and analysis
├── outputs/
│   └── dashboard.png                 # Final risk dashboard
└── brief/
    └── India-Korea Supply Chain Brief.docx  # Policy brief
```

## Data source

United Nations Comtrade Database — India semiconductor imports by origin country, HS codes 8541–8542, 2013–2024. Accessed May 2026. [comtrade.un.org](https://comtrade.un.org)

**Note on Korea exposure undercount:** UN Comtrade records flows by country of origin as reported by customs. Korean chips transshipped through Singapore and Vietnam appear under those origins, not Korea. The $3.69B bilateral figure is therefore a floor, not the ceiling.

## How to run

```bash
pip install pandas openpyxl jupyter
jupyter notebook notebooks/02data_cleaning.ipynb
```

## Author

BBA graduate building a geopolitical risk research portfolio. Previously at SBI (SME Finance Research). Open to analyst roles in trade policy, supply chain risk, and economic security.

Connect: [www.linkedin.com/in/areesha-firdaus1055]
