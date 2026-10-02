# Data Sources & Attribution

Nigeria Crop Yield & Climate Analysis (2000–2024)

Both datasets in this project were obtained directly from their original, authoritative sources — no third-party redistribution platform is involved. Each carries its own license, reproduced below in full so this project can be shared, referenced, or built on without ambiguity.

---

## Dataset 1 — FAOSTAT Crop Production & Yield Data

- **Source:** Food and Agriculture Organization of the United Nations (FAO), FAOSTAT corporate statistical database
- **Portal:** https://www.fao.org/faostat
- **Domain:** QCL — Crops and livestock products
- **Coverage:** Nigeria, national level, 2000–2024, 31 crop items, three elements (Area harvested, Yield, Production)
- **File in this project:** `FAOSTAT_data_en_5-16-2026.csv`

- **License:** **CC BY 4.0** (Creative Commons Attribution 4.0 International), per FAO's current database Terms of Use (https://www.fao.org/contact-us/terms/db-terms-of-use). Attribution required; redistribution, adaptation, and commercial use are permitted. A small number of FAOSTAT domains carry third-party data with different terms — this does not apply to the QCL domain used here.

**Suggested citation:**

> Data source: FAOSTAT, Food and Agriculture Organization of the United Nations (FAO). Crop production, area harvested, and yield data for Nigeria, 2000–2024, obtained via the FAOSTAT web portal (https://www.fao.org/faostat). Licensed under CC BY 4.0.

---

## Dataset 2 — NASA POWER Surface Meteorology & Precipitation Data

- **Source:** NASA Langley Research Center (LaRC), Prediction Of Worldwide Energy Resources (POWER) Project
- **Portal:** https://power.larc.nasa.gov (Data Access Viewer)
- **Parameter:** `PRECTOTCORR` — bias-corrected precipitation, MERRA-2 reanalysis
- **Coverage:** 11 × 13 latitude/longitude grid (143 cells), 7.5°N–12.5°N by 4.375°E–11.875°E, monthly and annual, 2000–2024. *This grid covers central Nigeria only — see the Data Dictionary for the full coverage disclosure.*
- **File in this project:** `POWER_Regional_Monthly_2000_2024.csv`
- **License:** **No usage restrictions.** NASA data of this kind is a U.S. Government work and is not copyrighted. NASA requests, but does not require, an acknowledgement.

**Suggested citation (NASA's requested acknowledgement wording):**

> The data used in this project were obtained from the NASA Langley Research Center (LaRC) Prediction of Worldwide Energy Resource (POWER) Project, funded through the NASA Earth Science/Applied Science Program, retrieved via the POWER Data Access Viewer (https://power.larc.nasa.gov).

---

## This Project's Own Work

The data model, Power Query transformations, DAX measures, dashboard design, and all documentation in this repository are original work built on top of the two public datasets above. See `LICENSE` for the terms covering that original work.
