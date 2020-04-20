# covid19_Question_Answer_model
COVID19: Question-Answering Model using BioSentVec Embedding
# Introduction 
  As we see COVID19 affected 2.5M people globally and 160k deaths, the worldwide AI research community are trying help medical community whatever the way we could. Many of medical questions are leads to research papers for answers. These questions are suitable for text mining, and developing text mining tools to provide insights on these questions.
	In this repo, I want to share how you can use BERT based embeddings pre-trained model can be used to build a text-based Question and Answering tool for fining answers related to Coronavirus from COVID19 research papers repository.
When I was with IBM, I involved a similar solution to IBM Risk Insights,[IBM Risk Insights](https://video.cube365.net/c/916244) which search for supply chain risks from the news articles, tweets, and weather data. Based on the base idea from the Risk Insights project and Biology knowledge domain for embeddings, I developed this model. With this model, users can search for research papers to find out and outputs related articles and which paper, under which section the user could find answers for the input question. Also, it displays the related paragraphs as output. It returns top article with highlighted answer sentences from the articles. My code is also uploaded to my Github
# Data
In response to the COVID-19 pandemic, the White House and a coalition of leading research groups have prepared the COVID-19 Open Research Dataset (CORD-19). CORD-19 is a resource of over 52,000 scholarly articles, including over 41,000 with full text, about COVID-19, SARS-CoV-2, and related coronaviruses.  This dataset is publicly available in [Kaggle’s  COVID-19 Open Research Dataset Challenge (CORD-19)](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge). I used only articles in the JSON format for this model. The dataset has 7865 articles in JSON format which contains 64,000 unique sections and 1.1M sentences. Also, it has articles metadata such as data published, authors, title, and abstract.
# Sentence Embedding
This solution primary for the medical domain so I used [BioSentVec](https://github.com/ncbi-nlp/BioSentVec) pre-trained model for embedding. BioSentVec created biomedical word and sentence embeddings using PubMed and the clinical notes from MIMIC-III Clinical Database. Both PubMed and MIMIC-III texts were split and tokenized using NLTK. We also lowercased all the words. More details and a pre-trained model can use accessed [here](https://github.com/ncbi-nlp/BioSentVec).
# Architecture
This solution is a type of Question Answering model. It is a retrieval-based QA model using embeddings.  The basic idea of this solution is comparing the question string with the sentence corpus, and results in the top score sentences as an answer. I create a vector representation of each sentence using a pre-trained BioSentVec embedding model and KNN to find the answer sentences.

More info visit my blog: https://rameshdatascientist.blogspot.com/2020/04/covid19-question-answering-model-based.html

	 
