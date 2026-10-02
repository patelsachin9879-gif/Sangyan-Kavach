# SANGYAN Safety Bot

## Run locally

1. Install Python dependencies:

   ```powershell
   py -m pip install -r requirements.txt
   ```

2. Set a Gemini API key in PowerShell (get one from Google AI Studio):

   ```powershell
   $env:GEMINI_API_KEY = "your-api-key"
   ```

   `GEMINI_MODEL` is optional and defaults to `gemini-2.5-flash`.

3. Start the API from this folder:

   ```powershell
   py -m uvicorn main:app --reload --host 127.0.0.1 --port 8000
   ```

4. Open `index.html` in a browser. The UI posts messages to
   `http://localhost:8000/api/analyze`. Check that the backend is running at
   `http://localhost:8000/health`.

Keep the API key in the backend environment; do not put it in `index.html`.
