# ada-2023-project-adavengers2023
ada-2023-project-adavengers2023 created by GitHub Classroom

During this project we will use the CMU Movie Summary Corpus available at http://www.cs.cmu.edu/~ark/personas/. 

## Title: Exploring the Evolution of Female Characters in Cinema Across Different Eras with the CMU Movie Summary Corpus. 

## Abstract

Our project aims to critically examine the portrayal of female characters in cinema. Driven by the movies‘ profound cognitive influence, our objective is to explore how depictions of women evolve with time and to identify any existing biases or subtle forms of discrimination.

To achieve this, we will investigate the differences in commonly used adjectives that appear alongside male or female characters in movie summaries. We will also study the characteristics of female characters across different movie genres, tracing how their portrayals have transformed in line with the rising tide of the feminist movement. 

This study is fueled by the increasing societal focus on gender representation in media. By scrutinizing historical and character-level data, we aim to reveal trends in the depiction of women in film, thereby mirroring broader societal shifts.

The data story can be found here : https://ariane-augustoni.github.io/Women_and_movies/overall

### Research Questions

1. **Female Character Identities in Synopses:**
    - Do movie summaries use different adjectives for women and men?  What personality traits are typically attributed to them? What implicit meanings are conveyed through adjectives used for women?
    - What are common identities, professions, and relationship statuses for female characters?
    - （try to use word co-occurrence networks effectively to visualize this data）
2.  **Female Characters in Different Genres and Themes:**
    - What are ratios of female characters in different genres?
    - What character types do female characters have most often (using the tv tropes)?
3. **Evolution of Female Protagonists:**
    - Did the amount of movies starring female protagonists change over time?
    - Were there specific periods of significant change linked to historical events?
    - How have the adjectives representing women changed over time? 

### Methods

### 1. **Female Character Identities in Synopses:**

**Data Preprocessing:**

Clean the text data by removing punctuation, numbers, and meaningless filler words (like "the," "is," "and," etc.). Tokenize the text, splitting it into individual words, and removing stopwords. Part-of-speech tagging, using natural language processing tools (NLTK was used) to identify the grammatical parts of each word, particularly adjectives.

**Extracting :**

Extract adjectives/profession/identities/relationship status based on the results of part-of-speech tagging.

**Building Word Embeddings:**

Use the pre-trained word embedding model Word2Vec to obtain vector representations for each target word (including adj. in the whole corpus and the word representing gender such as "he," "she," "man," "woman,").

**Calculating Distances:**

For each adjective vector showing in the whole text (or we can choose those we are interested in), calculate the average cosine distance to the representative vectors of male and female gender words.

**Quantifying Gender Bias:**

Identify bias by comparing the distance differences of adjectives to the two sets of gender word vectors. The proximity of adjectives to a gender word vector set may indicate a bias towards that gender.

**Statistical Analysis:**

Select the top hundred adjectives closest to each gender based on cosine similarities.

Set a defined time period (for example, five or ten years as a cycle) and repeatedly calculate to analyze the changes in high-frequency adjectives over time.

Do a flat soft clustering of words using their cosine distance and look if some clusters are more associated 

**Interpretation of Results:**

Analyze the semantic content of these adjectives to see if they conform to traditional gender stereotypes.

### 2. **Female protagonists in Different Genres and Themes:**

**Character Identification**: Identify all female characters in each synopsis, assess if there are at least two female characters and compare movies that pass vs. fail this criterion.

**Genre Classification**: Classify movies into genres/themes.

**Character Role Analysis**: Identify and categorize the roles played by women in these movies.

**Stereotype Analysis**: Analyze the roles for stereotypes and biases.

**Comparative Genre Analysis**: Compare the prevalence and types of female protagonists across genres.

### 3. Evolution of Female Protagonists Over Time

**Proportion Analysis:** Define who is the protagonist according to the frequency in the movies. Examine changes in the frequency of the female characters over time. 
Calculate the rate of female protagonists movies among all movies and examine the changes. 

**Role Evolution Analysis**: Examine how the representation of females in movies has changed over the years.  

### Proposed Timeline

**November 17-23:** 

Finish data exploration

**November 23-30:**

Finish statistical analysis, check each others parts

**December 1-14:**

Do visualizations/ Do data story and web interface

**December 14-22:**

Revise and improve data story

### Organization within the Team

Heling: Question 1, Discovery data analysis

Shu: Question 1, Discovery data analysis

Caroline: Question 2, Harmonizing Data story

Irem : Question 3, Harmonizing Data story

Ariane : Question 3, Web interface and turning plots into interactive plots  


## References
1.Learning Latent Personas of Film Characters
David Bamman, Brendan O'Connor, and Noah A. Smith
ACL 2013, Sofia, Bulgaria, August 2013 
