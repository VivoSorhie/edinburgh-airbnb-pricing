# Edinburgh Airbnb — Fringe Festival Pricing Analysis

**Who captures the revenue premium when 3 million festival-goers arrive, and who leaves money on the table?**

---

## The Setup

Every August, Edinburgh hosts the world's largest arts festival. Over 3 million tickets are sold across 25 days. Accommodation demand surges city-wide — and every Airbnb host has months of advance notice.

This project investigates a natural experiment: when a predictable demand shock arrives, which hosts adjust their pricing to capture the premium, and which don't?

## Key Findings

- **$3.08M+ left on the table** — a conservative, quality-adjusted estimate of the total revenue gap across Edinburgh's Airbnb market during the 2019 Fringe.
- **The Scaling Trap** — hosts managing 2–5 properties fail to price up at *higher* rates than single-property hosts, suggesting that intermediate scaling breaks manual pricing strategies before professional tools take over.
- **The Engagement Effect** — highly-reviewed casual hosts outperform low-engagement portfolio operators, proving that market participation beats portfolio size.
- **1,890 Fringe Specialists** — listings that only operate during the festival, identified through a strict availability filter (≥7 Fringe days, <3 baseline days), leaving millions uncaptured by ignoring event markups.

## Data

Source: [Inside Airbnb](http://insideairbnb.com/) — Edinburgh, scraped June 25, 2019 (via [Kaggle](https://www.kaggle.com/datasets/thoroc/edinburgh-inside-airbnb))

| File | Description |
|---|---|
| `listings.csv` | ~13,000 active listings with host, location, price, and review data |
| `calendar.csv` | Daily price and availability for each listing (June 2019 – June 2020) |
| `reviews.csv` | Review timestamps used to derive host activity tiers |

> **Note:** Raw data files are not included in this repo due to size. Download them from the source [here](https://www.kaggle.com/datasets/thoroc/edinburgh-inside-airbnb).

## Methodology

1. **Data Cleaning** — host tiers (single_property / small_portfolio / large_portfolio), activity tiers, price parsing
2. **Market Context** — neighbourhood distribution, room type mix, base price benchmarks
3. **Signal Verification** — confirming the Fringe creates a statistically significant, market-wide price uplift
4. **Pricing Gap** — measuring who adjusts pricing (and by how much) versus who flat-prices through peak demand
5. **Revenue Gap** — profiling excluded listings, ruling out data artefacts via diagnostic tests (host tenure, listing quality), and quantifying total market inefficiency

## Notebook

All analysis is contained in a single Jupyter notebook:

📓 **[`edinburgh_fringe_pricing_analysis.ipynb`](edinburgh_fringe_pricing_analysis.ipynb)**

The notebook is self-contained and designed to run in Google Colab or a local Jupyter environment. Simply upload the three required CSV files (`listings.csv`, `calendar.csv`, `reviews.csv`) to your runtime to execute the analysis.

## Tools

Python · pandas · NumPy · Matplotlib · Seaborn · Google Colab

## License

MIT
