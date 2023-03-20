# Bachelor Thesis | Question Answering System based on Tourism Knowledge Graph using state-of-the-art BERT embeddings

![1](https://user-images.githubusercontent.com/64464819/223718105-b5c564c3-c7c1-4640-b144-d2d1cb41e4b1.png)
In this paper, we conduct a thorough and extensive research on both Knowledge Graphs and Question
Answering Systems in order to highlight their potential and ultimately develop our own QA System that employs our original,
purpose-built (domain specific) Knowledge Graph for Tourism. You can find and read my Bachelor Thesis in the link below:
http://dspace.lib.uom.gr/handle/2159/28676 

## Research Problem
It is true that, nowadays, there is an overabundance of (tourism) information scattered on the Web which makes it difficult to have a great tourist experience and be well informed about your next travel destination without the confusing and time consuming process of it.Creating a Question Answering system based on a Tourism Knowledge Graph offers the user the ability to question a system with a centralized and semantically rich knowledge about their next travel destination and as a result help them better plan their itinerary

Thesis Idea: Create a Question Answering system based on a Tourism Knowledge Graph that offers the user the ability to question a system with a centralized and semantically rich knowledge about their next travel destination and as a result help them better plan their itinerary.


## Features
Some of the key features of our QA Systen include:
1.We have successfully created a (domain-specific) **Knowledge Graph** focusing on the **Tourism of the island of Santorini** consisting of 237 nodes and 285 edges. We must point out the fact that we have used the Turtle RDF Language in order to serialize our KG. Moreover, we must notice the fact that we have hosted the Tourism KG that we have created on the Neo4j Graph Data Platform. In order to enable the use of RDF in Neo4j we have made use of the Neosemantics (n10s) Plugin.
Additionally, for the purposes of populating our Tourism Knowledge Graph we have collected both structured and unstructured data related to Santorinian Tourism. It is important to notice the fact our Knowledge Graph contains mainly static data. For the population of this KG we managed to collect and “clean” a variety of data deriving from different sources.
![NEW+ALL](https://user-images.githubusercontent.com/64464819/223723913-69bf2d19-23b7-44fa-8a4a-757b486c49c0.PNG)


2.Question Answering System
Our QA System can be characterized as a closed domain question answering system as it aims to answer questions
under the specific domain of Tourism. Additionally, our system deploys a Template-Based Architecture in order to answer the factoid questions posed by the user.

  2.1 The Question Classification Subsystem
  The Question Classification subsystem is the first stage – out of the two stages of the Question Matching phase –
  that the input question must go through in order to get classified in the right group of Templates.
  In this study, for the purposes of building our Question Answering System, we have used the state-of-the-art NLP framework, BERT which stands for Bidirectional         Encoder Representations from Transformers.
  
  Key points:
  
      ➔ No Training Set
      
      ➔ Word Clusters
      
      ➔ BERT Embeddings

![3](https://user-images.githubusercontent.com/64464819/223725623-cc787075-308f-4cc4-a1f9-9ae65361aa0f.png)


  2.2 The Template Matching Subsystem
  Our second main subsystem and the second stage of the Question Matching Phase that is the Template Matching Subsystem. When designing this
  subsystem the main idea was that after sorting the input question into the best fitting group of templates we needed to compare that question with each template. In   order to do that we wanted to submit the question to a number of similarity tests and then compare and combine them in order to achieve a better accuracy in our       system. The Template Matching Subsystem consists of two subsystems:
    ● The Sentence Similarity (SS) Subsystem based on SentenceTransformers
    ● The Linguistic Similarity (LS) based on a more linguistic approach

  
  Key points:
  
      ➔ Two Methods
      
      ➔ SentenceTransformers
      
      ➔ Cosine Similarity
      
  ![Template Matching](https://user-images.githubusercontent.com/64464819/223727430-d5dbec14-6ba0-4cfe-9a3d-6c5dd231c48e.png)


  2.3 The Answer Retrieval Subsystem
  the last subsystem of our Question Answering system that aims to connect the Knowledge Graph we created with the QA system. After getting our user’s question and       having gone through the whole Question Matching phase successfully, meaning that we have matched our input question to a template, then we are ready for the Answer     Retrieval phase. In the next phase we are going to be “translating” the user’s question into a language that our knowledge graph database understands. Furthermore,     after retrieving the answer for the original question and printing it to the user, based on the abilities of our QA system and the way that it has been built we can   recommend to the user a possible follow-up question.
  
  Key points:
  
      ➔ Cypher Queries
      
      ➔ NER
      
      ➔ Follow-up Question Recommendation
      
      
## Getting started
To get started you will need to run the above notebooks either on your local Jupyter Notebook or on Google Collab and input the available csv files as well as a question.


## Technologies used
Our Question Answering System based on a Tourism KG was built using the following technologies:
1. BERT Embeddings (bert-base-uncased BERT model)
2. SentenceTransformers
3. Neo4j Graph Data Platform
4. Cypher Query Language
5. Turtle RDF
6. Neosemantics (n10s) Plugin
7. Python version 3.8
8. Google Collaboratory
9. gensim library
10. NLTK Porter Stemmer, WordNet Lemmatizer
11. Cosine Similarity
12. py2neo driver
13. SPACY Library (for NER)
14. Pandas Dataframe
15. sklearn metrics
16. Truecase Library


## Contributors
This Question Answering System was developed by me under the supervision and guidance of Georgia Koloniari during the year 2022-2023.

## Contact
LinkedIn: linkedin.com/in/christine-m5100

Email: christinem.5100@gmail.com

## License
This project is licensed under the MIT License - see the LICENSE file for details.
