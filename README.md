# Franchises detection using BoxOfficeMojo and OMDBAPI

I visualized a Social Network of Actors, where two actors are linked if they starred together in more than a movie. It is a rough estimate of the existence of a franchise.

The data is based on the top 500 Grossing Movies according to BoxOfficeMojo. After having retrieved the titles from scraping BoxOfficeMojo, I used the OMDBAPI to retrieve data about the movies.

Here is an example of how an entry from the OMDBAPI looks like.

```
{'Actors': 'Emma Watson, Dan Stevens, Luke Evans, Josh Gad',
 'Awards': 'Nominated for 2 Oscars. Another 12 wins & 65 nominations.',
 'BoxOffice': '$503,974,884',
 'Country': 'USA',
 'DVD': '06 Jun 2017',
 'Director': 'Bill Condon',
 'Genre': 'Family, Fantasy, Musical, Romance',
 'Language': 'English',
 'Metascore': '65',
 'Plot': 'A selfish prince is cursed to become a monster for the rest of his life, unless he learns to fall in love with a beautiful young woman he keeps prisoner.',
 'Poster': 'https://m.media-amazon.com/images/M/MV5BMTUwNjUxMTM4NV5BMl5BanBnXkFtZTgwODExMDQzMTI@._V1_SX300.jpg',
 'Production': 'Walt Disney Pictures',
 'Rated': 'PG',
 'Ratings': [{'Source': 'Internet Movie Database', 'Value': '7.2/10'},
  {'Source': 'Rotten Tomatoes', 'Value': '71%'},
  {'Source': 'Metacritic', 'Value': '65/100'}],
 'Released': '17 Mar 2017',
 'Response': 'True',
 'Runtime': '129 min',
 'Title': 'Beauty and the Beast',
 'Type': 'movie',
 'Website': 'http://movies.disney.com/beauty-and-the-beast-2017',
 'Writer': 'Stephen Chbosky (screenplay by), Evan Spiliotopoulos (screenplay by), Linda Woolverton (based on the 1991 animated film "Beauty and the Beast" animation screenplay by)',
 'Year': '2017',
 'imdbID': 'tt2771200',
 'imdbRating': '7.2',
 'imdbVotes': '241,321'}
```

Some caveats: the OMBDAPI returns only four actors per movie, the full cast is not available.

Here is the network.

The size of the bubble is the Centrality, while the more movies the Actors starred together in, the heavier the edge.

See how many franchises you can identify!

[!network][network.png]
