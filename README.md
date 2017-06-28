# resume-matcher

Ranking CVs against JDs.

## model-stuff/

- The target is to get simple English sentences out of the gigantic stackexchange dataset(~40GB), which will be fed into the model training for word2vec.

- A sample of training was added as ***sample-model-training.ipynb***

- **sample_bitcoin.stackexchange_paras.txt** is the paras.txt(paragraph in html tags) file for bitcoin.stackexchange.com subdirecory of the dataset. It was generated from bitcoin.stackexchange.com/Posts.xml using the code in ***paragraph_extraction_from_Posts.xml.ipynb*** notebook.

- **sample_bitcoin.stackexchange_sentences.txt** is the sentences.txt (pure sentences) file for bitcoin.stackexchange.com subdirectory of the dataset. It was generated from the corresponding paras.txt generated earlier using the code in ***sentence_extraction_from_paras.txt.ipynb***. The process took around 12.5 hours to complete.

## data

- ***raw_data/*** : contains collected CVs

- ***collectCV.py*** : While this program is running, every new text copied to clipboard is saved as a CV in **raw_data/** directory in text format. 

- ***jd.csv*** : This program is to filter the Job Descriptions, only for IT positions from the Kaggle dataset here: https://www.kaggle.com/c/job-salary-prediction/data.
