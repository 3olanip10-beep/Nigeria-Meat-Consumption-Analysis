# Nigeria's Meat Consumption Analysis | Power BI

## Project Overview

This project examines meat consumption patterns in Nigeria between 1990 and 2018, focusing on four meat categories: beef, pork, poultry and sheep meat.

Using Microsoft Power BI, I analysed consumption volumes, consumption per person and changes in demand over time.

My aim was to understand how Nigeria's meat market has evolved and how these patterns could inform decisions in the livestock and meat-processing industries.

I approached the analysis from the perspective of a Nigerian meat-processing company considering which product lines to investigate for possible expansion.

The project combines data analytics with my background in Animal Production and Health, allowing me to interpret the results from both an agricultural and a business perspective.

## Problem Statement

A Nigerian meat processing company wants to identify opportunities for expanding its operations.

Before investing in a new product line, management needs to understand which meat categories have the largest consumption volumes, which are growing fastest and whether national growth is also reflected in consumption per person.

This distinction is important because total meat consumption can increase as the population grows, even when consumption per individual declines.

The analysis therefore addresses four questions:

1. Which meat category had the highest consumption volume in Nigeria in 2018?
2. How did meat consumption per person change between 1990 and 2018?
3. Which meat category recorded the highest percentage growth in total consumption between 2013 and 2018?
4. Did total consumption and consumption per person follow similar trends?

## Tools and Technologies

**Microsoft Power BI**

- Power BI Desktop
- Power Query and data preparation
- DAX measures
- KPI development
- Data visualisation
- Time series analysis
- Comparative analysis
- Agricultural market analysis

## Dataset and Data Preparation

I imported `meat_consumption.csv` into Power BI and applied a page-level filter to focus specifically on Nigeria.

The dataset contains consumption data for different meat categories, years and measurement units.

Two units were particularly important:

- **THND_TONNE:** Total consumption in thousands of tonnes.
- **KG_CAP:** Consumption in kilograms per person.

Because both measures were stored in the same Value column, I used the Unit field and DAX measures to separate them for analysis.

I used:

- 1990-2018 for the historical consumption trends.
- 2018 as the main reporting year.
- 2013-2018 to compare more recent changes within the dataset.

## Dashboard Preview
The dashboard contains three KPI cards and four charts that explore national consumption patterns.

## Key Performance Indicators

| KPI | Result |
|---|---|
| Combined Meat Consumption (2018) | Approximately 1,251.6 thousand tonnes |
| Most Consumed Meat (2018) | Sheep meat |
| Fastest-Growing Meat by Volume (2013–2018) | Pork (+10.5%) |

These indicators provide a quick summary of the size of the four-category market, its largest product category and the strongest recent growth.

---

## Dashboard Analysis and Key Findings

### 1. Meat Consumption by Category in 2018

I compared the total consumption volume of beef, pork, poultry and sheep meat.

| Meat Type | Consumption (Thousand Tonnes) | Market Share |
|---|---:|---:|
| Sheep meat | 395.1 | 31.6% |
| Beef | 376.8 | 30.1% |
| Pork | 281.8 | 22.5% |
| Poultry | 198.0 | 15.8% |
| **Total** | **1,251.6** | **100%** |

**Key Findings**

- Sheep meat had the highest consumption volume at 395.1 thousand tonnes.
- Beef followed closely with 376.8 thousand tonnes.
- Pork accounted for 22.5% of the combined volume.
- Poultry had the lowest consumption volume among the four categories.

**Agricultural and Business Insight**

Sheep meat represented the largest category by volume in the 2018 data, suggesting that it would be worth investigating as a potential product line for a meat-processing company.

However, a large national market does not automatically guarantee profitability. Local demand, production costs, livestock availability and market access would need to be considered before investing.

### 2. Meat Consumption per Person (1990–2018)

I examined how consumption changed relative to Nigeria's population.

| Meat Type | 1990 (kg/person) | 2018 (kg/person) |
|---|---:|---:|
| Sheep meat | 1.52 | 1.77 |
| Beef | 1.50 | 1.35 |
| Pork | 0.88 | 1.12 |
| Poultry | 1.61 | 0.89 |

**Key Findings**

- Sheep meat consumption per person increased between 1990 and 2018.
- Pork also ended the period above its 1990 level.
- Beef consumption per person declined.
- Poultry recorded the largest decline between the two endpoints.

**Agricultural and Business Insight**

Changes in national meat consumption should not be interpreted using total volume alone.

Consumption per person provides another perspective on market demand and helps distinguish changes in overall consumption from changes in consumption relative to population size.

### 3. Changes in Meat Consumption Volume (2013–2018)

I calculated the percentage change in national consumption volume for each category.

| Meat Type | Volume Change |
|---|---:|
| Pork | +10.5% |
| Sheep meat | +5.4% |
| Poultry | +2.5% |
| Beef | −0.6% |

**Key Findings**

- Pork recorded the highest percentage growth in consumption volume.
- Pork consumption increased from approximately 255.0 to 281.8 thousand tonnes.
- Sheep meat recorded the second-highest percentage increase.
- Beef was the only category with a decline in total volume.

**Agricultural and Business Insight**

Pork's growth suggests that it is worth investigating as a potential expansion opportunity.

However, I would not recommend large-scale investment based on this trend alone. A company would need to understand the geographical markets, consumer preferences, product prices and supply conditions associated with this demand.

### 4. Total Consumption vs Consumption per Person (2013–2018)

I compared changes in total meat consumption with changes in consumption per person.

| Meat Type | Total Volume Change | Per-Person Change |
|---|---:|---:|
| Pork | +10.5% | −3.1% |
| Sheep meat | +5.4% | −7.5% |
| Poultry | +2.5% | −10.1% |
| Beef | −0.6% | −12.8% |

**Key Findings**

- Pork, sheep meat and poultry increased in total national consumption.
- All four meat categories experienced declining consumption per person between 2013 and 2018.
- Poultry showed a particularly noticeable difference between total volume growth and per-person consumption.
- Beef declined on both measures.

**Agricultural and Economic Insight**

One of the most important findings is that an increase in total national consumption does not necessarily mean that individual consumers are eating more meat.

This is particularly relevant for countries experiencing population growth.

Although the data shows these patterns, it does not contain the household income, prices or regional consumption information needed to determine their underlying causes.

---

## DAX Measures and Calculations

I created DAX measures to distinguish consumption volumes from per-person figures, calculate market shares and measure changes over time.

### Key DAX Measures

**Consumption (000 Tonnes)**

Uses `CALCULATE` to sum consumption values where the Unit field is `THND_TONNE`.

**Consumption (kg per person)**

Uses `CALCULATE` and `SELECTEDVALUE` to retrieve per-person consumption values from `KG_CAP` records.

**Total Meat Consumption**

Calculates the combined consumption volume of the four meat categories for the reporting year.

**Share of Four Meat Types**

Uses `DIVIDE` and `REMOVEFILTERS` to calculate each meat category's share of the combined volume.

**Most Consumed Meat**

Uses `TOPN` to identify the meat category with the highest consumption volume.

**Volume Change (%)**

Calculates the percentage difference in consumption volume between 2013 and 2018.

**Per-Person Change (%)**

Measures the percentage change in consumption per person over the same period.

**Fastest-Growing Meat**

Ranks meat categories according to their percentage growth in total volume.

These calculations helped transform the raw dataset into meaningful KPIs and visual comparisons.

## Dashboard Design and Features

The dashboard includes:

1. Three KPI cards showing combined consumption, the largest meat category and the fastest-growing category.
2. A horizontal bar chart comparing meat consumption volumes.
3. A line chart showing historical consumption per person.
4. A percentage-change bar chart comparing meat categories from 2013 to 2018.
5. A clustered bar chart comparing total-volume changes with changes in consumption per person.

A page-level filter was applied to focus the dashboard on Nigeria.

Each chart was designed to answer a specific question and support the overall analysis.

## Business and Agricultural Recommendations

Based on my analysis, I developed three main recommendations for a Nigerian meat-processing company.

### 1. Investigate Opportunities in Sheep Meat

I think the company should start by looking more closely at sheep meat because it recorded the highest consumption volume in 2018.

I would recommend speaking with local butchers, retailers and meat traders to understand which products and cuts are most frequently purchased.

I also believe working directly with local livestock farmers could help the company establish a more reliable supply while creating better market opportunities for producers.

### 2. Test Pork Products in Suitable Markets

Pork recorded the fastest growth in total consumption between 2013 and 2018.

I think the company could explore this opportunity through a small pilot in areas where pork is already regularly consumed.

Rather than immediately investing in a large processing facility, it would be more practical to work with a few retailers, test demand and assess whether customers make repeat purchases.

### 3. Consider Household Purchasing Power

One finding I consider particularly important is the decline in consumption per person across all four meat categories between 2013 and 2018.

I believe the company should investigate what households can afford before deciding on product sizes and pricing.

Speaking directly with customers and testing smaller packs or more affordable cuts could help determine which products best match local purchasing patterns.

## Limitations

This analysis is based on historical data ending in 2018 and should not be interpreted as a description of Nigeria's current meat market.

The dataset also lacks information on:

- Meat prices
- Household income
- Regional demand
- Production and supply costs
- Consumer purchasing preferences
- Market distribution channels

These variables would be important for evaluating the commercial feasibility of the opportunities identified.

The submitted report also identifies a chart-filtering issue: the chart titled as a 2018 consumption comparison displays accumulated historical volumes. This should be corrected in the Power BI report so that the visual matches the intended reporting year.

## Skills Demonstrated

Through this project, I demonstrated my ability to:

- Analyse agricultural and food consumption data.
- Develop DAX measures in Power BI.
- Compare historical trends across multiple categories.
- Distinguish national market volumes from per-person consumption.
- Build interactive analytical dashboards.
- Identify and communicate limitations in the available data.
- Translate agricultural data findings into practical business recommendations.
- Apply my Animal Production and Health knowledge to market analysis.

## Conclusion

The analysis identified sheep meat as the largest of the four meat categories by consumption volume in 2018, while pork recorded the fastest growth between 2013 and 2018.

At the same time, consumption per person declined across all four categories during the five-year comparison period.

These findings demonstrate why businesses should examine both total market size and per-person consumption before making investment decisions.

For me, this project was an opportunity to combine data analytics with my agricultural background and explore how evidence can support decisions across the livestock value chain.

It also strengthened my experience in Power BI, DAX, time-series analysis, dashboard design and communicating findings to a business audience.

## Author

**Olanipekun Joshua Tijesuni**

Data Analyst | Researcher | Agriculture

Interested in applying data analytics to agriculture, livestock production, animal welfare, food systems and business decision making.
