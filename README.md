# NetflixDataAnalysis

### Difficulties and interesting about your Netflix Show dataset 
#### Difficulties
1. Missing Data: One of the significant challenges is handling missing data. For instance, some shows might not have complete information about their release dates. This made it difficult to perform a comprehensive analysis 
   or predictive modeling.
2. Rapid Content Turnover: Netflix frequently updates its content library. The rapid turnover made it difficult to maintain an up-to-date dataset, as shows come and go regularly.
3. Multiple Genres: Shows can belong to multiple genres, making it challenging to categorize them neatly. This complexity can complicate genre-based analysis or recommendation systems.
4. Global Availability: Netflix operates globally, and the availability of shows can vary by region. Analyzing data without considering regional differences can lead to inaccurate conclusions.

#### Interesting Facts
 1. Content Release Strategies: Additionally, Netflix's strategy of releasing entire seasons at once versus weekly episodes can also be analyzed. This can provide insights into how different release strategies impact       viewer engagement and retention.

## Data Fun (20 pts):

### Use simple SQL queries to play with the data.
  SELECT * 
  FROM netflix_titles
  WHERE release_year = 2021;
  
  SELECT * 
  FROM netflix_titles
  WHERE director LIKE '%Toshiya Shinohara%';
  
  SELECT * 
  FROM netflix_titles
  WHERE rating = 'PG-13';
  
### Find 2 cool facts hidden within the data (e.g., most popular interests).
  1. The average time duration of the Netflix shows is 56 minutes and 46 seconds.

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

  SELECT * 
  FROM netflix_titles
  WHERE release_year = 2021;
  
  SELECT * 
  FROM netflix_titles
  WHERE director LIKE '%Toshiya Shinohara%';
  
  SELECT * 
  FROM netflix_titles
  WHERE rating = 'PG-13';

  SELECT title, duration, description
  FROM netflix_titles
  WHERE country = 'United States';
  
#### AVERAGE
  SELECT AVG(duration) AS average_duration_minutes
  FROM netflix_titles;

#### SUM

## Ask Away (30 pts):

### Formulate 2 questions about the data (e.g., what are popular shows in different countries?).
### Write basic SQL queries (WHERE, ORDER BY) to find answers.
##### How many movies are made in every country?
   SELECT country, COUNT(*) AS number_of_movies
   FROM netflix_titles
   WHERE type = 'Movie'
   GROUP BY country
   ORDER BY number_of_movies DESC;

##### How many TV Shows are made in every country?
   SELECT country, COUNT(*) AS number_of_tv_shows
   FROM netflix_titles
   WHERE type = 'TV Show'
   GROUP BY country
   ORDER BY number_of_tv_shows DESC;

##### How many movies in Japan are rated as TV-14?
   SELECT COUNT(*) AS number_of_tv14_movies
   FROM netflix_titles
   WHERE country = 'Japan'
     AND type = 'Movie'
     AND rating = 'TV-14';
     
##### Which are the movies that are listed as 'Thillers'?
   SELECT title, duration, description
   FROM netflix_titles
   WHERE type = 'Movie'
     AND listed_in LIKE '%Thrillers%';

### Share what you learned from the answers.

## Showtime! (20 pts):
### Use a tool (like Microsoft Excel charts) to create 3 charts showing your findings.
###Choose charts that clarify your discoveries using (bar charts, pie charts etc.).
