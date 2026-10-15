# Spatial Analysis of Poverty Distribution in East Java

**Mapping regional poverty data with R and spatial visualization**

> An academic group project for the Data Science course, exploring the geographic distribution of the number of people living in poverty across East Java's 38 regencies and cities.

## 📌 Project Overview

This project uses R to combine administrative boundary data and regional poverty data, then displays the results on maps. The analysis moves from an Indonesia-wide administrative map to East Java and finally to a thematic map of poverty distribution.

**Focus:** Spatial data processing, data joining, and geospatial visualization  
**Tools:** R, `sf`, `tidyverse`, `ggplot2`, `ggspatial`, `ggsflabel`, `mapview`, and `viridis`

## 🎯 Objectives

- Visualize administrative boundaries in Indonesia and East Java.
- Combine East Java spatial boundaries with poverty data at the regency/city level.
- Explore geographic differences in the **number of people living in poverty**, using static and interactive maps.

## 🗺️ Visualizations

### 1. Poverty Distribution in East Java

![Poverty distribution in East Java](Images/3.%20Poverty%20Distribution%20in%20East%20Java.png)

The thematic map uses graduated colors to compare recorded poverty counts between regencies and cities. Darker shades indicate higher values according to the map's legend.

### 2. East Java Administrative Map

![East Java administrative map](Images/2.%20Spatial%20East%20Java.png)

Administrative boundaries for the 38 regencies and cities in East Java.

### 3. Indonesia Administrative Map

![Indonesia administrative map](Images/1.%20Spatial%20Indonesia.png)

An initial overview of Indonesia's regency/city administrative boundaries.

## 🔍 Analysis Workflow

1. **Load spatial and poverty datasets.** The original assignment uses a national administrative-boundary `sf` dataset (522 geographic features) and a poverty dataset covering 38 East Java regencies/cities.
2. **Filter East Java's boundaries.** Select administrative features identified as `Jawa Timur`.
3. **Prepare the maps.** Transform coordinate reference systems for tiled basemaps.
4. **Check administrative names and join datasets.** Match regency/city names, then use `full_join()` to associate poverty attributes with spatial features.
5. **Visualize the results.** Create static maps using `ggplot2` and `sf`, and an interactive map using `mapview` in the R Markdown analysis.

## 💡 Findings from the Original Assignment

The course report identifies darker-shaded regions—including Jember and Probolinggo—as areas with relatively high recorded poverty counts. It also calls attention to Bondowoso in its discussion. These observations are descriptive and should be interpreted using the exact reference year, measurement units, and legend of the underlying dataset.

**Important distinction:** The map presents the *number of people living in poverty*, **not** the poverty rate. A higher count does not necessarily mean a higher percentage of residents live in poverty.

## 📂 Repository Structure

```text
Spatial Analysis of Poverty Distribution in East Java/
├── Analysis/    # R Markdown analysis / scripts
├── Datasets/    # Source data
├── Images/      # Maps displayed above
└── README.md
```

## ▶️ How to Reproduce

Open the R Markdown analysis in `Analysis/` with RStudio. Install the packages used in the document, confirm the required shapefile components and poverty dataset are available in `Datasets/`, and **update the local file paths** in the original `.Rmd` before running it. The original coursework contains absolute Windows paths, so it will not run unchanged on a different machine.

## 👥 Project Credits

This project was developed as a **group assignment** for the Data Science course (2024) by:

- Jasmin Nur Hanifa
- Mufrih Nur Huda Tri Putra
- Nabiilah Rahmatiah Tangke

The repository presents the group's coursework as a portfolio case study; no individual division of work is claimed here.
