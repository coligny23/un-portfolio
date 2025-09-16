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

## Limitations
POU relies on modeled estimates subject to revisions; CPI is overall (not food-only). National aggregates hide sub-national heterogeneity; no causal identification is attempted here. Treat these as **context indicators** to guide where/when to test practical solutions.

---

## Artifacts
- **Notebook:** `/notebooks/10_anchor_a_ingest.ipynb`  
- **Figures:** `/assets/anchor_a_pou_ken-rwa-tza-uga.png`, `/assets/anchor_a_cpi_ken-rwa-tza-uga.png`  
- **Clean samples:** `/data/sample/wdi_sn.itk.defc.zs_ken-rwa-tza-uga_2000_2024.csv`, `/data/sample/wdi_fp.cpi.totl_ken-rwa-tza-uga_2000_2024.csv`

**References.** World Bank, World Development Indicators: *Prevalence of undernourishment (SN.ITK.DEFC.ZS); Consumer price index (FP.CPI.TOTL)*.

---

