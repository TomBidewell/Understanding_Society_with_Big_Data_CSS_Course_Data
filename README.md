# Breakdown of Current Data

This README briefly describes each of the datasets provisionally included in the list of materials available to students for the Understanding Society with Big Data first year course. 

The documentation presented here is for the organisers of the course only. A more detailed and professional documentation will be created for the students before the course.

## Topics

The datasets are currently split into 3 main topic areas (Climate Change, Housing, and Polarisation). Before the start of the course, I would like to add one topic on music and another potentially on sports washing.


### Climate Change

Folder Structure:

The datasets for this topic explor climate change through four angles: using empirical data, google search trends, discussions in the news, discussions on Twitter. There is a range of types of data (numerical, text, network) and should provide the students with interesting and different angles to climate change.

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

Data Sources:

- **global_temperatures.csv, northern_hemisphere_temperatures.csv, southern_hemisphere_temperatures.csv** : 
This data originates from the NASA GISS Temperature Analysis (GISTEMP v4). The values are an estimate of the global surface temperature change derived from land-surface, air and sea-surface water temperature anomalies. This data provides temperature change values on the global scale as well as for the Northern and Southern Hemispheres. This data is downloaded from: https://www.kaggle.com/datasets/sujaykapadnis/global-surface-temperatures .

- **natural_emergencies.csv** :
This data records natural disasters and emergencies around the world from 2004-2025. The data came from the Emergency Events Database (EM-DAT) from the Centre for Research on the Epidemiology of Disasters. For further details, see: https://www.emdat.be .

- **sea_level_change.csv** :
This data is from NASA's Sea Surface Height project (NASA-SSH) and reports a time series of globally-averaged sea level change in centimetres from 1993 to the present day. More information on the project and the data can be found at the following links: https://podaac.jpl.nasa.gov/NASA-SSH , https://earth.gov/sealevel/vital-signs/sea-level/ . 

- **popularity_of_climate_searching_by_city.csv , popularity_of_climate_searching_by_region.csv , popularity_of_climate_searching_by_time.csv** :
Search trends from Google for the terms "Climate Change" and "Global Warming" worldwide, US-only and UK-only. We also split by region and city as well as provide time series for search popularity over time. 

- **climate_related_news_in_english.csv** :
This dataset is sourced from the GDELT Project and focuses on climate change discussions in television news. It covers BBC News (2017–2020) and CNN, MSNBC, and Fox News (2009–2020). The dataset includes approximately 95,000 instances where climate change is mentioned, along with the text of the surrounding 15-second segment for each mention. More information about the dataset can be found here: https://blog.gdeltproject.org/a-new-dataset-for-exploring-climate-change-narratives-on-television-news-2009-2020/ . 

- **climate_related_news_around_world_translated_to_english.csv** :
This dataset is also sourced from the GDELT Project but instead focuses on multilingual news titles mentioning climate change. The data spans 2015-2020 and covers 63 languages. The original dataset contains over 4 million instances so I randomly sampled 5000. To create English text for the students to read, I then translated the titles using deep_translator (https://pypi.org/project/deep-translator/#google-translate-1). I have not conducted formal tests for translation accuracy, beyond basic sanity checks comparing the outputs with Google Translate, which produced very similar results. While these translations may not be perfect, they offer a reasonable starting point for students to explore a multilingual and global dimension of climate change. More information on the dataset can be found here: https://blog.gdeltproject.org/a-new-multilingual-dataset-for-exploring-climate-change-narratives-4-1-million-news-urls-in-63-languages-2015-2020/ . 

- **retweet_week_num09_May-03-19.csv , retweet_week_num14_Jun-07-19.csv , retweet_week_num18_Jul-02-19.csv , retweet_week_num27_Sep-06-19.csv** :
This dataset is from the paper “From Chambers to Echo Chambers: Quantifying Polarization with a Second-Neighbor Approach Applied to Twitter’s Climate Discussion” by Kolić et al., 2025 (https://arxiv.org/abs/2206.14501). It contains weekly anonymised retweet networks discussing climate change throughout 2019. For manageability, I have selected retweets from the first week of each summer month (May, June, July, August, and September). Due to anonymisation, no information on the actual tweets is provided. Despite this, the dataset offers a clean resource for exploring network science concepts. One limitation is that the networks are still relatively large, which may be challenging for course exercises. I might do community detection over these networks and then sample from within these communities to reduce the size but keep the network's structure.

- **tweets_with_topics.csv** :
To complement the retweet networks, which do not include the content of tweets, we have also included a dataset from Effrosynidis et al., 2022 (https://data.mendeley.com/datasets/mw8yd7z9wc/2). This dataset spans over 13 years and contains more than 15 million climate-related tweets. While the actual tweet text is not provided, the dataset includes metadata such as sentiment, topic assignment, stance, and aggressiveness. This allows students to analyse the content and characteristics of climate discussions on Twitter, and when combined with the retweet networks above, provides a comprehensive resource for drawing insights about both network structure and tweet-level dynamics.


### Housing

Folder Structure:

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
  │   └── scottish_parliament_housing_discussions.csv
  │
  └── slurp
      └── data not here yet 
```

### Polarisation

Folder Structure:

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
    
