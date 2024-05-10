<h1>Project Guidelines</h1>

<h3>Requirements</h3>
Some data cleaning components. Meaning do not just take a dataset online that is already prepared and ready to go.
You will have to clean it up in some way.
Kaggle datasets are discouraged


<h3>Outline</h3>
- One section on background of data, question
- Describe data cleaning process. What was missing, what did you do to get around the missing inputs, and how did you clean it to make it workable.
- Visualization. Make plots, graphs, etc
- A little less important, statistical analysis. What model did you use and why? What did you infer from the model and analysis


Besides that, we are free to use any type of data we want, performing any sort of analysis to answer whatever questions we have of the data. Example: we use WW2 casualty stats and want to figure out how physical attributes or where they were trained helped with survival rates.

Final report will just be a summary with all this information, including visuals and some other miscellaneous stuff that might’ve been excluded from the presentation. Min 10 pages.


<h2>cleaning.Rmd Notes</h2>

<h3>Missing Data Substitutions</h3>
For missing Opening_Gross data, substituted with earliest recorded Gross
- The Wandering Earth 2 = $3,006,525-
  - Weekend Box Office Performance, Week 2
  - The week 2 date is within the same week as opening day
- Come Out in Jesus Name = $973795
  - Gross data on opening day
- The Lord of the Rings: The Return of the King = $1,176,085
  - April 13, 2023 Re-release, domestically

<h3>For missing MPAA data: most are simply not rated by MPAA</h3>
- Renaissance: A Film by Beyoncé (2023) - Not Rated (USA)
- Pathaan - Not Rated (USA)
- Jawan - Not Rated (USA)
- Animal - Not Rated (USA)
- Salaar - Not Rated (USA)
- Dunki - Not Rated (USA)
- The Chosen Season 3 Finale - PG
  - The TV show is rated TV-PG, which is the TV Parental Guidelines equivalent of PG in MPAA
- BTS: Not Yet in Cinemas - Not Rated (USA)
- Waitress: The Musical - Not Rated (USA)
-   No conclusive MPAA rating
- Tiger 3 - Not Rated (USA)
- Ponniyin Selvan: Part Two - Not Rated (USA)
- Left Behind: Rise of the Antichrist - Not Rated (USA)
- The Journey: A Music Special with Andrea Bocelli - Not Rated (USA)
- The Wandering Earth 2 - Not Rated (USA)
- 2023 Oscar Nominated Short Films: Live Action - Not Rated (USA)
- Tu Jhoothi Main Makkaar - Not Rated (USA)
- Come Out in Jesus Name - Not Rated (USA)
- Skinamarink - Not Rated (USA)
- Die Hard - R
- Re-released on December 8, 2023
- Winnie-the-Pooh: Blood and Honey - Not Rated (USA)
- Lost in the Stars - Not Rated (USA)
- Creation of the Gods I: Kingdom of Storms - Not Rated (USA)
- Back to the Future - PG

<h3>For missing Theaters data</h3>
- Lost in the Stars - 62
  - Weekend Box Office Performance
- The Retirement Plan - 1175, 925
  - Weekly Box Office Performance
  - For weeks of Sept. 15 and Sept. 22 respectively

<h3>For missing Distributor data</h3>
- https://www.the-numbers.com/market/2023/top-grossing-movies
- Filled in missing data with above

<h2>Miscellaneous Notes</h2>
- Removed Coraline movie data since it had too much missing data (such as budget and tickets.sold)
- Included function to extract individual covariate data – parse_data
  - Used this function to create the dataset, simple_movies, which just compiles the basic information such as budget and rank.
  - Simple_movies is used heavily in shiny.Rmd

<h2>shiny.Rmd Notes</h2>
<h3>Miscellaneous Notes</h3>
- Creating shiny app interface for user to interact with data
- Starts off with a basic overview of the movies data
  - Some data is excluded from this main window, specifically the ones  involving the dates (weekly data for one)
  - The release date should be included but could not figure out the code
- The other window just shows a simple bar graph with the top distributors
- Also included are links to source data, as well author names
- Can update in the future with analyses, should be as simple as implementing plots and such
