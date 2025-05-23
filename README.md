## AVGen
**AI Video Generation Tool**

A Python-based application that automatically generates 30–60 second videos by scraping trending news and social media topics, creating a script, and composing video segments with text overlays and images.

---

## Features

* **Trending Topic Ingestion**
  • Scrape news headlines (RSS/NewsAPI) and social media hashtags (Twitter/Reddit).
  • Rank and deduplicate topics by recency and popularity.

* **Automated Script Generation**
  • AI-driven script writer producing concise narratives for each topic.

* **Media Asset Sourcing**
  • Fetch relevant images and short clips via public APIs (e.g., Unsplash).

* **Video Rendering**
  • Assemble text overlays, images, and clips into polished 30–60 second videos using MoviePy.

* **Configurable & Modular**
  • YAML-based configuration.
  • Modular source structure for easy extension.

---

## Folder Structure

```plaintext
ai_video_gen/
├── configs/           # Configuration files (API keys, thresholds)
│   └── config.yaml
├── data/
│   ├── raw/           # Raw JSON/HTML dumps
│   └── processed/     # Cleaned topic data
├── src/               # Application modules
│   ├── ingestion/     # Trending-topic scrapers & ranker
│   ├── scripting/     # Script generator
│   ├── media/         # Asset fetcher
│   ├── render/        # Video builder
│   ├── utils/         # Helpers & logger
│   └── main.py        # Entry point
├── output/
│   ├── videos/        # Generated videos
│   └── scripts/       # Generated scripts
├── requirements.txt   # Python dependencies
├── .env.example       # Environment variables template
└── README.md          # Project overview
```

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-org/ai_video_gen.git
   cd ai_video_gen
   ```
2. Create and activate a virtual environment:

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
4. Copy and fill in environment variables:

   ```bash
   cp .env.example .env
   ```

---

## Usage

Run the main pipeline to fetch topics, generate scripts, and render videos:

```bash
python src/main.py --config configs/config.yaml
```

Outputs will appear under `output/scripts/` and `output/videos/`.

---

## Configuration

Edit `configs/config.yaml` to set your API keys, topic thresholds, and output settings.

---


