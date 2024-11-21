PDF Chat Bot - Streamlit Application
A conversational web application built with Streamlit that allows users to interact with PDF and image files (PNG, JPG, JPEG, WEBP). The app extracts text from these files and answers questions based on the content through an AI-powered chatbot.

📋 Features
File Upload: Upload PDFs or image files (PNG, JPG, JPEG, WEBP).
Text Extraction: Extracts text from PDFs and images using Optical Character Recognition (OCR).
Text Processing: Splits extracted text into chunks for efficient retrieval.
Conversational Interface: Ask questions about the content of uploaded files.
Similarity Search: Uses a vector store to find relevant document sections and generate responses.
🧑‍💻 How It Works
1. Upload Files
Upload one or multiple PDF or image files through the Streamlit interface.
2. Text Extraction
PDFs: Extract text directly from each page.
Images: Apply OCR using Tesseract to extract text from image files.
OCR for PDFs: Optionally enable OCR for embedded images in PDF files.
3. Text Processing
The extracted text is split into smaller chunks.
Embeddings (vector representations) of these text chunks are created and stored in a FAISS vector store for fast similarity search.
4. Conversational Interface
Users can ask questions related to the content of the uploaded files.
The app searches the vector store for relevant information and generates responses using the ChatGoogleGenerativeAI model.
⚙️ Installation and Setup
1. Clone the Repository
bash
Copy code
git clone https://github.com/your-username/pdf-chat-bot.git
cd pdf-chat-bot
2. Install Dependencies
Install the required Python libraries:

bash
Copy code
pip install -r requirements.txt
3. Set Up Environment Variables
Set your Google API Key for the Google Generative AI service:

bash
Copy code
export GOOGLE_API_KEY="your-api-key"
4. Install Tesseract OCR
To extract text from images, you need to install Tesseract OCR.

Download and install Tesseract from here.
On Windows, ensure Tesseract is added to your system’s PATH.
5. Run the Application
Once everything is set up, run the Streamlit app:

bash
Copy code
streamlit run app.py
🖥️ Using the Application
Upload Your Files
Use the sidebar to upload your PDF or image files.
Enable OCR for PDFs if needed.
Ask Questions
In the chat interface, ask questions about the content of the uploaded files.
The app will search for relevant information and generate responses based on the document.
Clear Conversation
Reset the conversation history at any time by clicking the "Clear Conversation" button in the sidebar.
⚡ Libraries and Technologies
Streamlit: Web interface framework.
PyPDF2: For extracting text from PDF files.
pytesseract: OCR tool for extracting text from images.
LangChain: For text splitting, embedding generation, and conversational AI.
FAISS: For fast similarity search of text embeddings.
🎯 Example Use Case
Upload a PDF: Upload a research paper or any document.
Ask Questions: Ask questions like "What is the main topic?" or "Summarize the introduction."
Get Answers: The app will analyze the content and respond based on the document’s context.
🤝 Contributing
Feel free to fork this project, submit issues, or open pull requests to enhance the app. Contributions are always welcome!

📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

📝 Contact
For any questions or feedback, feel free to open an issue in the repository or contact the project maintainer.
