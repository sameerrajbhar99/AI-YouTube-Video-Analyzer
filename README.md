# 🎥 TubeLens – AI YouTube Video Analyzer

TubeLens is a Streamlit web app that analyzes any YouTube video using an AI agent. Paste a video link and get a structured report with a video overview, timestamped segments, main themes, and key learning points, so you can understand a video without watching it end to end.

## ✨ Features

- **Video overview**: identifies the video type (tutorial, review, lecture, etc.) and its structure
- **Timestamp generation**: creates meaningful timestamps for major topic transitions
- **Content organization**: groups related segments and tracks topic progression
- **Emoji content markers**: 📚 Educational, 💻 Technical, 🎮 Gaming, 📱 Tech Review, 🎨 Creative
- **Simple UI**: paste a link, click a button, read the report

## 🛠️ Tech Stack

- [Python](https://www.python.org/)
- [Streamlit](https://streamlit.io/) for the web interface
- [Agno](https://docs.agno.com/) for the AI agent framework and `YouTubeTools`
- [Groq](https://groq.com/) for fast LLM inference (`openai/gpt-oss-120b`)
- `youtube-transcript-api` for fetching video transcripts
- `python-dotenv` for managing environment variables

## 📁 Project Structure

```
├── youtube_analyzer.py   # Builds the Agno agent (model, tools, instructions)
├── ui.py                 # Streamlit interface
├── requirements.txt      # Dependencies
└── .env                  # API key (not committed)
```
