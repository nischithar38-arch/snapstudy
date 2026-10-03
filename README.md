# 📚 SnapStudy

SnapStudy is a Streamlit chat app where a student enters their name and email once,
then chats with an AI study buddy - typing a question or attaching a photo of a problem,
diagram, or page of notes - and gets a plain-language explanation. One button emails a
clean set of revision notes to the student's inbox.

Built with **Gemini** (chat + vision) and **Gmail SMTP** (email).

## Features
- Photo or text input in a single chat box
- System prompt scoped to studying only (politely refuses off-topic questions)
- Graceful handling of blurry / irrelevant photos
- "Email my notes" button generates and sends a revision summary

## Run locally
1. `python -m venv venv`
2. Activate it: macOS/Linux `source venv/bin/activate` · Windows `.\venv\Scripts\Activate.ps1`
3. `pip install -r requirements.txt`
4. Copy `.streamlit/secrets.toml.example` to `.streamlit/secrets.toml` and fill in:
   - `GEMINI_API_KEY` from aistudio.google.com
   - `GMAIL_ADDRESS` and `GMAIL_APP_PASSWORD` (turn on 2-Step Verification, then create an App Password at myaccount.google.com/apppasswords)
5. `streamlit run app.py`

## Deploy
Push to GitHub (never commit `secrets.toml`), then deploy on share.streamlit.io and paste your secrets in the app's Settings → Secrets.
