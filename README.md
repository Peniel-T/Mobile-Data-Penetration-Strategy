# Mobile Data Penetration Strategy: Ashanti, Central, Western & Western North Regions, Ghana

A district-level geospatial analysis of where mobile data growth potential is highest across four regions of southern Ghana, built entirely from public data.

The project covers **99 districts** and a target population of about **25 million people**. It answers four practical questions:

1. Which districts have the highest potential for mobile data uptake?
2. Who are the customers, and how can they be segmented?
3. How should marketing be targeted by location?
4. How can the results be shared with a marketing team in a form they can actually use?

![Power BI dashboard](images/powerbi_dashboard.png)

## Key findings

- **Ashanti** is the top priority. It has the largest smartphone base (3.5M) and the largest working-age population (7.2M of 11.7M).
- **Central Region's coastal corridor** (Cape Coast, Elmina) is a dense, high-potential second market.
- **Western Region** scores lower overall (Priority 3), but its cocoa-belt districts are promising micro-markets with seasonal income peaks.
- **Western North** is a longer-term, lower-cost rural expansion opportunity.
- The working-age share is about 60 to 63% in every region, so regional size drives the priority order more than age structure does.

![District opportunity tiers](images/district_priority_map.png)

## Approach

### 1. Opportunity Score

Each district is scored on four equally weighted dimensions:

| Dimension | What it captures |
|---|---|
| Population size and density | Size of the working-age (15 to 64) customer base |
| Smartphone ownership | Device readiness |
| Educational attainment | Likelihood of productivity, e-commerce and social media use |
| Employment | Disposable income for data subscriptions |

Districts are then grouped into tiers:

| Tier | Score | Meaning |
|---|---|---|
| Priority 1 | Above 70 | Strong smartphone ownership, education and employment |
| Priority 2 | 40 to 70 | Moderate indicators, rising income potential |
| Priority 3 | Below 40 | Clear data gap, price-sensitive market |

### 2. Customer segments

Urban Professional, High School Graduate Worker, Rural Youth / Informal Worker, Cocoa Belt Entrepreneur, and Coastal / Tourism User.

### 3. Location-based marketing

Geo-fenced digital ads, a community agent network, seasonal and event-triggered campaigns, anchor-point Wi-Fi hotspots, and spatial micro-targeting using drive-time analysis to find "data deserts".

### 4. Sharing results

Interactive Power BI dashboard, ArcGIS Online / QGIS Cloud web map, StoryMap, automated Python/R geo-reports, and a WhatsApp bot for field teams.

## Data sources

| Dataset | Source | Year | Format / access |
|---|---|---|---|
| Population and Housing Census, district summary | Ghana Statistical Service (GSS) | 2021 | CSV / Excel, stats.gov.gh |
| Administrative boundaries (districts, regions) | GSS / OCHA HDX | 2021 | SHP, humdata.org |
| Educational attainment by district (15+) | GSS Census 2021 analytical reports | 2021 | PDF / Excel, stats.gov.gh |
| Employment status by district | GSS Census 2021 | 2021 | Excel, stats.gov.gh |
| Smartphone ownership / ICT access | GSS Census 2021, ICT module | 2021 | Excel, stats.gov.gh |
| Working-age population (15 to 64) by region | GSS Census 2021 | 2021 | Derived from census tables |
| OpenStreetMap road network, Ghana | OpenStreetMap contributors | 2024 | SHP / GeoJSON, geofabrik.de |
| Population density raster, Ghana | WorldPop / University of Southampton | 2020 | GeoTIFF, worldpop.org |

## Tools

| Tool | Purpose |
|---|---|
| QGIS 3.x | District boundary mapping, choropleth production, spatial joins |
| ArcGIS Pro / ArcGIS Online | Cartographic outputs, web map publishing, drive-time analysis |
| Microsoft Power BI | Interactive dashboard: education, employment, smartphone charts |
| Python (GeoPandas, Pandas, Matplotlib) | Opportunity score calculation, spatial data wrangling, chart generation |
| Microsoft Excel | Census data cleaning, opportunity score weighting, pivot analysis |
| Microsoft Word | Report compilation |

## Repository contents

```
.
├── README.md
├── report/
│   ├── Mobile_Data_Penetration_Strategy_Portfolio.pdf
│   └── Mobile_Data_Penetration_Strategy_Portfolio.docx
└── images/
    ├── powerbi_dashboard.png
    ├── district_priority_map.png
    └── study_area_map.png
```

## Limitations

This is a prototype built on public data.

- Smartphone ownership and usage were not validated through field surveys, and full drive-time modelling for all 99 districts was not run.
- The four score components are equally weighted by professional judgment. In a full project the weights would be calibrated against historical ARPU data.
- The 2021 census is the latest available but is several years old, so population growth and smartphone adoption have likely shifted.
- Without operator data (CDR, tower coverage, ARPU), the score relies on proxies rather than observed data use.
- Competitor presence by district is not accounted for.
- Analysis is at district level only. Community-level targeting would need higher-resolution data.

## Author

**Peniel Tenkoramah Twum**
GIS Data Analyst & Database / Information Management Professional
Accra, Ghana

## References

1. Ghana Statistical Service (2021). *Ghana 2021 Population and Housing Census: General Report.* Accra: GSS. https://statsghana.gov.gh
2. Ghana Statistical Service (2021). *2021 PHC District Analytical Reports: Ashanti, Central, Western and Western North Regions.* Accra: GSS.
3. OCHA Humanitarian Data Exchange (2021). *Ghana Administrative Level 2 Boundaries.* https://data.humdata.org
4. WorldPop (2020). *Ghana 100m Population Density Raster.* University of Southampton. https://www.worldpop.org
5. OpenStreetMap Contributors (2024). *Ghana Road Network Extract via Geofabrik.* https://download.geofabrik.de/africa/ghana.html
6. GSMA Intelligence (2024). *The Mobile Economy: Sub-Saharan Africa 2024.* London: GSMA.
7. National Communications Authority, Ghana (2024). *Quarterly Statistical Bulletin: Telecommunications.* Accra: NCA.
