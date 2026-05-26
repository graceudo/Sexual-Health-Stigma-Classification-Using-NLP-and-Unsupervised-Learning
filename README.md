# Sexual-Health-Stigma-Classification-Using-NLP-and-Unsupervised-Learning

Project Overview

This project explores how sexual health stigma is expressed within TikTok discussions using Natural Language Processing (NLP) and unsupervised machine learning techniques. Social media platforms increasingly act as spaces where users discuss HIV, sexually transmitted infections (STIs), symptoms, prevention methods, diagnosis experiences, and emotional wellbeing. While these discussions can encourage awareness and support, they may also contain misinformation, fear-driven narratives, judgement, and stigmatising language. The aim of this project was to develop a scalable NLP framework capable of identifying recurring themes, emotional patterns, and stigma-related discourse within large volumes of unstructured TikTok comments.

Objectives

The project aimed to classify and analyse sexual health discussions without relying on manually labelled data. Transformer-based semantic embeddings and unsupervised clustering methods were used to detect latent themes directly from the conversations. Additional objectives included identifying supportive versus stigma-related discussions, analysing emotional sentiment across clusters, examining audience engagement trends over time, and interpreting cluster meanings through qualitative analysis techniques such as keyword extraction and representative comment analysis.

Dataset and Preprocessing

The dataset consisted of TikTok comments collected from sexual health related videos using Apify. After preprocessing, the final dataset contained 1,162 unique comments. Cleaning steps included removing URLs, duplicate comments, excess whitespace, and empty entries while preserving emojis and conversational language patterns commonly found on TikTok. Timestamps were converted into datetime format to support temporal engagement analysis.

To measure audience interaction, a weighted engagement score was created using likes and replies. Logarithmic scaling was applied to reduce the impact of viral outliers while preserving meaningful engagement differences between comments.

Methodology

Semantic representations of comments were generated using Sentence Transformers, which converted each comment into a 384-dimensional embedding vector capable of capturing contextual meaning. These embeddings were clustered using the HDBSCAN algorithm, selected for its ability to handle noisy and highly variable social media text without requiring a predefined number of clusters.

Multiple parameter configurations were tested to optimise clustering quality. The final HDBSCAN configuration identified 12 semantic clusters while classifying approximately 68.6% of comments as noise or outliers, reflecting the highly diverse nature of online social media discourse. Clustering performance was evaluated using the Silhouette Score (0.3391) and Davies–Bouldin Index (2.1459).

Sentiment analysis was performed using the VADER sentiment lexicon from NLTK to examine emotional patterns across clusters. Temporal engagement analysis was also conducted to investigate how audience interaction changed over time across different discussion themes. Qualitative interpretation methods including TF-IDF keyword extraction, word clouds, and representative comment analysis were used to validate semantic coherence within clusters.

Key Findings

The results demonstrated that unsupervised NLP methods were effective for identifying meaningful themes within sexual health discussions. Several clusters reflected strong emotional support and empathy, containing phrases such as “thank you for sharing,” “god bless,” and “praying,” which also generated the highest engagement levels across the dataset. Other clusters revealed fear, anxiety, stigma, and symptom-related uncertainty, particularly surrounding HIV-related discussions.

Healthcare-oriented conversations were also identified, with clusters discussing HIV prevention methods, medication access, NHS services, and treatment advice. Temporal analysis showed that supportive discussions maintained relatively stable engagement over time, while emotionally sensitive or symptom-related conversations fluctuated more significantly.

The project demonstrated how transformer embeddings combined with density-based clustering can effectively identify nuanced emotional and semantic patterns within unstructured social media conversations.

Technologies Used
Python,
Sentence Transformers,
HDBSCAN,
NLTK (VADER Sentiment Analysis),
Scikit-learn,
Pandas,
NumPy,
Matplotlib & Seaborn,
TF-IDF Vectorisation, and
Apify.

Future Improvements

Future work could extend this research through multilingual analysis, automated stigma detection systems, topic modelling, network analysis, and larger cross-platform social media datasets. Additional work could also investigate supervised classification approaches for detecting harmful or misinformation-driven sexual health narratives in real time.
