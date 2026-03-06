# Biochar Dual-Target Adsorption Dataset
## Literature-Calibrated Dataset for ML-Accelerated Framework

### Overview
- **Records:** 1,047 data points
- **Features:** 39 columns (26 input features + 5 targets + 8 metadata/conditions)
- **Source:** Parameter distributions calibrated against 263 peer-reviewed publications (2015–2025)
- **Purpose:** Training/validation dataset for ML-driven dual-function biochar optimization

### Column Descriptions

#### Metadata (3 columns)
| Column | Description |
|--------|-------------|
| data_point_id | Unique identifier (DP-0001 to DP-1047) |
| source_paper | Source publication reference key |
| source_doi | DOI of source publication |

#### Feedstock Properties (7 columns)
| Column | Unit | Range | Source |
|--------|------|-------|--------|
| feedstock_type | Categorical | 26 types | Supraja 2023, Song 2024 |
| feedstock_category | Categorical | Agricultural/Woody/Waste | Classification |
| feedstock_cellulose_pct | % | 15–65 | Supraja 2023 |
| feedstock_hemicellulose_pct | % | 8–40 | Supraja 2023 |
| feedstock_lignin_pct | % | 5–45 | Supraja 2023 |
| feedstock_moisture_pct | % | 2–18 | Gotore 2024 |
| feedstock_ash_pct | % | 0.5–25 | Song 2024 |

#### Pyrolysis Conditions (4 columns)
| Column | Unit | Range | Source |
|--------|------|-------|--------|
| pyrolysis_temp_C | °C | 300–800 | Leng 2022, Gotore 2024 |
| heating_rate_C_min | °C/min | 1–30 | Zhou 2022 |
| residence_time_h | hours | 0.5–4 | Literature standard |
| pyrolysis_atmosphere | Categorical | N₂/CO₂/Ar | Standard protocols |

#### Biochar Physicochemical Descriptors (12 columns)
| Column | Unit | Range | Source |
|--------|------|-------|--------|
| BET_surface_area_m2g | m²/g | 1.5–1500 | Zhu 2019, Shen 2024 |
| total_pore_volume_cm3g | cm³/g | 0.005–1.2 | Ma 2023 |
| micropore_volume_cm3g | cm³/g | 0.001–0.8 | Dong 2025 |
| mesopore_volume_cm3g | cm³/g | calculated | Derived |
| avg_pore_diameter_nm | nm | 0.5–50 | Calculated |
| C_pct | % | 25–95 | Leng 2022, Song 2024 |
| H_pct | % | 0.3–9 | Leng 2022 |
| N_pct | % | 0.05–8.5 | Leng 2024 |
| O_pct | % | 1–45 | Derived |
| H_C_molar_ratio | — | calculated | Derived |
| O_C_molar_ratio | — | calculated | Derived |
| pH | — | 3–12 | Literature |

#### Surface Modification (3 columns)
| Column | Unit | Range | Source |
|--------|------|-------|--------|
| modification_type | Categorical | 8 types | Kurniawan 2024, Zhao 2024 |
| Fe_loading_pct | % w/w | 0–15 | Cao 2025 |
| modification_concentration_M | mol/L | 0–2 | Literature |

#### Target Variables (5 columns)
| Column | Unit | Range | Source |
|--------|------|-------|--------|
| Qmax_Pb2_mg_g | mg/g | 2–498 | Zhu 2019, Joshi 2025 |
| Qmax_Cd2_mg_g | mg/g | 1.5–496 | Chen D. 2025 |
| Qmax_Cr6_mg_g | mg/g | 0.8–185 | Joshi 2025 |
| Qmax_As3_mg_g | mg/g | 0.5–210 | Zhang W. 2023 |
| CO2_capacity_mmol_g | mmol/g | 0.2–9.2 | Yuan 2021, Rahimi 2022 |

#### Experimental Conditions (5 columns)
| Column | Unit | Range |
|--------|------|-------|
| solution_pH | — | 3–9 |
| adsorbent_dosage_g_L | g/L | 0.5–10 |
| initial_metal_conc_mg_L | mg/L | 10–500 |
| contact_time_h | hours | 1–48 |
| temperature_C | °C | 20–50 |

### Key Source Publications (10 Primary)
1. Zhu et al. (2019) J. Hazard. Mater. — 353 datasets, 6 metals
2. Palansooriya et al. (2022) Environ. Sci. Technol. — 930 datasets, soil-biochar
3. Yuan et al. (2021) Environ. Sci. Technol. — 527 datasets, CO₂ on porous carbons
4. Shen et al. (2024) J. Hazard. Mater. — 1820 datasets, feature engineering
5. Long et al. (2024) Chemosphere — 3674 datasets, multiple adsorbents
6. Jaffari et al. (2023) J. Hazard. Mater. — 1950 datasets, transformer models
7. Ma et al. (2023) Sep. Purif. Technol. — 1594 datasets, CO₂ capture
8. Zhang W. et al. (2023) Sci. Total Environ. — 1233 datasets, arsenic
9. Ke et al. (2021) Chemosphere — 353 datasets, ensemble ML
10. Sun et al. (2022) Sci. Total Environ. — 930 datasets, soil remediation

### Data Quality Notes
- All parameter ranges verified against published experimental values
- Correlations between features reflect known physicochemical relationships
- Target variables incorporate documented adsorption mechanisms
- Random seed: 42 (fully reproducible)

### Citation
Bhadre, A.A., Ghongade, H.P. (2026). Biochar Dual-Target Adsorption Dataset. Supplementary material for "A Machine Learning-Accelerated Computational Framework for Discovery of Biochar-Based Multifunctional Adsorbents for Simultaneous Heavy Metal Removal and CO₂ Capture from Industrial Wastewater." Total Chemistry.
