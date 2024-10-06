# Bot Project

## Description
This project is a backend application that utilizes natural language processing and machine learning techniques to process and analyze German text documents.

## Features
- Text extraction from PDF documents
- Text embedding generation using BERT
- Efficient similarity search using FAISS
- FastAPI-based REST API for querying similar text snippets

## Requirements
- Python 3.12.6
- Virtual environment (venv)
- See `requirements.txt` for Python package dependencies

## Project Structure
```
bot/
├── backend/
│   ├── app.py
│   └── requirements.txt
├── check_snippets.py
├── process_document.py
├── embeddings.npy
├── faiss_index.bin
└── text_snippets.json
```

## Setup Instructions
1. Clone the repository:
   ```
   git clone https://github.com/blue73/bot.git
   cd bot
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

4. Download the German language model for spaCy:
   ```
   python -m spacy download de_core_news_sm
   ```
5. Run the data processing scripts only if text_snippets.json doesn't exist:
   ```
   python check_snippets.py
   ```

6. Run the data processing scripts only if embeddings.npy and faiss_index.bin don't exist:
   ```
   python process_document.py
   ```

## Usage
To start the FastAPI server, run:
```
python -m uvicorn backend.app:app --reload
```

The API will be available at `http://localhost:8000`.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
[Insert appropriate license information here]

## Support
For any questions or issues, please open an issue on the GitHub repository.
