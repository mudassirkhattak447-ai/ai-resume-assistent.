# 📄 ATS Resume Checker

Upload your resume (PDF, DOCX or TXT) and get an ATS score, a section breakdown,
strengths, missing keywords and prioritised improvements. Optionally paste a job
description to check how well your resume matches it.

Built with [Streamlit](https://streamlit.io) and Google Gemini Flash.

## Features
- PDF / DOCX / TXT resume upload
- Overall ATS score (0-100) plus Formatting, Keywords, Content and Completeness scores
- Prioritised, actionable improvements
- Optional job-description matching

## Run locally
```bash
git clone <your-repo-url>
cd <your-repo>
pip install -r requirements.txt
export GEMINI_API_KEY="your-key"      # Windows PowerShell: $env:GEMINI_API_KEY="your-key"
streamlit run app.py
```
Get a free API key at https://aistudio.google.com/apikey. If you skip the
environment variable, the app asks for the key in the sidebar.

## Deploy on Streamlit Community Cloud
1. Push this repo to GitHub.
2. Go to https://share.streamlit.io and click **Create app**.
3. Pick your repo, branch `main` and main file `app.py`.
4. Open **Advanced settings → Secrets** and add:
   ```toml
   GEMINI_API_KEY = "your-key"
   ```
5. Click **Deploy**.

> Never commit your API key to GitHub.

## Notes
- Scanned (image-only) PDFs can't be read; use a text-based PDF or DOCX.
- Scores are AI estimates, not a guarantee of how a real ATS will rank you.
- The model name is set by `MODEL_NAME` at the top of `app.py`.# ai-resume-assistent.
