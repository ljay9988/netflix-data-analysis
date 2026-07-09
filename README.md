# Project Netflix content analysis.

Project Netflix content analysis. is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

## Dataset Content

* THe Dataset used in this project is the Netflix Movies and TV Shows dataset published by Shivam Bansal. It contains 8,807 entries representing all movies and TV shows available on Netflix at the time of collection. Each entry includes metadata such as:
Title, Type (movie or TV show), Director, Cast, Country of prduction, Date added to Netflix, Release year, Rating, Duration, Genre categories and Description. 

## Business Requirements

* Identify trends in Netflix's content catalogue including growth overtime.
* Understand genre popularity.
* Analyse geographical diversity, identifying which countries contribute the most content to Netflix.
* Provide visual insights that help stakeholders understand how Netflix's libary has evolved over time.

## Hypothesis and how to validate?

* Hypothesis 1 - Netflix has added significantly more content in recent years compared to earlier years.  
Validation:  
Analyse the date_added column, plot content additions over time, and identify growth trends. 

* Hypothesis 2 - Movies make up a larger portion of Netflix’s catalogue than TV shows.  
Validation:  
Calculate the distribution of type (Movie vs TV Show) and visualise it using a bar chart. 

* Hypothesis 3 - The majority of Netflix content originates from a small number of countries.  
Validation:  
Count occurrences in the country column and visualise the top contributing countries.

* Hypothesis 4 - Certain genres (e.g., Drama, Comedy) appear more frequently than others.  
Validation:  
Split the listed_in genre field, count genre frequency, and visualise the top genres.

* Hypothesis 5 - Most Netflix content is rated for mature audiences (e.g., TV‑MA, R).  
Validation:  
Analyse the distribution of the rating column and visualise the most common maturity ratings.

## Hypotheses Results

All five hypotheses were tested using the cleaned Netflix dataset.  
The visualisations and analysis confirmed each hypothesis:

Hypothesis 1: Netflix has added significantly more content in recent years.  
Confirmed — the content added per year shows a clear upward trend.

Hypothesis 2: Movies make up a larger portion of Netflix’s catalogue than TV shows.  
Confirmed — movies appear more frequently than TV shows in the dataset.

Hypothesis 3: Most Netflix content originates from a small number of countries.  
Confirmed — the United States and India dominate the catalogue.  
"Unknown" values were removed to keep results accurate.

Hypothesis 4: Certain genres appear more frequently than others.  
Confirmed — Drama, Comedy, and International content are the most common genres.

Hypothesis 5: Most Netflix content is rated for mature audiences.  
Confirmed — TV‑MA is the most common rating by a large margin.

## Project Plan

1. ETL (Extract, Transform, Load) 
   - Loaded the dataset.  
   - Removed duplicates and cleaned missing values.  
   - Standardised dates and split multi‑value fields.  
   - Prepared the dataset for analysis.

2. EDA (Exploratory Data Analysis)  
   - Explored trends in content, genres, ratings, and countries.  
   - Validated all five hypotheses using charts and summary statistics.

3. Visualisation Notebook  
   - Created clear visualisations to communicate insights.  
   - Removed invalid values such as "Unknown" to improve accuracy.


## The rationale to map the business requirements to the Data Visualisations

* Rationale for Visualisations

Each business requirement was mapped to a visualisation:

- Content growth over time → Line chart  
- Movies vs TV Shows → Bar chart  
- Top countries → Scatter plot  
- Genre popularity → Bar chart  
- Ratings distribution → Bar chart and scatter plot



## Analysis techniques used

- Data cleaning using pandas (dropna, explode, apply, value_counts).  
- Data transformation using string operations and lambda functions.  
- Exploratory analysis using grouping and counting.  
- Visualisation using matplotlib, seaborn, and plotly.

Limitations:
- Some fields (e.g., cast, director) contain missing values.  
- Country data includes "Unknown", which was removed for accuracy.  
- Genre lists vary in length, requiring explode operations.

## AI help
AI tools were used to help simplify code and improve documentation.
Use of AI Tools
AI tools (Microsoft Copilot) were used to support the project in the following ways:

- Helping generate clear explanations and Markdown text for the notebooks.
- Assisting with code structure and simplifying complex Python operations.
- Providing guidance on cleaning steps such as removing "Unknown" values.
- Helping design visualisation choices and improve readability.
- Supporting ideation when planning the project layout and documentation.
- helping with indentation and syntax.
All code was written and tested by me, with AI used only for guidance, clarification, and optimisation.

## Code Documentation References

During development, official documentation was used to understand and apply key functions:

- pandas.DataFrame.explode()  
  https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.explode.html

- pandas.Series.str.split()  
  https://pandas.pydata.org/docs/reference/api/pandas.Series.str.split.html

- pandas.Series.apply() with lambda 
  https://pandas.pydata.org/docs/reference/api/pandas.Series.apply.html

- pandas.DataFrame.value_counts()  
  https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html

- matplotlib.pyplot
  https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.html

- seaborn  
  https://seaborn.pydata.org/api.html

- plotly.express  
  https://plotly.com/python/plotly-express/

These resources helped me understand how to manipulate the dataset and build the visualisations.

 

## Unfixed Bugs

No major bugs remain unfixed.  
The hardest challenge for me was the data cleaning and handling "Unknown" country values, which was resolved by filtering them out.  
Some fields contain missing values, but these do not affect the main hypotheses.


## Development Roadmap

Future improvements could include:

- Adding dashboards using Power BI 
- Analysing cast and director patterns.  
- Adding predictive modelling (e.g., genre trends).  
- Improving automation in the ETL process.

These steps will help expand the project beyond basic analysis.


## Deployment (optional)

* If this is a Unit 3 Streamlit, Power BI or Tableau Public project, then you can include a link here and explain how you hosted the dashboard.


## Credits
Main Data Analysis Libraries

This project used several Python libraries to clean, analyse, and visualise the Netflix dataset.  
Below are the main libraries and simple examples of how they were used:

pandas
Used for data cleaning, transformation, and exploration.

Examples:
- `explode()` — to split multi‑value columns like genres and countries into separate rows.  
- `str.split()` — to break comma‑separated values into lists.  
- `apply()` with `lambda` — to clean text fields and create new columns.  
- `value_counts()` — to count occurrences for countries, genres, and ratings.

matplotlib
Used to create basic charts such as bar charts and scatter plots.

Example:
- `plt.scatter()` — to plot the top countries by number of titles.

seaborn
Used for cleaner, more visually appealing statistical plots.

Example:
- `sns.countplot()` — to show the distribution of movie vs TV show content.

plotly.express
Used for interactive charts that make the analysis easier to explore.

Example:
- `px.scatter()` — to create interactive bubble charts for top countries and ratings.


### Content 

- The text for the Home page was taken from the Wikipedia Article A
- Instructions on how to implement form validation were taken from a [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)




## Acknowledgements

Thanks to Code Institute for the dataset guidance and project structure.
thanks to Vasi, Rory, and Neil for the masterclasses and recordings watching them back really helped with getting set up and starting the project!!!  
Thanks to Microsoft Copilot for helping with making hard tasks sound simpler, ideation, documentation, and code optimisation and pointing me in the right direction.
