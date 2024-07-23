# Data Science: Genius API Analysis
This project involves collecting and analysing song and artist data from the Genius open-source web API for four different artists:
- Hozier
- Kanye West
- Kendrick Lamar
- Elton John

## Task 1: Data Collection
<b>Data Collection</b> is stored in the Jupyter Notebook <i>Genius_Data_Collection</b>. It accomplishes the following subtasks:
1) Creates and populating directories for raw data and lyrics from the Genuis API for the four artists of interest.
2) Uses a function to take advantage of the Genius website's search capabilities to obtain information on the artists' top 10 most "interacted with" songs. Once obtained, the function generates populates .json files with the information found. This function is to be run a number of times over a period of time to obtain time-specific information. This provides information on each song's:
- Name
- Unique ID Number
- Number of Annotations (Notes that explain deeper meaning behind the lyrics)
- User Interest (People who liked the Genius article via the website)
- Page Views
3) Creates a function to scrape the lyrics of the top song of each artist using the song path provided by the API to get approximate lyric length.

## Task 2: Data Analysis
<b>Data Analysis</b> is stored in the Jupyter Notebook <i>Genius_Data_Analysis</b>. It accomplishes the following subtasks:
1) Preprocesses the data by:
- Separating the .json files by artist
- Parsing the individual raw .json files that were taken over different time periods
- Reading and counting the approximate number of lyrics for each song, and storing them in a dictionary corresponding to their artist
- Storing all collected data in a Dataframe
2) Verifies the format, number of rows and date ranges, and missing values in the Dataframe
3) Stores the now cleaned data in a .json file
4) Performs <b>Annotation Analysis</b>, using boxplots and barcharts to compare:
- Min, max, mean, and median of annotations by the artist
- Min, max, mean, and median of annotations of each song by one artist
5) Performs <b>Page Views Analysis</b>, using graphs and barcharts to compare each artist's top viewed song and its views over the time period the data was collected for. This allowed for insights on:
- Total page views
- Top song page view rates over time
6) Performs <b>User Interest Analysis</b>, using piecharts and barcharts to compare the spread of interest across an artist's songs to see if an artist can be classified as a "one-hit wonder" with one successful song boosting their numbers.
7) Performs <b>Lyric Analysis</b>, using barcharts to compare how long an artist's songs are.
8) Performs <b>Correlation Analysis</b> on each of the above characteristics, using scatter matrices and heat maps to investigate if each of the above characteristics affect each other. Examples of intuitive correlations would include:
- Assuming Page Views would influence User Interest
- Assuming Amount of Lyrics would influence Amount of Annotations
