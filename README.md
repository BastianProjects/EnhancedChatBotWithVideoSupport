STEPS:
python -m venv venv
py -3.11 -m venv venv
Set-ExecutionPolicy Unrestricted -Scope Process
.\venv\Scripts\activate
pip install -r .\requirements.txt
streamlit run .\PDFEnhancedChatBot_WithVideoSupport.py

pip install git+https://github.com/openai/whisper.git
install ffmpeg

This project is an AI-powered chatbot application built using Streamlit, designed to handle and interact with various types of content, including PDFs, URLs, and video presentations. The chatbot leverages advanced natural language processing (NLP) models and tools to provide intelligent question-answering capabilities. Below is a detailed description:
Key Features:
1.	PDF Handling:
•	Upload and process PDF files.
•	Extract and summarize text from PDFs.
•	Index PDF content for efficient retrieval and question answering.
2.	URL Processing:
•	Load and process web pages using Selenium.
•	Summarize web page content.
•	Index web page content for querying.
3.	Video Presentation Support:
•	Upload video files (e.g., .mp4, .mov).
•	Transcribe audio from videos using Whisper.
•	Extract frames from videos and perform OCR (Optical Character Recognition) on slides.
•	Index transcribed audio and slide content for querying.
4.	Chatbot Functionality:
•	Answer user questions based on indexed content from PDFs, URLs, and videos.
•	Maintain chat history for context-aware responses.
•	Filter responses by specific content sources.
5.	Vector Database:
•	Use Chroma as a vector store for embedding and indexing content.
•	Support for clearing and managing the vector database.
6.	Streamlit Interface:
•	User-friendly interface for uploading files, entering URLs, and interacting with the chatbot.
•	Sidebar for managing sources and clearing data.
Technologies Used:
•	Streamlit: For building the web-based user interface.
•	LangChain: For text splitting, embeddings, and LLM integration.
•	Whisper: For audio transcription.
•	OpenCV: For video frame extraction.
•	Pytesseract: For OCR on extracted frames.
•	Chroma: For vector database storage and retrieval.
•	LLM Models: Custom models (llama3.2 for embeddings and gemma3 for language generation).
Purpose:
The application is designed to assist users in efficiently extracting, summarizing, and querying information from diverse content sources, making it ideal for research, presentations, and knowledge management tasks.
