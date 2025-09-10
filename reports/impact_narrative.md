# Impact Narrative — SDG 2/12/13 Focus
**Author:** George Odongo  |  **Date:** 2025-09-10  |  **Repo:** <https://github.com/coligny23/un-portfolio>

## 1) Context (≤100 words)
Food insecurity, post-harvest losses, and climate stress reinforce each other in Tanzania and across East Africa. While households face volatile food prices, edible produce is still lost along value chains due to handling, storage, transport, and market mismatches. Reducing loss and redirecting surplus can simultaneously advance **SDG 2 (Zero Hunger)** by improving access, **SDG 12 (Responsible Consumption/Production)** by preventing waste (Target 12.3), and **SDG 13 (Climate Action)** by avoiding emissions from decomposing organic waste. My contribution is a small, reproducible portfolio: open analyses of key indicators, a geospatial view of access constraints, and a pre-analysis plan for a low-cost behavioral/logistics pilot—packaged as briefs, dashboards, and code.
## 1.1) 2030 Agenda — Key Takeaways (UNITAR)
See detailed notes: [/reports/notes_unitar_fao.md]

## 2) Problem Signal (facts & trends)
**Common drivers of food loss/waste (SDG 12.3 context)**
- Post-harvest handling & storage gaps (spoilage, pests, moisture).
- Cold-chain & transport constraints (heat exposure, bruising, delays).
- Processing/packaging inefficiencies (spills, trimming, sub-optimal packaging).
- Grading & cosmetic standards (rejection by size/shape/appearance).
- Information/market mismatches (timing, price signals, distance to buyers).

*(Add 1–2 country-specific data points here once extracted in Anchor A.)*

## 3) SDG Alignment (concise)
- **SDG 2 — Zero Hunger:** improved availability/access via surplus redistribution.  
- **SDG 12 — Target 12.3:** prevent loss/waste across the chain; measure via FLI/FWI.  
- **SDG 13 — Climate Action:** avoided organic waste → reduced methane; resilience co-benefits.

## 4) Users / Beneficiaries
Smallholders, market vendors, low-income households, food banks/NGOs, municipal actors, and logistics partners who need low-cost, data-guided ways to move surplus to demand.

## 5) Proposed Contribution (what I will build)
- **Analytics:** “Food Insecurity Snapshot (TZ)” with clean, reproducible figures.  
- **GIS:** “Geospatial Barriers to Surplus-Produce Recovery” (travel-time/access).  
- **Experiment design:** PAP for an **SMS nudge/logistics info pilot**; power analysis.  
- **Outputs:** ≤600-word briefs, a lightweight dashboard, and public notebooks.

## 6) Indicators & Data
- **SDG 12.3.1(a) — Food Loss Index (FLI)** (FAO/FAOSTAT): % change in post-harvest losses.
- **SDG 12.3.1(b) — Food Waste Index (FWI)** (UNEP): kg/capita/year at retail, food service, households.
- **National total food waste (FWI-derived)**: population × waste rates by sector (contextual headline figure.

- **Core indicators:**  
  - **SDG 12.3.1(a) — Food Loss Index (FLI)** (FAO/FAOSTAT).  
  - **SDG 12.3.1(b) — Food Waste Index (FWI)** (UNEP, kg/capita/year).  
  - **SDG 2 linkers:** 2.1.1 Prevalence of Undernourishment; 2.1.2 FIES (context).  
- **Sources:** FAOSTAT, World Bank WDI, UNEP FWI, OpenStreetMap (markets/roads).  
- **Quality:** Document vintages, definitions; run sensitivity checks.

## 7) Methods & Ethics (one paragraph)
Use Python (pandas, matplotlib, statsmodels) for cleaning/visuals; QGIS for access maps; simple uncertainty bands where metadata allow. Pre-register the pilot’s analysis logic; label all assumptions and limitations. Handle only public or de-identified data; minimize PII, hash IDs, store securely. Adopt an “evidence, not certainty” stance and clearly separate description from causal claims.

## 8) Expected Outcomes (12-week horizon)
- **Near-term:** 3 briefs (Analytics, GIS, Pilot PAP), 1 public dashboard, reproducible notebooks.  
- **Use:** Strong evidence pieces for **UN internship** applications; a **PhD proposal** scaffold (research questions, methods, feasibility).  
- **Impact:** A prioritized view of where low-cost interventions could reduce waste and improve access.

## 9) Risks & Mitigations
- **Data gaps/consistency:** triangulate sources; annotate caveats.  
- **Over-interpreting correlations:** stick to design principles; run robustness checks.  
- **Adoption risk:** co-design briefs with prospective users; keep outputs practical and short.

## 10) Next Steps (dated)
- **Week 1–2:** Complete FAO Food Systems + Food Loss modules; draft **Anchor A** charts & ≤600-word brief.  
- **Week 3–4:** Build **Anchor B** access map (OSM + QGIS); publish brief and hotspot table.  
- **Week 5–6:** Write **Anchor C** PAP + power notebook; optional preregistration (OSF/AEA).  
- **Week 7–8:** Publish dashboard, integrate feedback, and submit UN internship applications.

---

### References (for footer use in briefs)
- FAO. FAOSTAT & Food Loss Index (12.3.1a).  
- UNEP. Food Waste Index (12.3.1b).  
- World Bank. World Development Indicators (SDG-relevant series).  
- UNITAR. *Introduction to the 2030 Agenda* e-course.
