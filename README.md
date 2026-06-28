# Price, Poverty, and Superbugs: Modeling AMR Exposure Risk in Tondo, Manila

## Problem Statement

The World Health Organization considers antimicrobial resistance (AMR) one of the top global public health threats. Also known as "superbugs," AMR does not exist only in contaminated food and beverages resulting from unhygienic food-handling practices but it is also found in contaminated processing equipment, storage facilities in slaughterhouses, and animal waste. So far, it has caused an estimated 1.27 million deaths globally in 2019, with projections of up to 10 million deaths by 2050 if left unaddressed. This means superbugs pose a serious threat to modern medicine, making infections harder to treat and routine medical procedures considerably riskier.

On April 30, 2026, BS Public Health students from UP Manila released the results of a 2024 study titled **_"Sip or Skip?: Microbiological Assessment for Antimicrobial Resistant Bacteria in Beverage Contents, Containers, and Palm Swabs of Vendors in Tondo, Manila."_** The study involved vendor palm swabs, cup swabs, and separate tests of water, ice, and the beverages themselves. Results showed heavy contamination across samples, including bacteria capable of causing disease, spreading infection, and resisting commonly used antibiotics. Liquid samples registered bacterial counts above allowable limits for powdered beverages and potable water, indicating widespread microbiological contamination across commonly consumed drinks on the streets. 

WHO experts emphasize a "One Health" approach to reducing the impact of AMR, calling for coordinated action across sectors to improve hygiene practices. In that spirit, and as a requirement of the Data Engineering Pilipinas Cohort, this study aims to give the general public, policymakers, and concerned authorities a clearer picture of the _non-health_ factors that contribute to a person's susceptibility to AMR exposure. One factor that is often overlooked is income which is the specific gap this study addresses.

## Research Question

 **"*Among low-income street-food consumers in Tondo, Manila, how does the price gap between AMR-contaminated street-vended beverages and microbiologically safer alternatives affect their continued exposure to antimicrobial-resistant bacteria?*"**

### Causal Chain

```
Household income / daily food budget
        │
        ▼
Price gap (street drink vs. safer alternative)
        │
        ▼
Probability of choosing the cheaper, contaminated option
        │
        ▼
Cumulative AMR exposure over time (weekly/monthly servings consumed)
```

## Audience

This study is grounded in Tondo, Manila, since that is the population the underlying microbiological data was drawn from. Beyond Tondo, the simulation is intended for the general public living in similarly dense, low-income urban communities elsewhere in the Philippines who may face the same exposure dynamic due to price and income gaps. It is also intended as a reference tool for policymakers and local health officials weighing interventions (subsidies, vendor regulation, public water access) against the lived economic constraints of the communities they affect.

## Key Metric (KPI)

**Expected number of AMR exposure events per month**, as a function of:
- household income / daily food budget, and
- the price gap between street-vended beverages and a safer alternative.
## Likely Data Sources

| Data Needed                                        | Likely Source                                                                                                                                                                             |
| -------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Household income / poverty threshold, NCR          | Philippine Statistics Authority (PSA)<br>- https://psa.gov.ph/statistics/income-expenditure/fies<br>- https://psa.gov.ph/statistics/poverty                                               |
| Average daily wage, NCR/Manila                     | PSA<br>- https://psa.gov.ph/statistics/occupational-wages-survey                                                                                                                          |
| Price of safer alternatives (bottled water/drinks) | DTI Suggested Retail Price (SRP) Bulletin for Basic Necessities and Prime Commodities.<br>- https://www.dti.gov.ph/dti-consumer-space/dti-latest-srps-basic-necessities-prime-commodities |
| Price of street-vended palamig in Tondo            | No published dataset exists; requires direct fieldwork/observation or asking people from Tondo through social media                                                                       |
## Possible Final Dashboard

The study aims to produce an interactive simulation surfacing the key metric above. Core interactive elements:

- A slider for **price gap** between street drinks and the chosen safer alternative.
- A slider or selector for **income bracket / daily food budget**.
- Output: **estimated AMR exposure events per month**, updating live as inputs change.

The underlying logic is best described as an **economic decision / risk-exposure model**, not an epidemiological transmission model, since it traces a consumer choice mechanism rather than person-to-person spread.