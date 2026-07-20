# AI Writing Evaluator

A free Streamlit web app that evaluates writing with Google's Gemini API.
The interface is designed as a professional academic evaluator, a compact SaaS dashboard, a simple student tool, and a premium AI writing assistant.

## What to Build

For this project, focus on a web app first. Streamlit is faster and cheaper than a mobile app, works on phones through the browser, and keeps your API key out of the public frontend code.

## Files

- `app.py` - main Streamlit application
- `requirements.txt` - Python packages for local install and Streamlit Community Cloud
- `.streamlit/config.toml` - app theme
- `.streamlit/secrets.toml.example` - example local secrets file

## Run Locally

If `python` or `pip` is not recognized on Windows, install Python from <https://www.python.org/downloads/> and tick **Add python.exe to PATH** during setup.

Install dependencies:

```bash
pip install -r requirements.txt
```

Create `.streamlit/secrets.toml`:

```toml
GEMINI_API_KEY = "your_actual_api_key"
```

Start the app:

```bash
streamlit run app.py
```

Windows virtual environment option:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
streamlit run app.py
```

## Deploy on Streamlit Community Cloud

1. Open GitHub Desktop.
2. Choose **File > New repository** and use this project folder, or choose **File > Add local repository** if you already initialized it.
3. Commit the files.
4. Publish the repository to GitHub.
5. Go to Streamlit Community Cloud and create a new app.
6. Select the GitHub repository, branch, and `app.py` as the main file.
7. Open the app's Secrets settings and add:

```toml
GEMINI_API_KEY = "your_actual_api_key"
```

8. Deploy the app.

Do not commit `.streamlit/secrets.toml` to GitHub. It contains your private API key.
