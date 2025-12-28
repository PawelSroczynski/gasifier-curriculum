# Research Sources

Reference materials for THRONE-GEMINI dual-phase biomass reactor design.

---

## Primary Inspiration: PyroFarm (Pyronet GmbH, Switzerland)

### PyroFarm P60 - Production Model (2024)

**Source:** `2024_Pyronet_Flyer_PyroFarm.pdf`
**URL:** https://www.pyronet.ch/pyrofarm/

| Parameter | Value |
|-----------|-------|
| Thermal output | 60 kW |
| Batch volume | 2 x 528 L = 1,056 L (dual container) |
| Pyrolysis temp | 400-650°C |
| Combustion temp | ~850°C (lambda-probe controlled) |
| Dimensions | L=5.3m, B=2.8m, H=2.5m (core) |
| Weight | 2,450 kg (core) + 605 kg (char storage) |

**Per-Batch Production:**

| Fuel Type | Burn Time | Fuel Mass | Heat Output | Biochar | CO₂ Sequestered |
|-----------|-----------|-----------|-------------|---------|-----------------|
| Pellets | 11 h | 330 kg | 660 kWh | 66 kg | 198 kg |
| Wood chips | 4 h | 125 kg | 250 kWh | 24 kg | 72 kg |

**Key Components:**
- A: Brennstoffbehälter (Fuel container / Pyrolysis reactor)
- B: Brennkammer (Combustion chamber @ 850°C)
- C: Wärmetauscher (Heat exchanger)
- D: Abgasgebläse (Exhaust fan - drives pyrolysis)
- E: Kohleabsaugung (Biochar vacuum extraction + moistening + grinding)
- F: Kamin (Chimney)

**Economics:**
- Heat cost: < 14 Rp/kWh (with biochar revenue 600-800 CHF/ton)
- Biochar value: 600-800 CHF/ton
- Target market: Agricultural operations

---

### PyroFarm 50kW - Development History (2017)

**Source:** `2017_Charnet_PyroFarm_Gutzwiller.pdf`
**Presenter:** Stephan Gutzwiller, Kaskad-E GmbH
**Event:** Charnet.ch Mitgliederversammlung, ZHAW Wädenswil, Feb 2017

**Development Timeline:**
- 2015: CHARday demonstration (heated swimming pool)
- 2017: 3 test prototypes, field testing
- 2020: First installation at organic farm in Stettlen (near Bern)
- 2021-2022: Testing phase
- 2023: Optimization
- 2024: Market-ready small series

**Price Point (2017):** ~25,000 CHF

**Swiss Pyrolysis Market Overview (2017):**

| System | Power | Price | Status |
|--------|-------|-------|--------|
| PyroCook | 3 kW | 650 CHF | 130 sold |
| PyroGrill | 4 kW | 1,500 CHF | Development |
| PyroFarm | 30-50 kW | 25,000 CHF | Field test |
| Biomacon | 60-500 kW | 75-300k EUR | Series (10 units) |
| Pyreg500 | 250 kW | 350-400k EUR | Series (25 units) |
| PyroPowerPlant | 150-1000 kW | 30k+ CHF | Field test |

---

### Design Inspiration Image

**Source:** `pyrofarm_50kw_inspiration.png`

CAD rendering of the PyroFarm 50kW dual-container swing-arm system showing:
- Two reactor vessels (fixed positions)
- Pivoting docking head with combustion chamber
- Heat exchanger above
- Steel frame structure
- Ash drawers below each reactor

---

## Biochar Applications (from Pyronet flyer)

### Soil Improvement
- Water retention in agricultural soils
- Nutrient buffer in specialty soils (peat replacement)
- Addite for compost, manure, slurry

### Disinfection & Hygiene
- Stable bedding (reduces pathogens)
- Water filtration
- Aquaculture water treatment

### Construction Materials
- Plaster addite
- Insulation material
- Concrete addite (sand replacement)
- Asphalt addite

### Feed & Food
- Livestock feed addite (methane reduction)
- Silage improvement
- Food supplement (E153 colorant)

### Odor Control
- Biogas plant filtration
- Stable bedding
- Slurry addite

---

## Regulatory Framework (Switzerland)

Two paths for approval:
1. **EN 303-5** - Heating boiler for solid fuels
2. **LRV Ziffer 74** - Agricultural biogenic waste combustion

Key requirements:
- Input: Natural, untreated wood only
- Heat utilization mandatory
- Biochar: EBC "premium" certification required
- Annual reporting to Federal Office for Agriculture

---

## Related Organizations

| Organization | Focus | URL |
|--------------|-------|-----|
| Pyronet GmbH | PyroFarm manufacturer | www.pyronet.ch |
| Kaskad-E GmbH | Original developer | www.kaskad-e.ch |
| Charnet.ch | Swiss biochar network | www.charnet.ch |
| Ithaka Institut | Biochar research | www.ithaka-institut.org |
| Verora GmbH | Biochar certification | www.verora.ch |
| Oekozentrum | PyroPowerPlant | www.oekozentrum.ch |
| Biomacon GmbH | Large-scale systems | www.biomacon.de |
| Pyreg GmbH | Industrial systems | www.pyreg.de |

---

## Climate Impact

**Per kWh of usable heat:**
- ~100g biochar produced
- ~280g CO₂ permanently sequestered
- Net effect: **Climate-positive heating**

IPCC recognizes biochar as one of the safest and most cost-effective Negative Emission Technologies (NET) since 2019.

---

## Relevance to THRONE-GEMINI

The PyroFarm design validates several THRONE-GEMINI concepts:

| PyroFarm Feature | THRONE-GEMINI Application |
|------------------|---------------------------|
| Dual containers | Enables continuous operation |
| Separate combustion chamber | Clean burn via staged combustion |
| Lambda-probe control | Optimal air/fuel ratio |
| Vacuum biochar extraction | Safe char handling |
| Batch operation | Fits state machine model |
| 400-650°C pyrolysis | Phase 1 temperature range |
| 850°C combustion | Validates gas burn temps |

**Key Extension:** THRONE-GEMINI adds Phase 2 (gasification at 800-1100°C) to produce syngas for engine fuel, whereas PyroFarm only performs pyrolysis for heat.
