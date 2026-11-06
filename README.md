# 🎥AI YouTube Video Analyzer

TubeLens is a Streamlit web app that analyzes any YouTube video using an AI agent. Paste a video link and get a structured report with a video overview, timestamped segments, main themes, and key learning points, so you can understand a video without watching it end to end.

## 🌐 Live Demo

👉 **[Try AI YouTube Video Analyzer](https://ai-youtube-video-analyzerrr.streamlit.app/)**

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
- Streamlit secrets for managing the API key

## 📁 Project Structure

```
├── youtube_analyzer.py   # Builds the Agno agent (model, tools, instructions)
├── ui.py                 # Streamlit interface
├── requirements.txt      # Dependencies
└── .streamlit/
    └── secrets.toml      # API key (not committed)
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add your Groq API key

Create a file at `.streamlit/secrets.toml`:

```toml
API_KEY_GROQ = "your_api_key_here"
```

### 5. Run the app

```bash
streamlit run ui.py
```

Open the local URL shown in your terminal (usually `http://localhost:8501`).

## 📖 How to Use

1. Paste a YouTube video link into the input box.
2. Click **Analyze Video**.
3. Wait a few seconds for the **Analysis Report** to appear.

## ⚙️ How It Works

1. `app.py` takes the video URL and sends it to the agent.
2. The agent uses `YouTubeTools` to fetch the video's metadata and transcript.
3. The Groq-hosted LLM follows the instructions in `youtube_analyzer.py` to build the overview, timestamps, and themes.
4. The result is rendered as Markdown in the Streamlit app.

## ⚠️ Limitations

- Works only for videos that have a transcript/captions available.
- Timestamps are AI-generated from the transcript, so spot-check important ones.
- Very long videos may hit model context limits.

## 🔮 Future Improvements

- Export reports as PDF or Markdown
- Support for multiple videos and playlists
- Chat with the video (follow-up questions)
- Language selection for summaries

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to open an issue or submit a pull request.

## 📄 License

This project is licensed under the MIT License.

## 👤 Author

**Sameer Rajbhar**
GitHub: [@sameerrajbhar99](https://github.com/sameerrajbhar99)
