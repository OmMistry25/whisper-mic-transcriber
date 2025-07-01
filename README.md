# Whisper Mic Transcriber

**Live microphone transcription using OpenAI Whisper, storing output for downstream processing.**

---

## Features

- Live transcription using your **laptop microphone**  
- Transcriptions **saved automatically** with timestamps  
- Simple, lightweight, and fully local  
- Ready to integrate with **downstream pipelines** later (summarization, Slack push, etc.)

---

## Setup

1️. **Clone the repository:**

```bash
git clone <your_repo_url>
cd whisper-mic-transcriber
```

2️. **Create and activate a virtual environment:**

```bash
python -m venv venv
source venv/bin/activate      # macOS/Linux
venv\Scripts\activate         # Windows
```

3️. **Install dependencies:**

```bash
pip install -r requirements.txt
```

---

## Usage

To start **live mic transcription:**

```bash
python mic_transcribe.py
```

- Records 10-second segments continuously.
- Transcribes using OpenAI Whisper.
- Prints transcriptions in the terminal.
- Saves to `transcriptions/transcriptions.txt` with timestamps.

Stop anytime using **CTRL+C**.

---

## Project Structure

```
whisper-mic-transcriber/
├── transcriptions/              # Stores output .txt files
│    └── transcriptions.txt
├── venv/                        # Virtual environment (excluded via .gitignore)
├── .gitignore
├── mic_transcribe.py            # Main transcription script
├── README.md                    # Project documentation
└── requirements.txt             # Dependencies
```

---

## Notes

- Uses **OpenAI Whisper** (`openai-whisper`) for accurate transcription.
- Uses **PyAudio** for microphone streaming (requires mic permissions on macOS).
- Defaults to using the **`base` Whisper model** (can adjust to `tiny`, `small`, etc. in `mic_transcribe.py`).
- Records at **44100 Hz** to match typical MacBook mic input.

---

## Next Steps (Optional Ideas)

- Add **post-processing pipelines** (summarization, keyword extraction).  
- Push transcriptions to **Slack, Notion, or Google Sheets**.  
- Add **hotkey-based start/stop** for ease of control.  
- Deploy on a **headless server or always-on device** for meeting transcription.

---

## Contributing

Pull requests and suggestions are welcome to improve workflows and integrations.

---

## License

MIT License

---

**Enjoy seamless live transcription on your laptop for your projects!**
