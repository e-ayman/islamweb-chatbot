# Islamweb Q&A Chatbot

A Flask-based chatbot that scrapes, preprocesses, and embeds Q&A data from Islamweb, indexes it with ChromaDB, and uses AraBERT & Google Gemini to serve relevant, context-aware answers—all ready to run in Google Colab with zero local setup.

## Setup

Before you run the project, just add your Google Gemini API token and your ngrok API token:

- **In Colab:**  
  ```python
  import os
  os.environ["GEMINI_API_TOKEN"] = "your_gemini_token_here"
  os.environ["NGROK_API_TOKEN"] = "your_ngrok_token_here"

## Features

- **Data Collection**: Web-scraping of Islamweb’s Q&A into structured (question, answer, category) records.  
- **Preprocessing & Embedding**: Text cleaning and embedding with AraBERT.  
- **Vector Store**: Fast similarity search powered by ChromaDB.  
- **Chat Interface**:  
  1. User query → embed  
  2. Retrieve top 3 relevant Q&As  
  3. Generate response via Google Gemini  
- **API**: Flask application exposes `/chat` endpoint for seamless integration.  
- **Colab-Ready**: Launch the notebook in Colab—no local environment needed.

## Requirements

See [`requirements.txt`](requirements.txt) for full dependency list:
