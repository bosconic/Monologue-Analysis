# Monologue-Analysis
1. By: Nicholas Bosco
2. Topic: Monologue Sentiment Analysis

This is the associated `README.md` file that accompanies the Monologue Sentiment Analysis Python Notebook (.ipyb)

# Background Information

The idea for the project is to compare six monologues from three different plays. The question: can you analyze the monolgoues solely on the words themselves to see if a particular monologue is meant for a particular gender identity? When reading *The actors book of Classical Monologues* Collected and introduced by Stefan Rudnicki [^1], he had suggested that for the actors who were interested in acting and have to do auditions, the actors can refer to the particular section to try and act out the monologue. He also mentioned that this was in no way to constrain female and male actors to solely the gender identity of the characters. I just throught it would be interesting if there can be a different interpretation to how Stefan Rudnicki divided the book. This work is my first introduction to Natural Language Processing (NLP) as I do enjoy reading I thought to combine my passion for the arts and literature with a data science perspective. Potentially there may be some insights drawn here that may have the reader consider how they view monologues in general. A large part of my knowledge and understanding of NLP was thanks to P. J. Deitel and H. M. Deitel's chapter: *Chapter 12: Natural Language Processing* in Intro to python for computer science and data science: Learning to program with AI, Big Data and The Cloud [^2].

[^1]: S. Rudnicki, The actor's Book of classical monologues. New York, NY: Penguin Books, 2009.
[^2]: P. J. Deitel and H. M. Deitel, “Natural Language Processing (NLP),” in Intro to python for computer science and data science: Learning to program with AI, Big Data and the cloud, Harlow: Pearson Education Limited, 2022.


## Inputs

The inputs for this project are the six .txt files that contain each of the monologues that went through two different kinds of sentiment analysis tests. The names of the monologues are mentioned within the text files. Another thing to mention when looking at the text files is that before the monologue begins I had added the source material of each monologue above, the monologue to ensure the reader knows where I had recieved the monologue from. I am unsure if the introduction affects the sentiment analysis of the monologues themselves but I thought to mention this here.


## Execution

The first sentiment analysis used the NLTK toolkit [^3] as well as the `punkt` lexicon. Second analysis relied on the Naive Bayes Analysis as well as the lexicon from the `movie reviews` library within the NLTK toolkit. After I had examined the code provided by my professor, I had tried to apply the neccessary findings that will ensure I complete the analysis of each monologue sucessfully. The code my seem repetative but it is important to see the process behind gathering the results per monologue as I had opted to read in six different text files containing monologues. I also wanted to visualize the results so I had to refer to the Pandas [^4] and mathplotlib [^5][^6] for the visualization help.

[^3]: K. Steven and E. Loper, title=Natural language processing with Python: analyzing text with the natural language toolkit. Reilly Media, Inc, 2009.
[^4]: “Pandas.dataframe.from_dict#,” pandas.DataFrame.from_dict - pandas 1.5.2 documentation. [Online]. Available: https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.from_dict.html. [Accessed: 15-Dec-2022].
[^5]: “Tutorials#,” Tutorials - Matplotlib 3.6.2 documentation. [Online]. Available: https://matplotlib.org/stable/tutorials/index.html. [Accessed: 15-Dec-2022]. 
[^6]: “Pyplot tutorial#,” Pyplot tutorial - Matplotlib 3.6.2 documentation. [Online]. Available: https://matplotlib.org/stable/tutorials/introductory/pyplot.html#sphx-glr-tutorials-introductory-pyplot-py. [Accessed: 15-Dec-2022]. 

## Output

The first sentiment analysis provides two scores Polarity and Subjectivity. Polarity is evaluated on a scale with the extremely negative sentiment score being -1.0 to 1.0 which is considered to be extremely positive sentiment score. Subjectivity is evaluated on a scale a 0.0 score means the corpus is completely objective and a score of 1.0 means the corpus is completely subjective. These scores are needed as it provides an over view to how the NLTK tool evaluates the corpus.

The second sentiment analysis provides a more in-depth polarity score per sentiment rating. By dividing the polarity scores into two parts `p_pos` means the sentiment polarity positivity score. and the `p_neg` means the sentiment polarity negativity score. Within the second sentiment analysis the code also classifies if the sentiment is typically positive or negative, which is a feature not included by the first analysis.

After I had collected all of the polarity scores, I wanted to generate a data frame of each character and the four categories (**polarity**, **subjectivity**, **sentiment polarity positivity score** and **sentiment polarity negativity score**). I decided to generate the dataframe by making a dictionary and then converting the dictionary per character with the four key's and their seperate values. Once I had accomplished this task all I had left was the visualization part.

For the visualizations I decided to make three different graphs: Polarity scores of monologues (bar graph), Sentiment polarity negativity score of monologues (scatter plot) and Sentiment Subjectivity score of monologues (bar graph). The process to generate the visualizations and data frame were a bit tricky as I am not as comfortable with the syntax for visualizations but I am proud of the result.

If you have made it this far, I appreciate your interest in the program and for the results.

# Acknowledgements

I would like to thank my professor, Dr. Maher Elshakankiri for providing great resources on the topic and letting me flourish and learn about NLP.

