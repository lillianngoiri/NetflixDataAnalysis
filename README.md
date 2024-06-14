# NetflixDataAnalysis

### Difficulties and interesting about your Netflix Show dataset 
#### Difficulties
1. Missing Data: One of the significant challenges is handling missing data. For instance, some shows might not have complete information about their release dates. This made it difficult to perform comprehensive analysis 
   or predictive modeling.
2. Rapid Content Turnover: Netflix frequently updates its content library. The rapid turnover made it difficult to maintain an up-to-date dataset, as shows come and go on a regular basis.
3. Multiple Genres: Shows can belong to multiple genres, making it challenging to categorize them neatly. This complexity can complicate genre-based analysis or recommendation systems.
4. Global Availability: Netflix operates globally, and the availability of shows can vary by region. Analyzing data without considering regional differences can lead to inaccurate conclusions.

#### Instresting Facts
 1. Content Release Strategies: Additionally, Netflix's strategy of releasing entire seasons at once versus weekly episodes can also be analyzed. This can provide insights into how different release strategies impact       viewer engagement and retention.

## Data Fun (20 pts):

### Use simple SQL queries to play with the data.
### Find 2 cool facts hidden within the data (e.g., most popular interests).
  1. The average time duration of the netflix shows is 56 minutes and 46 seconds.
### Use basic SQL queries like (COUNT, AVG, and SUM) to understand more about the data you have.
#### COUNT
  SELECT release_year, COUNT(*) AS num_shows_added
  FROM netflix_titles
  GROUP BY release_year
  ORDER BY release_year;

  SELECT country, COUNT(*) AS num_shows
  FROM netflix_titles
  GROUP BY country
  ORDER BY num_shows DESC
  LIMIT 10;
  
#### AVERAGE
  SELECT AVG(duration) AS average_duration_minutes
  FROM netflix_titles;


## Ask Away (30 pts):
### Formulate 2 questions about the data (e.g., what are popular shows in different countries?).
### Write basic SQL queries (WHERE, ORDER BY) to find answers.
### Share what you learned from the answers.

## Showtime! (20 pts):
### Use a tool (like Microsoft Excel charts) to create 3 charts showing your findings.
###Choose charts that clarify your discoveries using (bar charts, pie charts etc.).
