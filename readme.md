# PDF Chat App

## Introduction
------------
The PDF Chat App is a Python application that allows you to chat with OpenAI. The PDFs acts as a train model and after that You can ask questions about the PDFs using natural language, and the application will provide relevant responses based on the content of the documents. Please note that the app will only respond to questions related to the loaded PDFs.

## How It Works
------------

![MultiPDF Chat App Diagram](./docs/PDF-LangChain.jpg)

The application follows these steps to provide responses to your questions:

1. PDF Loading: The app reads multiple PDF documents and extracts their text content.

2. Text Chunking: The extracted text is divided into smaller chunks that can be processed effectively.

3. Language Model: The application utilizes a language model to generate vector representations (embeddings) of the text chunks.

4. Similarity Matching: When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.

5. Response Generation: The selected chunks are passed to the language model, which generates a response based on the relevant content of the PDFs.

## Dependencies and Installation
----------------------------
To install the MultiPDF Chat App, please follow these steps:

1. Clone the repository to your local machine.

2. Do this
   python3 -m venv .venv
   source ./.venv/bin/activate

3. Install the required dependencies by running the following command:
   ```
   pip install -r requirements.txt
   ```

3. Obtain an API key from OpenAI. copy the content from .env.example and duplicate it and rename it as .env. Add the OpenAI keyto the `.env` file in the project directory. The rate limiter will be an issue if you used a pdf with lots of text. The best way is to go to OpenAI account and setup your billing. 

4. After that just run streamlit run 
   ```
   streamlit run app.py
   ```

4. The application will launch in your default web browser, displaying the user interface.

5. Load multiple PDF documents into the app by following the provided instructions. Click on process

6. Ask questions in natural language about the loaded PDFs using the chat interface.

## Contributing
------------
This repository is intended for educational purposes and does not accept further contributions. It serves as supporting material for a YouTube tutorial that demonstrates how to build this project. Feel free to utilize and enhance the app based on your own requirements.
