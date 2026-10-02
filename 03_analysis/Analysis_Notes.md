% Analysis Notes — Supporting Computation
% Nigeria Crop Yield & Climate Analysis (2000–2024)

These are the exact computations behind every corrected figure in the Executive Briefing, Data Dictionary, and System Architecture documents, run directly against the live Power BI data model (not the raw CSVs, so they reflect the model's actual 793/25-row tables after cleaning).

## Headline Aggregates

- Total production, 2000–2024: **3,823,331,377 tonnes**
- Total area harvested by year: 2000 = 38,231,511 ha; 2021 = 58,238,286 ha; **peak = 2024 at 60,353,479 ha**
- Average yield (all crops, unweighted): 2000 = 3,970.7 kg/ha; 2021 = 4,368.1 kg/ha (**+10.01% growth**)

## Rainfall (Central-Grid Proxy, 25 Annual Values)

- Mean: 3.027 mm/day
- Minimum: 1.953 mm/day, **2004**
- Maximum: 5.724 mm/day, **2021**
- 2012 value (for reference against the retracted "2012 Collapse" claim): 3.447 mm/day — above the 25-year mean

## Yield-vs-Rainfall Correlation (Pearson r, n = 25 annual points)

| Crop | r |
|---|---|
| All crops, blended (unweighted average yield per year) | 0.335 |
| Maize (corn) | 0.441 |
| Rice | 0.121 |
| Wheat | 0.744 |
| Yams | −0.296 |

**Method:** annual average `Yield` per crop, joined to the annual central-grid rainfall average on `Year`, Pearson correlation coefficient. n = 25 for every crop with a full 2000–2024 reporting history in FAOSTAT; crops with gaps in their reporting history were excluded from the per-crop table above rather than estimated.

**Caveat:** 25 annual, spatially-partial data points is a small sample for any correlation claim. None of the r-values above should be read as statistically significant without a formal significance test, and none of this controls for other likely drivers of yield (fertilizer/input use, area under cultivation, commodity prices, pest and disease pressure). Treat these as descriptive associations, not evidence of a causal rainfall effect.

## 2012 Cereal Yield Check (against the retracted "12–15% synchronized contraction" claim)

| Crop | 2011 Yield (kg/ha) | 2012 Yield (kg/ha) | Change |
|---|---|---|---|
| Maize (corn) | 1,627.1 | 1,511.8 | −7.1% |
| Rice | 2,032.5 | 1,897.1 | −6.7% |
| Wheat | 1,279.1 | 1,018.9 | −20.4% |

None of the three cereals fall within the previously-claimed 12–15% range, and the three changes are not synchronized with each other or with the rainfall figure for that year.

---

*Computed 24 September 2026, directly from the model tables `FAOSTAT_data_en_5-16-2026` and `POWER_Regional_Monthly_2000_2024` via the pbix's underlying VertiPaq storage. Reproducible with any tool that can read the two model tables (e.g. Power BI's own DAX query view, or Python via a VertiPaq-model reader).*
