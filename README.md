# Astronomy-Doubt-Solving-Chatbot

This Python program implements a Retrieval-Augmented Generation (RAG) system tailored to answer astronomy-related questions. It combines retrieval of relevant information with generative natural language processing to deliver precise and contextually accurate answers. 


The following are the key components of this Project:

1. Wikipedia Retrieval:
* The program uses the wikipedia library to search for articles related to the user's query.
* It retrieves short summaries (up to three sentences) of the top results to provide a pool of potential context.

2. Semantic Search (Retriever):
* A SentenceTransformer model (multi-qa-mpnet-base-dot-v1) is used for semantic search.
* It compares the user's question with the retrieved Wikipedia summaries to select the most relevant context.
  
3. Generative Answering (Generator):
* A pre-trained question-answering (QA) model (deepset/roberta-base-squad2) is used to generate answers.
* It takes the user’s question and the retrieved context as inputs to produce a concise, accurate response.
