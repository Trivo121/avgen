## AVGen
**AI Video Generation Tool **

A Python application that automatically scrapes trending topics from news and social media, generates a short script, and builds a 30–60 second video with text overlays and images.

---

## 🚀 Features

1. **Ingestion**: Fetch trending headlines & hashtags via NewsAPI, RSS feeds, Twitter/X, or Reddit.
2. **Ranking**: Score and deduplicate topics by recency & engagement.
3. **Script Generation**: Produce a concise narration script using an AI prompt wrapper.
4. **Media Sourcing**: Retrieve relevant images & stock clips (e.g., Unsplash API).
5. **Video Rendering**: Assemble clips, images, and text overlays into a final video (MoviePy).
6. **Configurable**: All keys, thresholds, and settings in `configs/default.yaml`.

---

## 📂 Directory Structure

```
ai_video_gen/
├── configs/            # API keys & settings
├── data/               # raw & processed data dumps
├── src/                # source modules
│   ├── ingestion/      # topic scraping & ranking
│   ├── scripting/      # script generation
│   ├── media/          # image/video asset fetcher
│   ├── render/         # video builder pipeline
│   ├── utils/          # logging & helpers
│   └── main.py         # orchestrator entry point
├── notebooks/          # prototyping work
├── requirements.txt    # dependencies
└── README.md
```

---

## ⚙️ Installation

1. Clone this repo:

   ```bash
   git clone https://github.com/your-org/ai_video_gen.git
   cd ai_video_gen
   ```
2. Create & activate a virtualenv:

   ```bash
   python3 -m venv venv && source venv/bin/activate
   ```
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

---

## ▶️ Usage

1. Populate `configs/default.yaml` with your API keys.
2. Run the pipeline:

   ```bash
   python src/main.py --step ingestion  # pick trending topics
   python src/main.py --step all        # full end-to-end run
   ```
3. Generated videos appear in `output/videos/`.

---

## 📄 Deliverables

* **Source Code**: All Python modules under `src/`.
* **Generated Videos**: 30–60s clips in `output/videos/`.
* **Report**: Detailed steps & design rationale in `docs/report.pdf`.

---

## 🤝 Contributing

Contributions welcome! Please open an issue or submit a pull request.

---

