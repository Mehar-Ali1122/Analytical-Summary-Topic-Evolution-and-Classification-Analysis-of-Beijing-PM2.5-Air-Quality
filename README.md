# Analytical Summary: Topic Evolution and Classification Analysis

## About the Project

This project presents an analytical study of **Beijing PM2.5 air-quality data** using Natural Language Processing (NLP), topic modeling, statistical analysis, and data visualization techniques.

The main objective is to identify meaningful environmental patterns from air-quality observations and investigate how these patterns vary across different time periods, pollution levels, seasons, and meteorological conditions.

The project combines **BERTopic** and **Latent Dirichlet Allocation (LDA)** to discover latent topics from environmental data. The topic-modeling approaches are evaluated using topic coherence, allowing their results to be quantitatively compared.

## Objectives

- Analyze Beijing PM2.5 air-quality data.
- Explore temporal and environmental pollution patterns.
- Transform structured environmental observations into text representations.
- Apply BERTopic for semantic topic discovery.
- Apply LDA as a traditional topic-modeling baseline.
- Compare different topic-model configurations using coherence scores.
- Analyze topic evolution over time.
- Investigate the relationship between topics and pollution levels.
- Examine relationships between PM2.5 and meteorological variables.
- Analyze seasonal, monthly, hourly, and time-of-day pollution patterns.
- Generate visualizations and export analytical results.

## Dataset

The project uses the **Beijing PM2.5 Air Quality Dataset**, containing hourly air-quality and meteorological observations.

Important variables include:

- `year` – Year of observation
- `month` – Month of observation
- `day` – Day of observation
- `hour` – Hour of observation
- `pm2.5` – PM2.5 concentration
- `DEWP` – Dew point
- `TEMP` – Temperature
- `PRES` – Atmospheric pressure
- `cbwd` – Combined wind direction
- `Iws` – Cumulated wind speed
- `Is` – Cumulated hours of snow
- `Ir` – Cumulated hours of rain

## Methodology

The analytical workflow consists of the following major stages:

1. Data loading and validation
2. Data cleaning and missing-value handling
3. Date and time feature construction
4. Environmental feature engineering
5. Pollution-level categorization
6. Conversion of numerical observations into environmental text descriptions
7. NLP preprocessing
8. Time-window construction
9. BERTopic modeling
10. LDA topic modeling
11. Topic coherence evaluation
12. Model comparison
13. Topic evolution analysis
14. Environmental and pollution analysis
15. Meteorological correlation analysis
16. Visualization and result export

## Topic Modeling

### BERTopic

BERTopic is used to discover semantic topics from environmental observations.

The workflow uses transformer-based sentence embeddings together with dimensionality reduction, clustering, and topic representation techniques.

The project evaluates different embedding and UMAP configurations to investigate their influence on topic discovery.

### Latent Dirichlet Allocation

LDA is implemented as a traditional probabilistic topic-modeling baseline.

Different numbers of topics are evaluated, including:

- LDA with 5 topics
- LDA with 10 topics
- LDA with 15 topics

## Model Evaluation

Topic-model quality is evaluated using **topic coherence**.

The project compares the coherence of different BERTopic and LDA configurations and identifies configurations with stronger topic-word coherence.

The analytical results reported in the notebook include an LDA configuration with 5 topics achieving a coherence score of approximately **0.951**.

## Topic Evolution Analysis

The discovered topics are analyzed across time to investigate how environmental patterns change throughout the study period.

The analysis includes:

- Monthly topic distributions
- Topic frequency trends
- Temporal topic patterns
- Topic-environment relationships

## Environmental Analysis

The project investigates relationships between discovered topics and environmental variables, including:

- PM2.5 concentration
- Temperature
- Humidity
- Wind speed
- Atmospheric pressure
- Dew point
- Precipitation

Pollution levels are also categorized to facilitate analysis of topic distributions under different pollution conditions.

## Temporal Analysis

The project analyzes PM2.5 and topic patterns across:

- Seasons
- Months
- Hours of the day
- Different time periods

These analyses help identify temporal variations in air-quality conditions.

## Visualizations

The project generates several visualizations, including:

- PM2.5 distributions
- Pollution-level distributions
- Topic distributions
- Topic evolution plots
- Topic coherence comparisons
- Topic similarity visualizations
- Topic-environment heatmaps
- Seasonal analysis
- Monthly PM2.5 trends
- Hourly pollution patterns
- Meteorological correlation matrices

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn
- BERTopic
- Sentence Transformers
- Gensim
- UMAP
- HDBSCAN
- Google Colab

## Project Structure

```text
Analytical-Summary-Topic-Evolution-Classification/
│
├── Analytical_Summary_Topic__Evolution__Classification__Analysis_.ipynb
└── README.md
