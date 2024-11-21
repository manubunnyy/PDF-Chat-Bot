PDF Chat Bot - Streamlit Application
Overview
This Streamlit application allows users to interact with PDF and image files (PNG, JPG, JPEG, WEBP) by asking questions about their content. It processes the files to extract text and provides answers based on the extracted information through a conversational interface.

Features
File Upload: Upload PDFs or image files for processing.
Text Extraction: Extracts text from PDFs and images using OCR.
Text Processing: Splits extracted text into chunks for efficient searching.
Conversational Interface: Users can ask questions about the content of the uploaded files.
Similarity Search: The app finds relevant text chunks to answer user questions.
How It Works
Upload Files: Users can upload PDF or image files.
Text Extraction: The app extracts text from the files. For images, it uses OCR (Tesseract). PDFs can also have OCR applied if required.
Text Processing: The extracted text is split into smaller chunks, which are embedded and stored in a vector store for efficient search.
Question-Answering: When a user asks a question, the app searches the vector store for relevant information and generates a response using the ChatGoogleGenerativeAI model.
Technical Details
Libraries Used:
Streamlit: For the web interface.
PyPDF2: To read PDF files.
pytesseract: For Optical Character Recognition (OCR).
LangChain: For text splitting, embeddings, and conversational AI integration.
FAISS: For storing and searching text embeddings efficiently.
Usage
Install Dependencies:
Install the required Python libraries via pip install -r requirements.txt.

Set Up:

Set your Google API key as an environment variable.
Install Tesseract OCR for text extraction from images.
Run the Application:
Execute streamlit run app.py to launch the web app.

Upload Files:
Use the sidebar to upload your PDFs or images. Enable OCR for PDF files if needed.

Ask Questions:
In the chat interface, ask questions about the uploaded files. The app will generate answers based on the content of the files.

Clear Conversation:
You can reset the session and start fresh by clearing the conversation.

