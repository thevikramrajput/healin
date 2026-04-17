# Dr. Saheli - Medical Assistant

Dr. Saheli is a futuristic, intelligent medical chatbot powered by **Google Gemini** and **Pinecone vector embeddings**. It uses a robust internal RAG (Retrieval-Augmented Generation) pipeline to fetch domain-specific medical knowledge to ensure accurate and context-aware responses.

## Features
- **Cyberpunk UI**: A beautifully stylized hacker-aesthetic chat interface.
- **RAG Architecture**: Uses Pinecone for rapid document retrieval alongside Hugging Face embeddings.
- **Powered by Gemini**: Fully integrated with the Google gemini-flash-latest generative AI framework for instantaneous intelligence.

## 🚀 Beginner's Quick Start Guide

Follow these step-by-step instructions to run the application completely offline on your own machine.

### 1. Prerequisites
Make sure you have [Python 3.10+](https://www.python.org/downloads/) installed on your computer.

### 2. Prepare the Virtual Environment
Open your terminal (PowerShell or Command Prompt) and navigate into the project folder. Create and activate an isolated Python environment so your global packages don't conflict:

**Create the environment:**
`powershell
python -m venv venv2
`

**Activate the environment:**
`powershell
.\venv2\Scripts\activate
`
*(You should see (venv2) appear at the start of your terminal line).*

### 3. Install Dependencies
With your environment active, install all required packages:
`powershell
pip install -r requirements.txt
`

### 4. Configure Environment Variables
Create a file named literally .env inside the main project folder. Add your API keys inside this file:
`ini
PINECONE_API_KEY="your_pinecone_key"
HUGGINGFACEHUB_API_TOKEN="your_huggingface_token_for_embeddings"
GOOGLE_API_KEY="your_google_gemini_api_key"
`

### 5. Initialize the Vector Store *(First time only!)*
If this is your first time setting up the project and Pinecone requires the medical documents, run the index script to build your vector database:
`powershell
python store_index.py
`

### 6. Start the Application
Boot up the main Flask backend:
`powershell
python app.py
`

### 7. Start Chatting
Open your favorite web browser (Chrome, Edge, Safari) and navigate to:
👉 [http://127.0.0.1:8080](http://127.0.0.1:8080)

*Note: All old boilerplate AWS, Docker, and deployment legacy artifacts have been cleanly removed to focus strictly on an optimized, fast offline RAG implementation.*
