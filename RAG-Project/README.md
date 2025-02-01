# RAG-Based File Processor in Google Colab

## Overview
This project is a **Retrieval-Augmented Generation (RAG) system** implemented in **Google Colab** that allows users to upload files (PDFs, images, or text files). The system extracts text from these files, identifies questions, and provides AI-generated answers using Google's Generative AI model and Pinecone vector database.

## Features
- **File Upload Support:** Upload PDFs, images, or text files.
- **Text Extraction:** Uses OCR (Tesseract) for images and PyPDF2 for PDFs.
- **AI-Powered Answer Generation:** Uses Google's Generative AI model.
- **Vector Search with Pinecone:** Retrieves relevant context for better answers.
- **Fully Automated Workflow:** No manual text input required.

## Installation & Setup
1. **Install Dependencies:**
   ```python
   !pip install pytesseract pypdf2 langchain-pinecone langchain-google-genai pinecone-client
   ```
2. **Set API Keys in Google Colab:**
   - `GOOGLE_API_KEY_1`
   - `PINECONEKEY1`
   
   Store them securely using:
   ```python
   from google.colab import userdata
   userdata['GOOGLE_API_KEY_1'] = 'your-google-api-key'
   userdata['PINECONEKEY1'] = 'your-pinecone-api-key'
   ```

## How It Works
1. **File Upload:** Users upload a file containing questions.
2. **Text Extraction:** The system extracts text from PDFs, images, or text files.
3. **RAG System Initialization:**
   - Google Generative AI model is initialized.
   - Pinecone vector store is set up.
4. **Question Processing:**
   - Extracted text is split into questions.
   - Relevant data is retrieved from the vector store.
   - AI generates an answer for each question.
5. **Output Display:** Answers are printed in the Colab output.

## Usage Instructions
1. **Run the Colab Notebook.**
2. **Upload a file when prompted.**
3. **Wait for the system to process the file and answer questions.**
4. **View generated answers in the Colab output.**

## Technologies Used
- **Python**
- **Google Colab**
- **Google Generative AI API**
- **Pinecone (Vector Search)**
- **Tesseract OCR**
- **PyPDF2**
- **LangChain**

## Future Improvements
- Support for more file formats (e.g., Word documents).
- Integration with a web-based UI.
- Enhanced question-answering accuracy.

## Author
Developed by Mavia Ahmed.

## License
This project is open-source and available under the MIT License.

