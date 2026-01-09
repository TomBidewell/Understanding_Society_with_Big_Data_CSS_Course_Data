# Understanding Society with Big Data Computational Social Science (INFR08034) Data Repository

This repository contains the datasets used in the Understanding Society with Big Data course. The data here will be used throughout the course to help you learn how computational and data-driven methods can be applied to real questions about society.

The datasets span multiple topics, data types, and analytical approaches, including numerical data, text, and networks. They are designed to support hands-on work for tools introduced during the course.

You do not need to use every dataset. Instead, you are encouraged to explore, compare, and choose data that best fits your interests and research questions.

## What’s in this repository?

### Topics covered
The data are organised into three main topic areas:
- Climate Change
- Housing
- Political Polarisation

Each topic folder contains multiple datasets offering different perspectives on the same issue (for example, combining official statistics with social media data or network data with text).

### Climate Change

This topic explores climate change from multiple angles: empirical measurements, public attention, media narratives, and online discussion.

#### Folder Structure

```
climate_change
  ├── empirical_data
  │   ├── global_temperatures
  │   │   ├── global_temperatures.csv
  │   │   ├── northern_hemisphere_temperatures.csv
  │   │   └── southern_hemisphere_temperatures.csv
  │   │
  │   ├── natural_emergencies
  │   │   └── natural_emergencies.csv
  │   │
  │   └── sea_levels
  │       └── sea_level_change.csv
  │
  ├── google_trends
  │   ├── popularity_of_climate_searching_by_city.csv
  │   ├── popularity_of_climate_searching_by_region.csv
  │   └── popularity_of_climate_searching_by_time.csv
  │
  ├── news
  │   ├── climate_related_news_around_world_translated_to_english.csv
  │   └── climate_related_news_in_english.csv
  │
  └── twitter
      ├── retweet_week_num09_May-03-19.csv
      ├── retweet_week_num14_Jun-07-19.csv
      ├── retweet_week_num18_Jul-02-19.csv
      ├── retweet_week_num27_Sep-06-19.csv
      └── tweets_with_topics.csv
```

#### What you can explore?
- Long-term trends in global and regional temperatures
- The relationship between climate events and public attention
- How climate change is discussed in news media across countries
- Network structures and topic dynamics in Twitter discussions

#### Key Datasets
- **global_temperatures.csv, northern_hemisphere_temperatures.csv, southern_hemisphere_temperatures.csv** :
This data originates from the NASA GISS Temperature Analysis (GISTEMP v4). The values are an estimate of the global surface temperature change derived from land-surface, air and sea-surface water temperature anomalies. This data provides temperature change values on the global scale as well as for the Northern and Southern Hemispheres. This data is downloaded from: https://www.kaggle.com/datasets/sujaykapadnis/global-surface-temperatures .
- **natural_emergencies.csv** :
This data records natural disasters and emergencies around the world from 2004-2025. The data came from the Emergency Events Database (EM-DAT) from the Centre for Research on the Epidemiology of Disasters. For further details, see: [https://www.emdat.be](https://www.emdat.be/) .
- **sea_level_change.csv** :
This data is from NASA's Sea Surface Height project (NASA-SSH) and reports a time series of globally-averaged sea level change in centimetres from 1993 to the present day. More information on the project and the data can be found at the following links: https://podaac.jpl.nasa.gov/NASA-SSH , https://earth.gov/sealevel/vital-signs/sea-level/ .
- **popularity_of_climate_searching_by_city.csv , popularity_of_climate_searching_by_region.csv , popularity_of_climate_searching_by_time.csv** :
Search trends from Google for the terms "Climate Change" and "Global Warming" worldwide, US-only and UK-only. We also split by region and city as well as provide time series for search popularity over time.
- **climate_related_news_in_english.csv** :
This dataset is sourced from the GDELT Project and focuses on climate change discussions in television news. It covers BBC News (2017–2020) and CNN, MSNBC, and Fox News (2009–2020). The dataset includes approximately 95,000 instances where climate change is mentioned, along with the text of the surrounding 15-second segment for each mention. More information about the dataset can be found here: https://blog.gdeltproject.org/a-new-dataset-for-exploring-climate-change-narratives-on-television-news-2009-2020/ .
- **climate_related_news_around_world_translated_to_english.csv** :
This dataset is also sourced from the GDELT Project and focuses on multilingual news headlines that mention climate change. It spans the period from 2015 to 2020 and covers 63 languages. The original dataset contains over 4 million instances, which is beyond the scope of this course. We therefore randomly sampled 5,000 data points for use in this study. As the news headlines were originally written in multiple languages, they were translated into English for the purposes of the course using an automated translation tool ([https://pypi.org/project/deep-translator/#google-translate-1](https://pypi.org/project/deep-translator/#google-translate-1)). More information on the dataset can be found here: [https://blog.gdeltproject.org/a-new-multilingual-dataset-for-exploring-climate-change-narratives-4-1-million-news-urls-in-63-languages-2015-2020/](https://blog.gdeltproject.org/a-new-multilingual-dataset-for-exploring-climate-change-narratives-4-1-million-news-urls-in-63-languages-2015-2020/) .
- **retweet_week_num09_May-03-19.csv , retweet_week_num14_Jun-07-19.csv , retweet_week_num18_Jul-02-19.csv , retweet_week_num27_Sep-06-19.csv** :
This dataset is drawn from From Chambers to Echo Chambers: Quantifying Polarization with a Second-Neighbor Approach Applied to Twitter’s Climate Discussion by Kolić et al. 2025 ([https://arxiv.org/abs/2206.14501](https://arxiv.org/abs/2206.14501)). It consists of weekly anonymised retweet networks related to climate change throughout 2019. Due to the scale of the full dataset, we retain only retweet networks from the first week of each summer month (May–September). The dataset includes network structure only; no information about the textual content of the tweets is provided. 
- **tweets_with_topics.csv** :
To complement the retweet network data, we also include a dataset from Effrosynidis et al. 2022 ([https://data.mendeley.com/datasets/mw8yd7z9wc/2](https://data.mendeley.com/datasets/mw8yd7z9wc/2)). The original dataset spans more than 13 years and contains over 15 million climate-related tweets. For the purposes of this course, we retain a random sample of 5,000 instances. Although the tweet text itself is not included, the dataset provides rich metadata, including sentiment, topic assignment and stance.


### Housing

This topic focuses on the housing crisis in Scotland, combining public discourse, political debate, and official statistics.

```
housing
  ├── housing_discussions_reddit
  │   ├── edinburgh_rent_comments.csv
  │   ├── edinburgh_rent_edges.csv
  │   ├── edinburgh_rent_nodes.csv
  │   └── edinburgh_rent_posts.csv
  │
  ├── rental_prices
  │   ├── 1bed_rental_prices_around_scotland.csv
  │   ├── 1bed_shared_rental_prices_around_scotland.csv
  │   ├── 2bed_rental_prices_around_scotland.csv
  │   ├── 3bed_rental_prices_around_scotland.csv
  │   ├── 4bed_rental_prices_around_scotland.csv
  │   └── rental_prices_for_scotland_overall.csv
  │
  ├── scottish_parliament_housing_discussions
      └── scottish_parliament_housing_discussions.csv

```

#### What you can explore?

- How people discuss rent and housing in Scotland on Reddit
- Changes in rental prices over time and across regions of Scotland
- How housing and rent are debated in the Scottish Parliament

#### Key Datasets

- **edinburgh_rent_comments.csv, edinburgh_rent_edges.csv , edinburgh_rent_nodes.csv , edinburgh_rent_posts.csv** :
This dataset contains the 1,000 most recent posts from the r/Edinburgh subreddit with the word “rent” in the title, collected in Summer 2025. All posts and comments have been cleaned and preprocessed. The dataset includes post-level and comment-level metadata, along with corresponding nodelist and edgelist files representing the discussion network. Each post was manually reviewed to ensure relevance to housing-related topics (excluding unrelated rentals such as bikes or equipment).
- **1bed_rental_prices_around_scotland.csv, 1bed_shared_rental_prices_around_scotland.csv, 2bed_rental_prices_around_scotland.csv, 3bed_rental_prices_around_scotland.csv, 4bed_rental_prices_around_scotland.csv, rental_prices_for_scotland_overall.csv** :
These datasets are sourced from a Scottish Government report on private sector rental prices in Scotland covering the period 2010–2024. With the exception of the overall dataset, each file includes geographic data, dividing Scotland into its Broad Rental Market Areas (BRMAs). The overall dataset provides a time-series of rental prices for different property sizes. More information can be found here: https://www.gov.scot/publications/private-sector-rent-statistics-scotland-2010-to-2024/ .
- **scottish_parliament_housing_discussions.csv** :
This dataset contains transcripts of Scottish parliamentary discussions relating to rental prices. The discussions span the period January 2010 to May 2025 and were scraped directly from the Search What Was Said in Parliament website using Beautiful Soup. Further information about the data source can be found here: https://www.parliament.scot/chamber-and-committees/official-report/search-what-was-said-in-parliament .

### Political Polarisation

This topic examines political polarisation using social media data, networks, and comparative numerical indicators.

```
polarisation
  ├── brexit
  │   ├── early
  │   │   ├── mps_mention_nodelist_early.csv
  │   │   ├── mps_mentions_edgelist_early.csv
  │   │   ├── mps_retweet_edgelist_early.csv
  │   │   ├── mps_retweet_nodelist_early.csv
  │   │   └── twts_corpus_sample_early.csv
  │   │
  │   └── late
  │       ├── mps_mention_nodelist_late.csv
  │       ├── mps_mentions_edgelist_late.csv
  │       ├── mps_retweet_edgelist_late.csv
  │       ├── mps_retweet_nodelist_late.csv
  │       └── twts_corpus_sample_late.csv
  │
  ├── truth_social
  │   └── posts_with_all_attributes.csv
  │
  ├── twitter
  │   └── leaving space for Sandrine's US election data
  │
  └── western_europe_polarisation
      └── Dataset_of_ideological_polarization.csv
```


### What you can explore?
- Polarisation in online political networks
- Differences between early and late phases of political debates
- Political communication in ideologically aligned platforms
- Long-run trends in ideological polarisation across countries

#### Key Datasets

- **mps_mention_nodelist_{early|late}.csv , mps_mentions_edgelist_{early|late}.csv, mps_retweet_edgelist_{early|late}.csv, mps_retweet_nodelist_{early|late}.csv, twts_corpus_sample_{early|late}.csv** :
This dataset contains Twitter networks of MPs, where posts are retweeted either by other politicians or by members of the public. The aim is to explore patterns of polarisation, examining whether users tend to retweet within their own ideological circles. The original dataset includes 100,000 retweets. To make the networks more manageable for students, I randomly selected two one-month periods (one from the beginning and one from the end of the dataset’s timespan) and retained only the network information from these windows (labelled early and late, respectively). The materials include retweet networks, mention networks, and the retweet data. I plan to extend these datasets with tweet-level analyses (e.g. sentiment analysis). Feedback on these particular datasets would be especially welcome.
- **posts_with_all_attributes.csv** :
This dataset is drawn from my research on Truth Social and contains posts made by American politicians on the platform. It includes metadata at the politician level, along with post-level attributes such as the presence of fear or hate speech and the emotions expressed in each post (anger, fear, sadness, joy, and surprise). The dataset offers students an opportunity to analyse political discourse within a highly ideologically aligned social media environment.
- **Sandrine's US Election Data** :
Leaving space for Sandrine's US election twitter data.
- **Dataset_of_ideological_polarization.csv** :
This dataset provides numerical measures of ideological polarisation in Western Europe since 1945. It is based on expert survey assessments of parties’ left–right placements and applies Dalton’s Polarisation Index (2008) to convert these into quantitative values. The dataset covers 20 Western European countries over the period 1945–2023, encompassing 398 parliamentary elections and legislatures. The data originates from Vincenzo et al. (2023) and is discussed further here: https://search.gesis.org/research_data/SDN-10.7802-2592?doi=10.7802/2592 .







