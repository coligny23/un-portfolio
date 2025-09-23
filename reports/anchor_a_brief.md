# Anchor A — Food Insecurity Snapshot (Tanzania & Neighbors)

**Question.** What do recent indicators suggest about undernourishment trends and price pressure in Tanzania relative to Kenya, Uganda, and Rwanda—and what are the immediate implications for SDG 2/12/13 workstreams?

**Why this matters (SDG 2/12/13).** SDG 2 focuses on access and availability; SDG 12.3 targets reduced food loss/waste; SDG 13 captures climate co-benefits from avoided organic waste. Tracking undernourishment alongside consumer price levels helps interpret affordability constraints and the urgency of loss-to-access interventions.

---

## Data & Methods
World Bank WDI (CSV bundles):
- **SN.ITK.DEFC.ZS** — *Prevalence of undernourishment (% of population)* (latest year in series: **2022**).  
- **FP.CPI.TOTL** — *Consumer price index (2010=100, overall CPI)* (latest year in series: **2024**).  

**Countries:** Tanzania (TZA), Kenya (KEN), Uganda (UGA), Rwanda (RWA).  
**Pipeline:** Cleaned with pandas, reshaped to long format, and plotted as simple lines; report latest values and 10-year / 5-year deltas.  
**Caveats:** National averages may mask sub-national disparity; 2020–2022 dynamics reflect COVID-19, weather, and methodological updates.

---

## Key Results (descriptive, non-causal)

### Prevalence of undernourishment (latest, 2022)
| Country | % of population |
|---|---:|
| Tanzania | **23.8** |
| Kenya | **34.5** |
| Uganda | **36.9** |
| Rwanda | **31.4** |

**Decade change (2012 → 2022, percentage points)**
- **Kenya:** **+15.6 pp** (18.9 → 34.5)  
- **Uganda:** **+14.5 pp** (22.4 → 36.9)  
- **Tanzania:** **+1.6 pp** (22.2 → 23.8)  
- **Rwanda:** **−4.2 pp** (35.6 → 31.4)

### CPI, overall (index 2010=100; latest 2024) & 5-year change (2019 → 2024)
| Country | Latest CPI | 5-yr change |
|---|---:|---:|
| Tanzania | **224.1** | **+19.6%** |
| Kenya | **257.4** | **+35.5%** |
| Uganda | **216.9** | **+23.2%** |
| Rwanda | **237.2** | **+57.0%** |

**Interpretation (short).**
- **Affordability pressure** rose across all four countries over 2019–2024—strongest in **Rwanda** and **Kenya**.  
- **Undernourishment** remains elevated; **Rwanda** shows modest improvement since 2012, **Tanzania** is roughly flat, and **Kenya/Uganda** worsened—underscoring the need for targeted, low-cost access improvements and **waste-to-access** pathways.  
- These signals justify piloting interventions that **shift edible surplus** to vulnerable consumers and MSMEs, while tracking SDG 12.3 loss/waste metrics.

---

---

## 12.3 Alignment 

**What we added today.** Household food-waste signals from the **UNEP Food Waste Index 2024** (city/district studies), plus an optional conversion to national **tonnes** using WDI population. These are **context** datapoints to complement POU/CPI; they are not nationally representative and should be read with care.

### Household Food Waste — Latest datapoint (kg/capita/year)
*Latest observation per country from the compiled studies; sub-national coverage varies.*

| Country  | Latest kg/cap/yr | Year | Study area (source) |
|---|---:|---:|---|
| **Tanzania** | **245** | 2023 | Iramba District (UN-Habitat 2023a) |
| **Kenya**    | **40**  | 2023 | Homa Bay (UN-Habitat 2023b) |
| **Uganda**   | **89**  | 2021 | Kampala (UNEP & UCPC 2021) |
| **Rwanda**   | **117** | 2023 | Musanze (UN-Habitat 2023c) |

> Note: The **Tanzania 245 kg/cap/yr** value is an **outlier** (rural district context) vs. Dar es Salaam studies (117–128). Use this as an *upper bound* until a national study is available.

### Household Food Waste — “Conservative” summary (median of the last ≤3 datapoints)
*Dampens single-site outliers; window reflects available years.*

| Country  | Median kg/cap/yr (≈) | Year window |
|---|---:|---|
| **Tanzania** | **128** | 2021–2023 |
| **Kenya**    | **55**  | 2020–2023 |
| **Uganda**   | **89**  | 2021 |
| **Rwanda**   | **140.5** | 2013–2023 |

### From kg/capita → tonnes (latest; order-of-magnitude)
Using **WDI population (SP.POP.TOTL)**, the notebook computes `tonnes_est = kg_per_capita × population / 1000`.

| Country  | Latest year | Estimated tonnes |
|---|---:|---:|
| **Kenya**  | 2023 | **2,257,318 t** (~**2.26 Mt**) |
| **Rwanda** | 2023 | **1,668,018 t** (~**1.67 Mt**) |
| **Uganda** | 2021 | **4,451,343 t** (~**4.45 Mt**) |
| **Tanzania** | 2023 | **1.679724e+07 t** (~**1.68 Mt**) |

**Implications.** Pairing these **FWI** signals with **POU/CPI** strengthens the case for targeted **waste-to-access** pilots (e.g., routing “imperfect” produce to low-income markets and MSMEs). Where the latest datapoint is an outlier (e.g., Tanzania), use the **conservative median** for planning and present both values transparently.

**New artifacts.**  
- `/assets/anchor_a_fwi_bar.png` *(kg/capita, latest)*  
- *(if population loaded)* `/assets/anchor_a_fwi_tonnes_bar.png` *(estimated tonnes)*  
- `/data/sample/unep_fwi_household_latest_kgcap_tza-ken-uga-rwa.csv`  
- *(if population loaded)* `/data/sample/unep_fwi_household_latest_tonnes_tza-ken-uga-rwa.csv`

---

## Limitations
POU relies on modeled estimates subject to revisions; CPI is overall (not food-only). National aggregates hide sub-national heterogeneity; no causal identification is attempted here. Treat these as **context indicators** to guide where/when to test practical solutions.

---

## Artifacts
- **Notebook:** `/notebooks/10_anchor_a_ingest.ipynb`  
- **Figures:** `/assets/anchor_a_pou_ken-rwa-tza-uga.png`, `/assets/anchor_a_cpi_ken-rwa-tza-uga.png`  
- **Clean samples:** `/data/sample/wdi_sn.itk.defc.zs_ken-rwa-tza-uga_2000_2024.csv`, `/data/sample/wdi_fp.cpi.totl_ken-rwa-tza-uga_2000_2024.csv`

**References.** World Bank, World Development Indicators: *Prevalence of undernourishment (SN.ITK.DEFC.ZS); Consumer price index (FP.CPI.TOTL)*.

---

