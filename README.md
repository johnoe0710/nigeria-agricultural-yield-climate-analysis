# Nigeria Crop Yield & Climate Analysis (2000–2024)

An end-to-end Power BI analysis of Nigeria's national crop production, land use, and yield trends against a regional rainfall proxy, 2000–2024. Built to demonstrate a full analytical workflow — data sourcing, cleaning, modeling, DAX, and dashboarding — not just a finished dashboard.

## Screenshots

The project includes the final dashboard screenshots in `05_images/`:

- `01-dashboard-overview.png`
- `02-yield-trend-analysis.png`
- `03-rainfall-correlation.png`
- `04-model-relationship-view.png`

See [`05_images/README.md`](05_images/README.md) for the approved capture list and view guidance.

## Project Objective

This project describes **national-level** crop production, area harvested, and yield trends in Nigeria, alongside an **annual rainfall proxy covering a central band of the country**. It does not cover state- or zone-level food supply, and it does not include trade or import data — see [Limitations](#limitations) below.

## Repository Structure

```
Agriculture-Yield-Analysis-Project/
├── 01_raw_data/          Original FAOSTAT and NASA POWER CSV exports, unmodified
├── 02_cleaned_data/      The Power BI file (.pbix) — model, Power Query, DAX, dashboard
├── 03_analysis/          Supporting statistical notes (correlation coefficients, headline figures)
├── 04_report/            Executive Briefing & Business Insights Deck
├── 05_images/            Dashboard screenshots
├── 06_documentation/     Data dictionary, system architecture, user manual, ETL workflow
├── CORRECTION_LOG.md     Full history of corrections made to this project and why
├── DATA_SOURCES.md       Data provenance and licensing for both datasets
└── LICENSE               License for this project's own work
```

## Data Sources

- **FAOSTAT** (FAO) — national crop production, area harvested, and yield data for Nigeria, 2000–2024. Licensed CC BY 4.0.
- **NASA POWER** — precipitation reanalysis data (`PRECTOTCORR`), 2000–2024, covering a 143-cell grid over central Nigeria only. No usage restrictions; NASA requests acknowledgement.

Full attribution and citation text: [`DATA_SOURCES.md`](DATA_SOURCES.md).

## Tools

Power BI Desktop (data model, Power Query, DAX), Python (for the independent correlation calculation documented in `03_analysis/Analysis_Notes.md`).

## Key Figures

| Metric | Value |
|---|---|
| Total production, 2000–2024 | 3.82 billion tonnes |
| Total land footprint, peak year | 60.35 million hectares (2024) |
| Average yield growth, 2000→2021 | +10.0% |
| Yield-vs-rainfall correlation (blended, all crops) | r = 0.34 (n = 25 years) |

Full findings and methodology: [`04_report/Executive_Briefing_and_Business_Insights_Deck.docx`](04_report/Executive_Briefing_and_Business_Insights_Deck.docx).

## Limitations

- **National-level only** — no state or geopolitical-zone breakdown exists in the source data.
- **Partial climate coverage** — the rainfall data covers a 143-cell grid (7.5°N–12.5°N, 4.375°E–11.875°E), excluding the South-South, South-East, most of the South-West, and the far north. Every rainfall figure in this project describes that region, not the whole country.
- **No trade/import data** — this project cannot speak to the role of imports in Nigeria's food supply.
- **Correlational, not causal** — the yield-vs-rainfall relationship is descriptive. No significance testing or control for other variables (inputs, prices, policy) has been performed.

Full detail: [`06_documentation/Data_Dictionary_and_Field_Catalog.docx`](06_documentation/Data_Dictionary_and_Field_Catalog.docx).

## Reproducing This Project

1. Clone this repository.
2. Open `02_cleaned_data/Nigeria_Crop_Yield_and_climate_analysis_2000_2024.pbix` in Power BI Desktop.
3. If prompted on refresh, confirm the data source paths point to the `.csv` files in `01_raw_data/` in your local copy of this repository.
4. Refresh — should complete with no errors, landing on 793 crop-year records and 25 annual rainfall records.

## License

This project's own work (data model, transformations, measures, dashboard design, documentation) is licensed under the MIT License — see [`LICENSE`](LICENSE). The underlying datasets carry their own licenses — see [`DATA_SOURCES.md`](DATA_SOURCES.md).

## Author

John O. Ezekiel
