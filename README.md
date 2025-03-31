# AI-Powered Behavioral Analysis for Suicide Prevention, Substance Use, and Mental Health Crisis Detection with Longitudinal Geospatial Crisis Trend Analysis
# **Description**

Public health agencies and crisis service providers face challenges in detecting and addressing emerging suicide, substance use, and mental health crises in real time. Traditional public health data sources—such as hospital admissions, overdose reports, and crisis hotline statistics—are valuable but lag behind the actual emergence of crises within communities. This project proposes an AI-driven public health monitoring system that integrates:

**Behavioral tracking** – Analyzing how individuals engage with crisis-related content to identify patterns of distress escalation.

**Crisis-related language analysis** – Detecting keywords, slang, and coded language used to discuss mental health struggles, suicidality, and substance use.

**Geospatial crisis mapping with longitudinal trend analysis** – Identifying where distress-related discussions are concentrated and tracking changes over time to detect increasing crisis trends within specific geographic regions. By collecting and analyzing this data over time, this system will provide early-warning indicators of worsening mental health conditions and emerging substance use risks in communities.

These insights can help service providers predict areas of growing crisis and proactively allocate resources to where they are needed most.

# Task Name:
Human AI Project Tests for Prospective GSoC 2025 Applicants

# Approaching the Task:
**Data Extraction:**
Used Reddit API (PRAW) to extract posts related to mental health crises.
Filtered posts based on specific keywords (e.g., "depressed," "suicidal," "addiction help").
Collected metadata: Post ID, Timestamp, Text, Upvotes, Comments.

**Preprocessing & Cleaning:**
Removed stopwords, emojis, special characters, and converted text to lowercase.
Cleaned and stored the dataset in CSV format for further analysis.

**Sentiment & Risk Classification:**
Applied TextBlob for sentiment classification (Positive, Neutral, Negative).

**Created crisis lexicons to categorize posts into risk levels:**
High-Risk: Explicit crisis language.
Moderate Concern: Help-seeking behavior.
Low Concern: General discussions.
Tagged posts with appropriate sentiment and risk levels.

**Geolocation Extraction:**
Extracted location names from text using NLP (SpaCy).
Implemented regex-based pattern matching for place detection.

**Geocoding with OpenCage API:**
Used OpenCage API to convert locations into latitude and longitude coordinates.
Cached results to reduce repetitive geocoding requests.

**Heatmap Visualization:**
Generated an interactive heatmap using Folium.
Displayed crisis hotspots based on post density.
Identified top 5 locations with the highest crisis discussions.

**Longitudinal Analysis:**
Conducted time-series analysis to track crisis trends over time.
Visualized regional distress patterns by location and date.

This systematic approach ensured efficient data extraction, crisis classification, and geospatial visualization for mental health crisis detection using Reddit API. 

# Future endeavours

**Real-Time Crisis Monitoring System:**Develop a real-time dashboard for continuous monitoring of crisis discussions.
Integrate streaming data pipelines (e.g., Kafka, Apache Spark) for live post ingestion.
Display dynamic heatmaps and risk patterns in real time.

**Improved Geolocation Accuracy:**
Implement NLP-based location disambiguation to resolve ambiguous place names.
Use Google Maps API or Mapbox for more accurate and detailed geocoding.
Add country and region-level mapping for broader trend analysis.

**Advanced Topic Modeling:**
Use LDA (Latent Dirichlet Allocation) or BERTopic for topic modeling.
Identify emerging crisis trends by extracting latent topics from disussions.
Visualize topic trends over time using interactive plots.

**Sentiment and Emotion Analysis:**
Expand classification to include emotion detection (e.g., anger, sadness, fear).
Use multiclass sentiment classifiers (e.g., DistilBERT) for nuanced emotion taging.
Visualize emotion heatmaps across locations.




