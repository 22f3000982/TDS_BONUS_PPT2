# Render Deployment Guide

## Configuration for Render.com

### Build Command:
```
pip install -r requirements.txt
```

### Start Command (Option 1 - Recommended):
```
uvicorn app:app --host 0.0.0.0 --port 10000
```

### Start Command (Option 2 - With Gunicorn):
```
gunicorn app:app -w 4 -k uvicorn.workers.UvicornWorker
```

## Environment Variables
If your app uses any API keys, set them in the Render dashboard under Environment Variables:
- `OPENAI_API_KEY`
- `ANTHROPIC_API_KEY` 
- `GOOGLE_API_KEY`

## Deployment Steps
1. Go to render.com
2. Create new Web Service
3. Connect your GitHub repo
4. Use the build and start commands above
5. Set environment variables if needed
6. Deploy!

Your app will be available at: `https://your-app-name.onrender.com`
