# Project Overview

## Motivation
Our project aims to leverage class lectures to create a lecture summarizer and a chatbot capable of answering student queries based on these lectures. By developing a system that can summarize lecture content and provide interactive assistance to students, we aim to enhance learning experiences and facilitate better understanding of complex topics.

## Web Scraping from YouTube
**WebScrapingFromYoutube.ipynb**: This notebook focuses on scraping data from YouTube related to a specific search topic query. It utilizes Selenium and BeautifulSoup libraries to scrape search results for videos matching the query. The extracted data includes video titles, views, and URLs. The script then sorts the videos based on view counts and selects the top 5 videos for deeper analysis. For each of these top videos, it retrieves the number of likes and scrapes the transcripts using the youtube_transcript_api library. Finally, it cleans the transcripts and prepares them for further processing.

## Text Summarization
**test_summarizer_v2.ipynb**: Summarizing class lectures involves condensing the key points, concepts, and discussions covered during a lecture into concise and easily digestible information. This notebook explores the implementation of various text summarization models including BART, BERT, PEGASUS, T5, and LED. The performance metrics used for evaluation include ROUGE and BLEU.

## Chatbot
**chatapp.py**: This script implements a chatbot using the llama-2-70b language model. The chatbot is designed to interact with users in a conversational manner, providing responses to questions about class lectures. It utilizes components such as ConversationalRetrievalChain, HuggingFaceEmbeddings, Replicate (llama-2-70b), CharacterTextSplitter, and FAISS to effectively respond to user queries based on lecture content.

![ModelStructure](https://github.com/BhargavN02/NLP-Based-Teaching-Assistant/assets/28643880/f7103a0b-208b-404e-adb1-557c3bbedac6)


## Purpose and Models Used
The purpose of the chatbot is to provide interactive assistance to students by answering their queries about class lectures. The models used include:
- **ConversationalRetrievalChain**: Manages the conversation flow and retrieves relevant information from the document corpus.
- **HuggingFaceEmbeddings**: Embeds the text data into vector representations understandable by the conversational models.
- **Replicate (llama-2-70b)**: Understands user queries, generates responses, and maintains context within the conversation.
- **CharacterTextSplitter**: Splits input text into smaller chunks for processing.
- **FAISS**: Indexes and searches the document corpus efficiently.

Overall, the project aims to create an integrated system that enhances the learning experience by summarizing lectures and providing interactive assistance to students through the chatbot.
