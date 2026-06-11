# Retraction Watch - Global Retraction Analysis
## تحليل بيانات السحب العلمي العالمي

**By Dalia Kbar | Information Specialist & Data Analyst**  

---

## Overview | نظرة عامة

This repository presents a comprehensive bibliometric analysis of **70,121 retracted scientific papers** from the [Retraction Watch Database](https://retractionwatch.com/) - the world's largest curated dataset of retracted research.

The analysis covers retraction trends over time, geographic distribution by region and country, retraction reasons, journal and subject patterns, and time-to-retraction speed by nation. A key methodological contribution is the application of **fractional bibliometric counting**, ensuring fair attribution of retracted papers across multi-country collaborations.


---

## Key Findings | النتائج الرئيسية

1- Retraction surge post-2010: Annual retractions grew from <500/year before 2010 to a peak of 13,519 in 2023 - a 27× increase.

2- Asia-Pacific dominates: 66.5% of all retraction-linked papers. China alone accounts for 35,145 fractional credits (50.78%) - confirmed even after fair credit distribution.

3- Top reason - publisher-driven: "Investigation by Journal/Publisher" leads with 30,522 mentions (11.4%). Paper mills rank #7 with 11,738 mentions (4.4%).

4- Biology and Technology dominate by subject: Biology – Cellular #1 with 12,588 mentions (6.6%), followed by Technology (12,451) and Computer Science (9,158).

5- Publisher concentration: Top 15 publishers account for 75.4% of all retractions. Hindawi leads at 16.4%, followed by IEEE at 14.4%.

6- Most retractions involve multiple reasons: 78–86% of retracted papers cite 3 or more reasons. Asia-Pacific is highest at 86%; Europe lowest at 66%.

7- Regional retraction patterns differ: Latin America leads on publisher investigations (21%). Sub-Saharan Africa shows the highest data concerns (15%). North America has the most institutional investigations (7%).

8- Time to retraction is increasing: Average rose from ~1.3 years (1990) to 4.4 years (2026) - papers are taking longer to retract despite better detection tools.

9- Country retraction speed varies sharply: Japan takes the longest at 6.5 years average. Czech Republic and Australia are among the fastest at ~3.3 years. Global average is 4.2 years.

10- Psychiatry papers take longest by subject: Medicine – Psychiatry averages 13.3 years to retraction. Biology – Molecular and Medicine – Oncology retract fastest at ~3.1 years.

---

## Methodology | المنهجية

### Fractional Bibliometric Counting | العدّ الكسري البيبليومتري

This analysis applies **fractional counting** - a standard bibliometric method where each paper's credit is divided equally among all affiliated countries (1/n per country). This prevents data inflation from multi-country collaborations.

| Method | Total Credits | Use Case |
|--------|--------------|----------|
| Full counting | 87,775 country mentions | Measuring participation/presence |
| **Fractional counting** *(used here)* | 69,207 papers mapped | Measuring actual contribution |

**Example:** A paper with authors from China, USA, and Germany → each country receives **0.33 credits**, not 1.

> **Note:** 914 papers had no country data recorded in Retraction Watch and were excluded from all geographic analyses. These are not "unknown" countries - the field was simply not populated.

---

## Repository Structure | هيكلية المستودع

```
Retraction_Analysis/
│
├── README.md                          ← This file (EN + AR)
├── LICENSE                            ← MIT License
│
├── visualizations/                    ← All final charts (PNG, 180 DPI)
│   ├── 01_retractions_over_time.png       Retraction trends 1970–2026
│   ├── 02_fractional_dashboard.png        Regional & country breakdown
│   ├── 03_top20_reasons.png               Top 20 retraction reasons
│   ├── 04_top20_journals.png              Top 20 journals by retractions
│   ├── 05_top20_subjects.png              Top 20 subject fields
│   ├── 06_time_to_retraction_country.png  Country speed race (avg years)
│   ├── 07_multi_reason_regions.png        Simple vs complex by region
│   ├── 08_publisher_concentration.png     Publisher concentration analysis
│   ├── 09_reason_region_heatmap.png       Reason × region bubble grid
│   ├── 10_subject_reason_mosaic.png       Subject × reason Marimekko chart
│   ├── 11_reason_cooccurrence_network.png Chord diagram of co-occurring reasons
│   └── 12_top20_countries.png              
│   └── 13_time_to_retraction_country_detail.png
│   └── 14_time_to_retraction_subject.png
│   └── 15_average_time_retraction.png

                

│
├── data/                              ← Final processed CSVs only (no raw data)
│   ├── region_summary_final.csv           Region totals (full counting)
│   ├── country_summary_final.csv          Country totals (full counting)
│   ├── region_fractional.csv              Region totals (fractional counting)
│   ├── country_fractional.csv             Country totals (fractional counting)
│   ├── top20_reasons.csv                  Top 20 retraction reasons
│   ├── top20_journals.csv                 Top 20 journals
│   ├── top20_subjects.csv                 Top 20 subjects
│   ├── retractions_per_year.csv           Annual retraction counts 1970–2026
│   ├── time_retraction_country.csv        Avg years to retraction by country
│   └── time_retraction_subject.csv        Avg years to retraction by subject
│
└── LICENSE
```

---

## Visualizations Preview | معاينة المخططات

| Chart | What It Shows |
|-------|--------------|
| Retraction Trends | The post-2010 surge from <500/yr to 13,519 in 2023 |
| Fractional Dashboard | Asia-Pacific 66.5% · Europe 14.7% · North America 9.0% |
| Top 20 Reasons | Investigation by Publisher dominates at 11.4% |
| Publisher Concentration | Top 15 publishers = 75.4% of all retractions |
| Country Speed Race | Who retracts fastest - pure gradient by actual data |
| Reason Co-occurrence | Chord diagram showing which reasons cluster together |
| Subject × Reason Mosaic | Marimekko showing complexity by field |

---

## Data Source | مصدر البيانات

**Retraction Watch Database**  
- (https://retractiondatabase.org/) - maintained by the Center for Scientific Integrity  
- The raw dataset (`retraction_watch.csv`) is **not included** in this repository due to size and licensing. It can be uploaded directly from Retraction Watch.

**Region classification:** Pew Research World Regions framework

---

## Tools Used | الأدوات المستخدمة

| Tool | Purpose |
|------|---------|
| Python 3.x | Data pipeline, analysis, visualization |
| pandas | Data cleaning, transformation, aggregation |
| matplotlib | All visualizations (12 chart types) |
| numpy | Statistical calculations |

---

## License | الرخصة

Creative Commons Attribution 4.0 International License (CC BY 4.0)

Copyright (c) 2026 Dalia Kbar

This work is licensed under the Creative Commons Attribution 4.0 International License.

You are free to:
 • Share     - copy and redistribute the material in any medium or format
 • Adapt     - remix, transform, and build upon the material for any purpose,
                 even commercially

Under the following terms:
   •Attribution - You must give appropriate credit to the original author,
                   provide a link to the license, and indicate if changes were made.

                   Please cite as:
                   Kbar, D. (2026). Global Retraction Analysis.
                   GitHub: https://github.com/dalia-info95/Retraction_Analysis

   • No additional restrictions - You may not apply legal terms or technological
                   measures that legally restrict others from doing anything the
                   license permits.

Full license text: https://creativecommons.org/licenses/by/4.0/legalcode

─────────────────────────────────────────────────────────────────────────────

SCOPE OF THIS LICENSE

This license applies to:
  • All data files (*.csv) contained in the /data/ directory
  • All visualizations and charts (*.png) contained in the /visualizations/ directory
  • The README.md documentation file

This license does NOT apply to:
  • The underlying raw Retraction Watch dataset (retraction_watch.csv),
    which is the intellectual property of the Center for Scientific Integrity
    and subject to Retraction Watch's own terms of use.
    Source: https://retractiondatabase.org/

---

## Author | المؤلف

**Dalia Kbar**  
Information Specialist & Data Analyst  


💼 [LinkedIn](https://www.linkedin.com/in/dalia-kbar-8b0b641ba/)  
🐙 [GitHub](https://github.com/dalia-info95/Retraction_Analysis)

---
