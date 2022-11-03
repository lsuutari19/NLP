# Project 23. Personality trait
Course work for University of Oulu's Natural Language Processing course

## Instructions and requirements
The tasks are provided as .ipynb-files: please see the files tasks_tool1.ipynb, tasks_tool2.ipynb and tasks_tool3.ipynb for the tasks performed with the tools 1, 2 and 3, respectively. For more details, please see the report.

To run the scripts, the following libraries are required:
* pandas
* contractions
* nltk
* scikit-learn
* numpy
* plotly.

**Important note:** For tasks_tool1.ipynb and tasks_tool2.ipynb, the version 0.20.1 of scikit-learn should be used. However, for tasks_tool3.ipynb, the version 0.22.1 is required.

## Specification

### 1
Write a script that gathers and concatenates the scripts corresponding to each character to make up a separate corpus for each character, and determine the characteristics of each corpus in terms of number of tokens, size of vocabulary, average length of individual script, standard deviation of script length, proportion of stopwords employed. Provide the results in a table to visualize the discrepancy among the various characters. 

### 2
We want to compare the various characters in terms of their personality traits, especially, the big-five personality traits (Openness, Consciousness, Extraversion, Agreeableness and Neuroticism). For this purpose, we rely on some existing implementations that infer from the text the corresponding personality trait. We may refer to some existing implementations in https://github.com/topics/personality-traits. For instance, you may use popular MELD or SenticNet. Study two of the provided implementations, and suggest a script that input the whole corpus of a given character and then outputs the scores assigned to each personality trait (a vector of five dimension). Use PCA to reduce the dimension of the outputted file into 2D dimension and then provide a graphical illustration (2D space) where each character is represented as a doc. Identify the characters that are close to each other in terms of personality traits.

### 3
Repeat the 2) when using the cosine similarity of the five-personality vector scores of each pair of characters as metric to quantify how the two characters are close in terms of their personality. Draw the corresponding character matrix similarity.

### 4
Repeat 2-3) when using the alternative implementation (e.g., SenticNet, MELD,..).
Now we want to track the personality of trait of a given character at a local level, not after aggregating all its scripts. For this purpose, write a script that, for each script, it generates the corresponding five personality vector, and saves it in a database file.

### 5
Now we want to evaluate the consistency of each character in terms of personality generated. For this purpose, assume that a given character is assigned the personality trait corresponding to the highest personality trait score. We evaluate the consistency of the character’s personality by the extent to which the  dominating personality trait is invariant across the different scripts. Suggest an expression and a script that allows you to quantify this intuition, and compare the characters accordingly. 

### 6
Consider the sentiment of every script of each character according to Vader sentiment analyzer. We want to test whether a given personality trait is associated with a given sentiment polarity. Write a script that calculates the overall sentiment score (arithmetic sum of positive and negative sentiment score) of each script and associate this with the personality trait that corresponds to the highest personality trait score. For each character, generate a histogram that shows for each personality trait, the proportion of positive sentiment and proportion of negative sentiment associated to each personality trait that occurred in character’s script.

### 7
Identify relevant literature to justify the findings and comment on the limitations of the approach.   
