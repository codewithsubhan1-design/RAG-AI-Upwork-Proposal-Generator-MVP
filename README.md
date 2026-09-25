# RAG AI Upwork Proposal Generator — MVP

Django + Gemini API + local vector retrieval MVP for generating personalized Upwork proposals.

## Features
- Job title/description input
- Lightweight job requirement analysis
- RAG retrieval from a local knowledge base
- Gemini API proposal generation
- Simple web UI
- Django REST-style JSON endpoint

## Quick start

1. Create a virtual environment:
   `python -m venv .venv`

2. Activate it on Windows:
   `.venv\Scripts\activate`

3. Install dependencies:
   `pip install -r requirements.txt`

4. Copy `.env.example` to `.env` and add your Gemini API key.

5. Run:
   `python manage.py migrate`
   `python manage.py runserver`

6. Open:
   `http://127.0.0.1:8000/`

## Notes
The MVP uses TF-IDF + cosine similarity for retrieval so it can run locally without a separate vector database. Gemini is used for generation when `GEMINI_API_KEY` is configured.
