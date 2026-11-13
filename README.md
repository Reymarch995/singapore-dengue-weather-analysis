# Singapore Dengue, Weather and Population Analysis

Completed as coursework for the Diploma in Computer Engineering at Singapore Polytechnic and published with my lecturer's permission.

## Project background

I completed this project as part of my school coursework to explore a question: **How well do weather conditions and population density explain dengue activity in Singapore?**

Using public datasets from 2014 to 2018, I examined dengue trends and their relationships with rainfall, temperature, relative humidity and national population density. The project involved data cleaning, time-series aggregation, visualisation and correlation analysis in Python.

## Approach

- Cleaned five datasets and combined weekly dengue cases into monthly totals to match the weather data.
- Compared monthly dengue cases with weather in the same month and with weather one and two months earlier.
- Compared population density with annual dengue incidence per 100,000 people, keeping the population analysis at its original annual frequency.
- Used line charts, bar charts, a correlation heatmap and a scatter plot to interpret the results.

## Key findings

- Annual dengue cases in the analysis fell from **18,326 in 2014 to 3,283 in 2018**, a decrease of about **82%**.
- Same-month weather correlations were weak. The strongest tested weather relationship was temperature one month earlier, with a correlation of approximately **r = 0.27**.
- National population density increased by about **2.5%** over the period while dengue cases declined substantially. The annual density–incidence correlation was negative, but it was based on only five observations.

These results suggest that weather and national population density alone do not adequately account for the dengue patterns observed in this study.

## Limitations

This is an observational analysis: correlation does not establish causation. The population comparison contains only five annual observations, and national averages cannot capture differences between neighbourhoods. Weekly dengue counts are aggregated into monthly totals, which also limits the time precision of the comparison.

Other possible influences, such as mosquito levels, circulating virus types and vector-control activity, were not included in the numerical analysis. The full reasoning, charts and interpretation are available in the [notebook](dengue-analysis.ipynb).

## Contents

- `dengue-analysis.ipynb` — analysis and visualisations
- `dengue-analysis.html` — exported notebook
- Five CSV files — dengue, weather and population datasets

## Run the notebook

Keep the CSV files in the same directory as the notebook. Install Python, Jupyter Notebook, NumPy, pandas, Matplotlib and seaborn, then open the notebook and run its cells in order:

```sh
python -m pip install notebook numpy pandas matplotlib seaborn
jupyter notebook
```

## Data sources and attribution

This school project uses the following datasets from [data.gov.sg](https://data.gov.sg/). Credit goes to the respective government agencies:

- [Weekly number of dengue and dengue haemorrhagic fever cases](https://data.gov.sg/datasets/d_ac1eecf0886ff0bceefbc51556247015/view) — Ministry of Health (MOH)
- [Rainfall: monthly total](https://data.gov.sg/datasets/d_b16d06b83473fdfcc92ed9d37b66ba58/view) — National Environment Agency (NEA)
- [Surface air temperature: monthly mean](https://data.gov.sg/datasets/d_755290a24afe70c8f9e8bcbf9f251573/view) — NEA
- [Relative humidity: monthly mean](https://data.gov.sg/datasets/d_e3b1111a26b2aefef4f386c068d4ca5d/view) — NEA
- [Indicators on population, annual](https://data.gov.sg/datasets/d_3d227e5d9fdec73f3bcadce671c333a6/view) — Singapore Department of Statistics (SingStat)

Contains information from the datasets listed above, accessed on August 2026 from data.gov.sg, made available under the terms of the [Singapore Open Data Licence version 1.0](https://data.gov.sg/open-data-licence).
