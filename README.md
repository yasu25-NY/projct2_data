# TITLE  
**Can Japan’s Ports Compete on the Global Stage?**

---

## SHORT DESCRIPTION OF WHAT YOU AIMED TO ACCOMPLISH  
To examine how competitive Japan's ports are in the global supply chain.  
Given Japan's low self-sufficiency in both energy and resources, port strength is closely tied to the country’s economic and national stability.

---

## SHORT DESCRIPTION OF YOUR FINDINGS  
Despite local stakeholders claiming that Japanese ports are growing and even understaffed due to high demand, analysis revealed that they lag significantly in global competitiveness and logistics efficiency.  
Meanwhile, Busan Port in South Korea has recorded an impressive 13.5% growth in recent years, emerging as a highly advanced global hub.

---

## SUMMARY OF THE DATA COLLECTION PROCESS, WITH LINKS / OVERVIEW OF THE DATA ANALYSIS PROCESS  

This project followed a multi-stage process that involved data collection, spatial analysis, and final visualization through an interactive website.

### Python Notebooks  
- `scraping_TEU.ipynb`: Scraped TEU data from the World Shipping Council  
- `add_coordinates.ipynb`: Merged port coordinate data from Upply  
- `change_long.ipynb`: Reshaped the dataset into long-format for Flourish  
- `growthrate.ipynb`: Calculated port-level growth rate (2019–2023)

### Tools Used  
- **Python** (Pandas, BeautifulSoup)  
- **QGIS** (Geospatial processing)  
- **Mapbox GL JS + Scrollama** (Interactive mapping and storytelling)  
- **Datawrapper & Flourish** (Visualization tools)  
- **HTML/CSS** (Website creation)

### Datasets  
- `top_50_ports.csv`: Annual TEU data for the top 50 global ports  
- `port_namefull.csv`: Port names and coordinates from Upply  
- `top_50_ports_list.csv`: Merged TEU and coordinate data  
- `top_50_ports_long_corrected.csv`: Flourish-ready format  
- `japan1990.csv`, `japan2023.csv`: TEU data manually extracted from PDFs published by Japan Port Association  
- `port_growth_2019_2023_labeled.csv`: Re-aggregated dataset with growth rates  
- `wpi_port2.geojson`: GeoJSON of transit ports derived from World Port Index using QGIS  
- `busan.kml`: Used for visual verification of satellite imagery of Busan's new terminal

### Primary Data Sources  
- Upply (Port coordinates): https://opendata.upply.com/seaports  
- World Shipping Council: https://www.worldshipping.org/  
- NGA (World Port Index): https://msi.nga.mil/Publications/WPI  
- Japan Port Association: https://www.phaj.or.jp/distribution/sitemap/index.html

---

## WHAT YOU LEARNED  

- **Importance of Data Format Design**  
  One key takeaway was realizing how important it is to design your data structure with the final visualization tool in mind. It was a major setback to reformat everything for Flourish after initial cleaning.

- **Discovery of Geospatial Opportunities**  
  Although QGIS has a steep learning curve, its ability to handle spatial data opens up many compelling avenues for analysis.  
  Differentiating between standard ports and transit hubs visually added clarity to the final product.

- **Difficulties in Interactive HTML**  
  Even with a template, integrating Mapbox with Scrollama was a challenge. Interactive storytelling requires a deeper understanding of HTML/CSS and can be labor-intensive relative to its impact.

- **Effort vs. Impact**  
  Interactive visuals are powerful, but deciding where to invest your time and energy is key—especially when debugging complex interactions.

---

## WHAT YOU WANTED TO DO BUT COULDN'T  

- Collect and compare data on port congestion, trade volume, route shifts, and freight rates  
- Acquire more extensive historical TEU data (availability was limited)  
- Visualize live ship tracking data on the site (a goal for Project 3)

---

## SECURITY NOTES  
The Mapbox API token used in the HTML is protected via domain restriction to `https://yasu25-ny.github.io/*`, preventing misuse from outside sources.

---

## LINK TO PROJECT WEBSITE  
➡️ https://yasu25-ny.github.io/project_2/

## LINK TO ANALYSIS REPOSITORY  
➡️ [GitHub Repository with code & data](https://github.com/yasu25-ny/PORT_analysis) (replace with actual URL)

