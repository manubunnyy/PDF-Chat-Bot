# PDF Chat Bot - Streamlit Application

A conversational web application built with **Streamlit** that allows users to interact with **PDF** and **image files** (PNG, JPG, JPEG, WEBP). The app extracts text from these files and answers questions based on the content through an AI-powered chatbot.

---

## 📋 Features

- **File Upload**: Upload PDFs or image files (PNG, JPG, JPEG, WEBP).
- **Text Extraction**: Extracts text from PDFs and images using Optical Character Recognition (OCR).
- **Text Processing**: Splits extracted text into chunks for efficient retrieval.
- **Conversational Interface**: Ask questions about the content of uploaded files.
- **Similarity Search**: Uses a vector store to find relevant document sections and generate responses.

---

## 🧑‍💻 How It Works

### 1. **Upload Files**
- Upload one or multiple PDF or image files through the Streamlit interface.

### 2. **Text Extraction**
- **PDFs**: Extract text directly from each page.
- **Images**: Apply OCR using **Tesseract** to extract text from image files.
- **OCR for PDFs**: Optionally enable OCR for embedded images in PDF files.

### 3. **Text Processing**
- The extracted text is split into smaller chunks.
- **Embeddings** (vector representations) of these text chunks are created and stored in a **FAISS** vector store for fast similarity search.

### 4. **Conversational Interface**
- Users can ask questions related to the content of the uploaded files.
- The app searches the vector store for relevant information and generates responses using the **ChatGoogleGenerativeAI** model.

---

## ⚙️ Installation and Setup
### Quick steps:
1. **Install dependencies**:  
   Ensure you’ve run `pip install -r requirements.txt` to install all necessary libraries.
   
2. **Run the Streamlit app**:  
   Use `streamlit run app.py` to launch the app.

This setup should allow others to easily follow the instructions and get the app running!

