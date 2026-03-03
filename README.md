**Performance Analysis of Elite Runners at the Berlin Marathon in Python**
* Exploratory data analysis of Berlin Marathon top 100 finishers (2015-2025), examining performance trends, gender distribution, and nationality patterns using Python. The project uses official race results data accessed via API and focuses on performance evolution among elite runners.

**Tools & Techniques**
* API data extraction & pagination, JSON parsing, data cleaning & transformation, multi-index grouping & reshaping (groupby, unstack), custom function creation, time conversion (hh:mm:ss to seconds), aggregations & ranking (mean, size, nlargest), data visualization with matplotlib

**Key Insights**
* The average finishing time among the top 100 male runners remained relatively stable across the years, with minor fluctuations.
* The average finishing time overall and for each gender has increased in 2021, possibly indicating a lack of training opportunities during the onset of the COVID-19 pandemic in 2020.
* Female runners among the top 100 finishers showed a gradual improvement in average finishing time in recent years.
* The gender distribution within the top 100 runners varies by year, with male runners accounting for a higher share.
* Germany consistently represents a large share of the top 100 finishers, reflecting the domestic nature of the event.
* East African nations (particularly Kenya and Ethiopia) frequently rank among the top nationalities in the elite field.
* The composition of nationalities among the top 100 changes slightly over time, indicating shifts in competitive dominance. 

**Data Information**
* Data was collected from the official [Berlin Marathon website](https://www.bmw-berlin-marathon.com/en/your-race/results) and the [results API](https://api.results.scc-events.com/result).
* The project extracts the following variables for each athlete: Event Year, Name, Nationality, Gender, Overall Place, Gender Place, Club, Official Finishing Time (brutto).
* Finishing times were converted into seconds for quantitative analysis.

**Project Structure**
* Data Collection: Iterative API requests per year (2015-2025, excluding 2020, since 2020 the Berlin Marathon did not take place), pagination to retrieve top 100 finishers, handling different API parameters pre/post 2020.
* Data Cleaning & Transformation: Selection of relevant variables, conversion of finishing times into numerical format, creation of structured pandas data frame.
* Exploratory Analysis: Average finishing time per year and gender, gender distribution among top 100 runners, top 3 nationalities per year, trend visualizations.
* Visualization: Line plots(performance trends), comparative gender analysis, nationality ranking over time.
