Data science capstone project: Final submision
========================================================
author: YE
date: 2016-10-01
autosize: true

1- Description of the app: How it works?
========================================================

The main goal of the application is to predict the next word you could type in.

## How to use it?

1. Click on: <https://ryves.shinyapps.io/DatascienceCapstone/>
2. Wait about 30 seconds while the initialization is runing. 
3. Type in words inside the texarea 
4. The application will suggest 5 words to complete your sentence.
5. If one of the 5 suggestions matches, you can select it by clicking on it.


2- Algorithm design: Getting and cleaning data
========================================================
The first thing was to get, clean and understand the data. For this task, I decide to use the "TM" package.
The main steps was:

1. Load data as a CORPUS
2. Get some features like the name of each file, the number of lines in each file,...
3. Cleaning: remove ponctuation, remove numbers, strip white spaces,...
4. Save each file on a new directory.

3- Algorithm design: Sampling, tokenization and "Ngramification"
========================================================
After cleaning data, to build an application which can run on SHINY, I decide to sample 10000 lines in each file. After that:

1. "Tokenization" of each TXT file.
2. "Ngramification" of each file: 1-gram, 2-grams, 3-grams and 4-grams
3. I combine all "UNIGRAMS" files in one data frame and counting every occurence of each "UNIGRAM"
4. I repeat the same process for "BIGRAMS", "TRIGRAMS" and "QUAGRAMS"

4- Algorithm design: Prediction model
========================================================
The model is based on the "MAXIMUM LIKELIHOOD ESTIMATION" method. It uses the conditional probality of seeing word "Wn" by using counts from a corpus:

P(Wn|W1...Wn-1) = c(W1...Wn)/c(W1...Wn-1).

## How about unseen n-grams?

The smoothing method I used in this app is "BACKOFF".

The principle consists on: 

P(Wi|Wi-3 Wi-2 Wi-1) = a1*P(Wi|Wi-3 Wi-2 Wi-1) + a2*P(Wi|Wi-2 Wi-1) + a3*P(Wi|Wi-1) + a4*P(Wi)

I fixed a1=0.9, a2=0.6, a3=0.3 and a4=0.1

5- Improvements
========================================================

1- The use of external sources: To avoid spelling mistakes, a dictionnary can be useful

2- Personnalization: We all have a personal writting style, to adapt the application to each one, I have add machine learning mechanisms
