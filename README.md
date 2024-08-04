# Gemini PDF Chatbot

Gemini PDF Chatbot is a web application built using Streamlit that allows users to upload PDF documents and interact with them through a conversational chatbot interface. This project leverages Google's Generative AI models to generate responses based on the content of the uploaded PDFs.

## Features

- **PDF Upload**: Users can upload multiple PDF files which the application processes to extract text.
- **Text Processing**: Extracted text is divided into manageable chunks for efficient processing.
- **Conversational Interface**: Users can ask questions about the uploaded PDFs, and the chatbot provides detailed answers based on the document content.
- **Contextual Answers**: The chatbot aims to answer questions based on the provided context, ensuring accuracy.
- **Chat History**: Users can view the conversation history and clear it as needed.

![image](https://github.com/user-attachments/assets/94b5606b-f8a1-4904-aa52-37a2bd6cd43a)


## Requirements

- Python 3.7 or higher
- Required Python packages (see `requirements.txt`)

## Installation

1. **Clone the repository**:

   ```bash
   git clone <link>
   ```

2. **Create a virtual environment**:

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the required packages**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**:

   Create a `.env` file in the root directory and add your Google API key:

   ```plaintext
   GOOGLE_API_KEY=your_google_api_key_here
   ```

5. **Run the application**:

   ```bash
   streamlit run app.py
   ```

## Usage

1. Open the application in your browser (usually at `http://localhost:8501`).
2. Upload PDF files using the sidebar uploader.
3. Click on the "Submit & Process" button to process the PDFs.
4. Type your questions in the chat input area to interact with the PDFs.
5. Use the "Clear Chat History" button to reset the conversation.

## File Structure

- **`app.py`**: Main application file containing the Streamlit app logic.
- **`requirements.txt`**: Lists the dependencies required for the project.
- **`.env`**: Environment file to store sensitive information such as API keys.

## Key Functions

- `get_pdf_text(pdf_docs)`: Reads and extracts text from uploaded PDF files.
- `get_text_chunks(text)`: Splits text into smaller chunks for processing.
- `get_vector_store(chunks)`: Generates embeddings for text chunks and stores them in a FAISS vector store.
- `get_conversational_chain()`: Sets up the conversational AI model and prompt template.
- `user_input(user_question)`: Handles user queries and retrieves relevant document sections for generating answers.

## Dependencies

This project uses the following main libraries:

- Streamlit
- PyPDF2
- Langchain
- Google Generative AI
- FAISS
- dotenv


## Acknowledgments

- [Google Gemini](https://ai.google.com/): For providing the underlying language model.
- [Streamlit](https://streamlit.io/): For the user interface framework.
