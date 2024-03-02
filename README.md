# netflix_movies_tv_shows

# Project Summary

Netflix is a popular streaming service that provides its subscribers with a wide range of movies, TV shows, documentaries, and original content to watch on demand. The company was founded in 1997 as a DVD rental service but later pivoted to an online streaming model in 2007. Since then, Netflix has grown into one of the most popular streaming services globally, with over 200 million subscribers in more than 190 countries as of 2021.

Netflix's success is due in part to its innovative business model and emphasis on creating original content. The company invests heavily in producing its own movies and TV shows, which have won numerous awards and attracted high-profile talent. Netflix also uses sophisticated algorithms to recommend content to its users, based on their viewing history and preferences.

This project aimed to identify patterns in the content available on the platform and group them into clusters based on similarities in their genres, sub-genres, release year, and other features. The project utilized machine learning algorithms such as K-means clustering and Hierarchical Clustering to cluster the data.

# Methods used:
Descriptive Statistics.

Data Visualization.

Machine Learning.

# Libraries utilized:
NumPy and Pandas - For dataset cleaning and analysis.

Matplotlib, Plotly and Seaborn - For Data Visualization.

SkLearn and nltk - For machine learning and clustering.

# Data Description
Show_id : Unique ID for every Movie / Tv Show

Type : Identifier - A Movie or TV Show

Title : Title of the Movie / Tv Show

Director : Director of the Movie

Cast : Actors involved in the movie / show

Country : Country where the movie / show was produced

Date_added : Date it was added on Netflix

Release_year : Actual Releaseyear of the movie / show

Rating : TV Rating of the movie / show

Duration : Total Duration - in minutes or number of seasons

Listed_in : Genres

Description: The Summary description

# Problem Statement

This dataset contains tv shows and movies available on Netflix as of 2019. The data is collected from Flixable which is a third-party Netflix search engine. In 2018, they released an interesting report which shows that the number of tv shows on Netflix has nearly tripled since 2010. The streaming service's number of movies has decreased by more than 2000 titles since 2010, while its number of tv shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset.

In this project, i did

Exploratory Data Analysis

Understood what types of content are available in different countries.

If Netflix has been increasingly focusing on TV rather than movies in recent years.

Clustered similar content by matching text-based features.

# EDA Summary:

There are more movies (69.14%) than TV shows (30.86%) in the dataset.
Raul Campos and Jan Suter together have directed 18 movies / TV shows, higher than anyone.
The highest number of movies / TV shows were based out of the US, followed by India and UK. The top 3 countries together account for about 56% of all movies and TV shows in the dataset. This value increases to about 78% for top ten countries.
Netflix has greater number of new movies / TV shows than the old ones.
The dramas is the most popular genre followed by comedies and documentaries. These three genres account for about 41% of all movies and TV shows. This value increases to about 82% for top 10 genres.
On average a greater number of shows are added in the months of October, November, December, and January.
There is a decrease in the number of shows added in the year 2020, which might be attributed to the covid-19-induced lockdowns, which halted the creation of shows. We have Netflix data only up to 16th January 2021, hence there are less movies added in this year.
The majority of the shows on Netflix are catered to the needs of adult and young adult population.
Over the years, Netflix has consistently focused on adding more shows in its platform. Though there was a decrease in the number of movies added in 2020, this pattern did not exist in the number of TV shows added in the same year. This might signal that Netflix is increasingly concentrating on introducing more TV series to its platform rather than movies.
The TV series in the dataset have up to 16 seasons, however the bulk of them only have one. This might mean that the majority of TV shows has only recently begun, and that further seasons are on the way. There are very few TV shows that have more than 8 seasons.
The length of a movie may range from 3 min to 312 minutes, and is almost normally distributed.
Netflix has several movies on its site, including those that were released in way back 1942. Movies produced in the 1940s had a fairly short duration on average. On average, movies made in the 1960s have the longest movie length. The average length of a movie has been continuously decreasing since the 2000s.
Dramas, comedies, and documentaries are the most popular genre for the movies on Netflix. International, crime, and kids are the most popular genre for TV shows on Netflix.
Raul Campos and Jan Suter have together directed in 18 movies, higher than anyone yet. This is followed by Marcus Roboy, Jay Karas, and Cathy Gracia-Molina. Alastair Fothergill has directed three TV shows, the most of any director. Only six directors have directed more than one television show.
Samuel West has appeared in 10 movies, followed by Jeff Dunham with 7 movies. David Attenborough has appeared in 13 TV shows, followed by Michela Luci, Jamie Watson, Anna Claire Bartlam, Dante Zee, Eric Peterson with 4 TV shows.

# Summary and Conclusion:
In this project, we tackled a text clustering issue where we had to categorize Netflix shows into specific clusters such that the shows within a cluster are similar to one another and the shows in different clusters are dissimilar to one another.

Once our dataset is loaded, and then we search for duplicates and missing values. No duplicate values were discovered, and any missing values were used to fill them in. In our dataset, the director column contains the most missing entries, followed by cast, country, and date_added. The string "unknown" is used to fill missing values in the director and country columns, "no cast" is used fill in the cast column, and the mode value is used to fill missing values in the rating column. the records that had null entries in the "date_added" column were deleted.

31% of Netflix's content is television shows, while 69% of it is movie show, demonstrating that movie shows have greater content. TV-MA, which stands for "Mature Audience," is the most frequently used classification for movie and tv shows, followed by TV-14, which stands for "Younger Audience." Since the number of movie shows is higher than the number of TV shows, movie shows receive the highest rating when compared to TV shows, from this we can say people like to watch movie show than compare to tv shows.

Over the years, Netflix has added more shows to its platform. Most movies were released in 2017 and 2018. Most television shows were broadcast in 2019 and 2020. The covid-19-induced lockdowns that stopped the production of shows may be to blame for the decline in the number of movies added in the year 2020. There are fewer movies uploaded this year because the Netflix data we have only extends through 2021.

Netflix's movie show library is expanding much more quickly than its TV show library. It looks that Netflix has prioritised adding more movie material over TV shows. The growth of movies has been significantly more pronounced than that of TV shows.More content is released over the Christmas season (October, November, December, and January). There are more movies released each month compared to TV shows.Documentaries are the most popular Netflix category, followed by stand-up comedy, dramas, and foreign films. Kids TV is the most well-liked Netflix TV shows.

The majority of movies durations last between 90 and 120 minutes. Most tv shows have just one season. The lengthiest average runtimes are found in NC-17 rated movies. The average duration of movies with a TV-Y rating is the shortest. The geograph visualisations show that the United States and India are the two countries that produce the most content.

Majority of the features have textual value so I applied NLP to that for preprocessing the data. After that, the dimension increased to 10000. So I applied PCA for dimensionality reduction, and I ended up with 4000 features.

I implemented two models kmeans and agglomerative clustering. In kmeans I got 6 cluster value with the elbow method and silhouette score. So finally I chose 6 number of clusters as my optimal k value. At last through dendrogram i found the optimal value for k is 4. So i ended up doing agglomerative clustering with four clusters.
