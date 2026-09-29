# Analytical Summary: Topic Evolution and Classification Analysis of Beijing PM2.5 Air Quality

## Overview

This project presents an end-to-end **Natural Language Processing (NLP) and environmental data analytics pipeline** for discovering latent environmental patterns and analyzing their evolution over time using the **Beijing PM2.5 Air Quality Dataset**.

The project combines traditional statistical topic modeling with modern transformer-based semantic modeling to investigate relationships between air pollution, meteorological conditions, pollution categories, and temporal environmental patterns.

The central objective is to transform structured air-quality measurements into textual environmental descriptions and apply **BERTopic and Latent Dirichlet Allocation (LDA)** to identify meaningful latent topics. These topics are subsequently analyzed across time, seasons, pollution levels, and meteorological conditions.

The project therefore integrates:

- Environmental data preprocessing
- Feature engineering
- Text generation from structured sensor measurements
- NLP preprocessing
- Transformer-based topic modeling
- Traditional LDA topic modeling
- Topic coherence evaluation
- Model comparison
- Temporal topic evolution
- Pollution-level classification
- Meteorological correlation analysis
- Seasonal and hourly pollution analysis
- Topic-environment relationship analysis
- Visualization and result export

---

## Project Objectives

The major objectives of this project are:

1. **Analyze Beijing PM2.5 air-quality data** across time and environmental conditions.
2. Transform numerical environmental measurements into structured textual descriptions suitable for NLP-based analysis.
3. Discover latent environmental patterns using **BERTopic**.
4. Compare transformer-based BERTopic models with traditional **LDA topic models**.
5. Optimize topic-model configurations using **topic coherence** as a quality measure.
6. Examine how discovered topics evolve across different time periods.
7. Investigate relationships between environmental topics and pollution levels.
8. Analyze correlations between PM2.5 concentrations and meteorological variables.
9. Identify seasonal and time-of-day pollution patterns.
10. Produce interpretable visualizations and export analytical results for further research.

---

## Dataset

The project uses the **Beijing PM2.5 Air Quality Dataset**, covering hourly observations from **2010 to 2014**.

The dataset contains environmental measurements including:

| Feature | Description |
|---|---|
| `year` | Year of observation |
| `month` | Month of observation |
| `day` | Day of observation |
| `hour` | Hour of observation |
| `pm2.5` | PM2.5 concentration |
| `DEWP` | Dew point |
| `TEMP` | Temperature |
| `PRES` | Atmospheric pressure |
| `cbwd` | Combined wind direction |
| `Iws` / `IWS` | Cumulated wind speed |
| `Is` | Cumulated hours of snow |
| `Ir` | Cumulated hours of rain |

The notebook loads the dataset from the UCI Machine Learning Repository and includes a fallback mechanism for generating synthetic environmental data if the external dataset cannot be loaded.

---

## Analytical Framework

The project follows a multi-stage analytical workflow.

```text
Beijing PM2.5 Dataset
        │
        ▼
Data Loading & Validation
        │
        ▼
Data Cleaning & Missing-Value Handling
        │
        ▼
Feature Engineering
        │
        ├── Date/Time Features
        ├── Seasonal Features
        ├── Time-of-Day Features
        └── Pollution Categories
        │
        ▼
Environmental Text Generation
        │
        ▼
Text Preprocessing
        │
        ▼
Time-Window Creation
        │
        ▼
Topic Modeling
        │
        ├───────────────┐
        ▼               ▼
    BERTopic           LDA
        │               │
        └───────┬───────┘
                ▼
        Topic Coherence
        & Model Comparison
                │
                ▼
        Best Configuration
                │
        ┌───────┼────────┐
        ▼       ▼        ▼
   Topic      Topic    Environmental
 Evolution  Distribution  Analysis
        │       │        │
        └───────┼────────┘
                ▼
       Final Environmental
             Insights

### A small correction I recommend

Your notebook filename says **“Topic Evolution and Classification Analysis,”** but the classification part is primarily **pollution-level categorization**, not a conventional supervised ML classifier such as Random Forest, SVM, or Logistic Regression. The README above deliberately describes it as **pollution-level classification/categorization** rather than claiming that a supervised classifier was trained.

Also, I would **not put “Best Model: LDA_5” permanently in the README as an absolute conclusion** if you intend to keep experimenting. Your notebook has a second, enhanced comparison that evaluates multiple BERTopic configurations and LDA configurations. The README above therefore describes `LDA_5 / 0.951` as the **reported result in the analytical summary**, while explaining that the enhanced framework performs its own comparison. This keeps your GitHub documentation scientifically defensible.
