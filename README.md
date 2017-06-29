# resume-matcher

Ranking CVs against JDs.

# About Generated Word@Vec Word Embeddings

- Each word is represented as a **300-sized numpy array.** :saxophone:

- Trained against ***stackoverflow***:star: data dump (in xml).

- Collected ***1237328 word types*** from a ***corpus of 565919447 raw words*** and ***32701720 sentences.*** :heavy_exclamation_mark:

- Running time ~3hrs. :hourglass_flowing_sand:

- Most of the text preprocessing was already completed earlier.

- For more details see **model-stuff** below.

# Directory details

## model-stuff/

- **Successfully trained the word2vec model on stackoverflow data !! 🌞**

- The code is present as ***Word2Vec Model Training.ipynb*** notebook. The model is saved in model/ subdirectory (locally).

- **sample_bitcoin.stackexchange_paras.txt** is the paras.txt(paragraph in html tags) file for bitcoin.stackexchange.com subdirecory of the dataset. It was generated from bitcoin.stackexchange.com/Posts.xml using the code in ***paragraph_extraction_from_Posts.xml.ipynb*** notebook.

- **sample_bitcoin.stackexchange_sentences.txt** is the sentences.txt (pure sentences) file for bitcoin.stackexchange.com subdirectory of the dataset. It was generated from the corresponding paras.txt generated earlier using the code in ***sentence_extraction_from_paras.txt.ipynb***. The process took around 12.5 hours to complete.

## data

- ***raw_data/*** : contains collected CVs

- ***collectCV.py*** : While this program is running, every new text copied to clipboard is saved as a CV in **raw_data/** directory in text format.

- ***jd.csv*** : This program is to filter the Job Descriptions, only for IT positions from the Kaggle dataset here: https://www.kaggle.com/c/job-salary-prediction/data.
