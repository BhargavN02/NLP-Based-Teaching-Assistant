# Project Overview

## Motivation
Our project aims to leverage class lectures to create a lecture summarizer and a chatbot capable of answering student queries based on these lectures. By developing a system that can summarize lecture content and provide interactive assistance to students, we aim to enhance learning experiences and facilitate better understanding of complex topics.

## Web Scraping from YouTube
**WebScrapingFromYoutube.ipynb**: This notebook focuses on scraping data from YouTube related to a specific search topic query. It utilizes Selenium and BeautifulSoup libraries to scrape search results for videos matching the query. The extracted data includes video titles, views, and URLs. The script then sorts the videos based on view counts and selects the top 5 videos for deeper analysis. For each of these top videos, it retrieves the number of likes and scrapes the transcripts using the youtube_transcript_api library. Finally, it cleans the transcripts and prepares them for further processing.

## Text Summarization
**test_summarizer_v2.ipynb**: Summarizing class lectures involves condensing the key points, concepts, and discussions covered during a lecture into concise and easily digestible information. This notebook explores the implementation of various text summarization models including BART, BERT, PEGASUS, T5, and LED. The performance metrics used for evaluation include ROUGE and BLEU.

<img width="498" alt="Evaluation Metrics" src="https://github.com/BhargavN02/NLP-Based-Teaching-Assistant/assets/72100583/5289d4e5-d708-4608-a29a-5183808c078d">

## MultiDoc Chatbot

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

### Description
This project aims to create a chatbot capable of answering questions based on uploaded documents. The chatbot utilizes Natural Language Processing (NLP) techniques to understand user queries and provide relevant responses.

### Setup Instructions
1. Create a new virtual environment.
2. Install dependencies listed in the `requirements.txt` file.
3. Sign up on the Replicate portal and obtain an API token.
4. Set up the API token as an environment variable.

### Usage
1. Run the `chatapp.py` file using the command `streamlit run chatapp.py`.
2. Upload documents using the file uploader widget.
3. Ask questions related to the uploaded documents using the text input field.
4. The chatbot will generate responses based on the uploaded documents and user queries.

### Code Explanation
- The provided code initializes a Streamlit application.
- It sets up a sidebar for document processing and a file uploader widget to upload documents.
- Uploaded documents are processed, and their text content is extracted.
- The text content is split into smaller chunks for efficient processing.
- Embeddings are created using the Hugging Face embeddings model.
- A vector store is created using FAISS to index the text chunks.
- A conversational chain object is created to handle user queries and provide responses.
- The main function orchestrates the application flow and interaction with the chatbot.

### Running the Application
- To run the application, execute the command `streamlit run chatapp.py` in the terminal.
- Access the application through the provided URL in the terminal.

### Future Improvements
- Integration of multi-modal learning techniques to understand images alongside text.
- Video segmentation and analysis to enhance the chatbot's capabilities.
- Continuous refinement and optimization of the chatbot's responses based on user feedback.
