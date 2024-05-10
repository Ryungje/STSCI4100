<h1>Project Guidelines</h1>

<h3>Requirements</h3>
Some data cleaning components. Meaning do not just take a dataset online that is already prepared and ready to go.
You will have to clean it up in some way.
Kaggle datasets are discouraged


<h3>Outline</h3>
- One section on background of data, question<br>
- Describe data cleaning process. What was missing, what did you do to get around the missing inputs, and how did you clean it to make it workable.<br>
- Visualization. Make plots, graphs, etc<br>
- A little less important, statistical analysis. What model did you use and why? What did you infer from the model and analysis<br>
<br>
<br>
Besides that, we are free to use any type of data we want, performing any sort of analysis to answer whatever questions we have of the data. Example: we use WW2 casualty stats and want to figure out how physical attributes or where they were trained helped with survival rates.
<br>
Final report will just be a summary with all this information, including visuals and some other miscellaneous stuff that might’ve been excluded from the presentation. Min 10 pages.
<br>
<h2>cleaning.Rmd Notes</h2>

<h3>Missing Data Substitutions</h3>
For missing Opening_Gross data, substituted with earliest recorded Gross<br>
- The Wandering Earth 2 = $3,006,525<br>
  - Weekend Box Office Performance, Week 2<br>
  - The week 2 date is within the same week as opening day<br>
- Come Out in Jesus Name = $973795<br>
  - Gross data on opening day<br>
- The Lord of the Rings: The Return of the King = $1,176,085<br>
  - April 13, 2023 Re-release, domestically<br>

<h3>Missing MPAA data: most are simply not rated by MPAA</h3>
- Renaissance: A Film by Beyoncé (2023) - Not Rated (USA)<br>
- Pathaan - Not Rated (USA)<br>
- Jawan - Not Rated (USA)<br>
- Animal - Not Rated (USA)<br>
- Salaar - Not Rated (USA)<br>
- Dunki - Not Rated (USA)<br>
- The Chosen Season 3 Finale - PG<br>
  - The TV show is rated TV-PG, which is the TV Parental Guidelines<br> equivalent of PG in MPAA<br>
- BTS: Not Yet in Cinemas - Not Rated (USA)<br>
- Waitress: The Musical - Not Rated (USA)<br>
-   No conclusive MPAA rating<br>
- Tiger 3 - Not Rated (USA)<br>
- Ponniyin Selvan: Part Two - Not Rated (USA)<br>
- Left Behind: Rise of the Antichrist - Not Rated (USA)<br>
- The Journey: A Music Special with Andrea Bocelli - Not Rated (USA)<br>
- The Wandering Earth 2 - Not Rated (USA)<br>
- 2023 Oscar Nominated Short Films: Live Action - Not Rated (USA)<br>
- Tu Jhoothi Main Makkaar - Not Rated (USA)<br>
- Come Out in Jesus Name - Not Rated (USA)<br>
- Skinamarink - Not Rated (USA)<br>
- Die Hard - R<br>
- Re-released on December 8, 2023<br>
- Winnie-the-Pooh: Blood and Honey - Not Rated (USA)<br>
- Lost in the Stars - Not Rated (USA)<br>
- Creation of the Gods I: Kingdom of Storms - Not Rated (USA)<br>
- Back to the Future - PG<br>

<h3>Missing Theaters data</h3>
- Lost in the Stars - 62<br>
  - Weekend Box Office Performance<br>
- The Retirement Plan - 1175, 925<br>
  - Weekly Box Office Performance<br>
  - For weeks of Sept. 15 and Sept. 22 respectively<br>

<h3>Missing Distributor data</h3>
- https://www.the-numbers.com/market/2023/top-grossing-movies<br>
- Filled in missing data with above<br>

<h2>Miscellaneous Notes</h2>
- Removed Coraline movie data since it had too much missing data (such as budget and tickets.sold)<br>
- Included function to extract individual covariate data – parse_data<br>
  - Used this function to create the dataset, simple_movies, which just compiles the basic information such as budget and rank.<br>
  - Simple_movies is used heavily in shiny.Rmd<br>

<h2>shiny.Rmd Notes</h2>
<h3>Miscellaneous Notes</h3>
- Creating shiny app interface for user to interact with data<br>
- Starts off with a basic overview of the movies data<br>
  - Some data is excluded from this main window, specifically the ones  involving the dates (weekly data for one)<br>
  - The release date should be included but could not figure out the code<br>
- The other window just shows a simple bar graph with the top distributors<br>
- Also included are links to source data, as well author names<br>
- Can update in the future with analyses, should be as simple as implementing plots and such<br>
