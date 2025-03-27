# Personal-AI-Voice Chatbot

# Live Demo
[Click here to access the deployed App](https://personal-ai-assitant-sn8r.onrender.com/)

# Overview
This project is a voice-interactive chatbot built using Flask for the backend and the Web Speech API for speech recognition and synthesis. It integrates Google Generative AI for natural language understanding and FAISS for efficient similarity search. The chatbot allows users to input queries via text or voice and receive AI-generated responses in both text and speech formats.

# Features
* Voice & Text Interaction: Users can type or use speech recognition to ask questions.
* AI-Powered Responses: Utilizes Google Generative AI for intelligent responses.
* Embeddings & Similarity Search: Uses FAISS for efficient document retrieval.
* Text-to-Speech (TTS): Converts AI responses into speech.

# Tech Stack
* **Backend:** Flask
* **Frontend:** HTML, CSS, JavaScript
* **AI Model:** Google Generative AI (Gemini)
* **Vector Store:** FAISS
* **Speech Recognition & TTS:** Web Speech API

*Notes* : To personalize the chatbot's responses, add your own documents to the documents folder (not included in the repository; create it in the project root). Then, run the following command to process the documents and update the FAISS vector database:
```python process_docs.py``` 
This will convert your documents into vector embeddings and store them in the database, enabling the chatbot to provide context-aware responses based on your custom data.

# Repository Structure

```
├── app.py                # Flask application
├── templates
│   ├── index.html        # Frontend UI
├── static
│   ├── styles.css        # CSS for UI
│   ├── script.js         # JavaScript for frontend
├── faiss_db              # FAISS Vector Store
├── requirements.txt      # Dependencies
├── .env                  # API Keys (Not included in repo)
├── documents/            # Documents for RAG (Not included in repo)
├── process_docs.py       # Script convert PDFs to vectors
```

# Setup & Installation Guide

1. Clone the Repository
   ```
   git clone https://github.com/Durai-Bharath/Personal-AI-Assitant.git
   cd Personal-AI-Assistant
   ```
2. Create a Virtual Environment (Optional but Recommended)
   ```
   python -m venv venv
   source venv/bin/activate  # On MacOS/Linux
   venv\Scripts\activate    # On Windows
   ```
3. Install Dependencies
   ```
   pip install -r requirements.txt
   ```
4. Set Up Environment Variables
   Create a .env file in the root directory and add your Google API Key:
   ```
   GOOGLE_API_KEY=your_google_api_key
   ```
5. Run the Application Locally
   ```
   python app.py
   ```
   This will start the chatbot server, and you can access it at http://localhost:5000.
