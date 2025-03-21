SUITS - Your Legal Assistant

SUITS is an AI-powered legal assistant that allows users to interact with their PDF documents by asking questions and receiving relevant answers. It utilizes Google Generative AI and FAISS for vector storage and similarity search, ensuring accurate and contextual responses.

Features

Upload multiple PDF files

Extract text from uploaded PDFs

Chunk large text data for efficient processing

Store and retrieve document embeddings using FAISS

Answer user queries based on uploaded documents

Ensures responses are based only on available context


Tech Stack

Frontend: Streamlit

Backend: Python

AI/ML: Google Generative AI, FAISS, LangChain

Dependencies:

PyPDF2: Extracts text from uploaded PDF documents.

python-dotenv: Loads environment variables from a .env file to securely store API keys.

google-generativeai: Provides access to Google Generative AI models for embeddings and chat-based question answering.

langchain: Aids in text processing, document chunking, and managing conversational AI workflows.

FAISS: Enables efficient storage and retrieval of vector embeddings for similarity search.

streamlit: Provides a simple interface for users to upload PDFs and interact with the AI assistant.



Installation

Prerequisites

Ensure you have Python 3.8+ installed on your system.

Setup

1. Clone this repository:

git clone https://github.com/your-repo/suits-legal-assistant.git
cd suits-legal-assistant


2. Install dependencies:

pip install -r requirements.txt


3. Set up your API key:

Create a .env file in the project directory.

Add your Google API key:

GOOGLE_API_KEY=your_api_key_here




Usage

Uploading and Processing PDFs

1. Run the Streamlit app:

streamlit run app.py


2. Navigate to the sidebar and upload your PDF files.


3. Click Submit & Process to extract and process text.


4. The application will:

Extract text from PDFs using PyPDF2.

Split the extracted text into smaller chunks using LangChain's RecursiveCharacterTextSplitter.

Generate vector embeddings for text chunks using Google Generative AI Embeddings.

Store embeddings in a FAISS vector database for efficient retrieval.




Asking Questions

1. Enter a query related to the uploaded PDFs in the input field.


2. The application will:

Retrieve the most relevant text chunks using FAISS similarity search.

Use LangChain's Question Answering Chain with Google Generative AI (Gemini-Pro) to generate an answer.

Display the answer in the chat interface.




Folder Structure

|-- suits-legal-assistant
    |-- app.py                # Main application file
    |-- requirements.txt      # Python dependencies
    |-- .env                  # Environment variables (Add API key here)
    |-- faiss_index/         # Vector storage directory

Troubleshooting

Error: Google API key not found

Ensure you've correctly added your API key in the .env file.


Slow responses

Reduce the chunk_size in get_text_chunks() if dealing with large documents.



License

This project is open-source and available under the MIT License.

Author

Developed by Your Name

Contributing

Feel free to fork the repository and submit pull requests for improvements!

