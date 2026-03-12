# 🔬 Life Of Research — WEB Edition

[![Deploy Life Of Research WEB to GitHub Pages](https://github.com/PranayMahendrakar/life-of-research-web/actions/workflows/deploy.yml/badge.svg)](https://github.com/PranayMahendrakar/life-of-research-web/actions/workflows/deploy.yml)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-orange?style=flat-square&logo=github)](https://pranaymahendrakar.github.io/life-of-research-web/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with HTML5](https://img.shields.io/badge/Made%20with-HTML5%20%2B%20JS-red?style=flat-square)](https://developer.mozilla.org/en-US/docs/Web/HTML)

> **Full browser-based conversion of the PySide6 "Life Of Research" desktop application.**  
> Same 11-agent AI pipeline, same 3-panel UI, same real-time streaming — runs entirely in your browser. No installation required.

## 🌐 Live App

**👉 [https://pranaymahendrakar.github.io/life-of-research-web/](https://pranaymahendrakar.github.io/life-of-research-web/)**

---

## ✨ Features

| Feature | Description |
|---|---|
| 🤖 11 AI Agents | Hypothesis Generator, Literature Intelligence, Debate Mode, Reviewer, Statistician, Ethics Committee, Innovation Scout, Devil's Advocate, Synthesizer, Impact Predictor, Final Judge |
| 🔄 Real-time Streaming | SSE token-by-token streaming via OpenAI fetch API |
| 📊 Score Rings | Live canvas-rendered score rings (Latest & Best scores) |
| 📈 Score Graph | Score progression chart across pipeline loops |
| 🕸️ Knowledge Graph | Agent connection visualization with canvas |
| 🏆 Achievement System | Unlockable badges based on scores and milestones |
| 💬 Debate Mode | Toggle adversarial agent debate on/off |
| 📤 Export | Download results as Markdown, HTML, TXT, or JSON |
| 🎨 3-Panel Layout | Config panel · Chat feed · Scores/Pipeline/Graph/Memory |
| 🔑 API Key | Bring your own OpenAI API key — never stored on server |

---

## 🚀 Quick Start

**No installation needed!** Just open the live app:

1. Go to **[https://pranaymahendrakar.github.io/life-of-research-web/](https://pranaymahendrakar.github.io/life-of-research-web/)**
2. Enter your **OpenAI API Key** in the left panel
3. Choose your **model** (gpt-4o, gpt-4o-mini, gpt-4-turbo, gpt-3.5-turbo)
4. Type your **research topic** (e.g., "Efficient KV Cache Optimization in Large Language Models")
5. Select **paper type** and **citation style**
6. Set **max loops** and **stop score** threshold
7. Click **▶ LAUNCH RESEARCH LAB**
8. Watch the agents work in real-time!

---
## 🏗️ Architecture

```
Single-file Web App (index.html)
├── HTML Structure     — 3-panel layout matching PySide6 desktop app
├── CSS Styling        — Dark theme, monospace fonts, animated elements
├── JavaScript Core    — State management, pipeline orchestration
├── OpenAI Integration — Direct browser fetch() with SSE streaming
├── Canvas Rendering   — Score rings, score graph, knowledge graph
└── Export Engine      — Blob-based client-side file downloads
```

### AI Agent Pipeline Flow

```
LOOP START
    │
    ├─► [1] Hypothesis Generator    — Generates research hypothesis
    ├─► [2] Literature Intelligence — Reviews related literature
    ├─► [3] Debate Mode (optional)  — Adversarial perspective
    ├─► [4] Peer Reviewer           — Reviews and scores the paper
    ├─► [5] Statistician            — Statistical analysis
    ├─► [6] Ethics Committee        — Ethical implications review
    ├─► [7] Innovation Scout        — Novelty assessment
    ├─► [8] Devil's Advocate        — Challenges assumptions
    ├─► [9] Synthesizer             — Synthesizes all feedback
    ├─► [10] Impact Predictor       — Predicts research impact
    └─► [11] Final Judge            — Final score (0-10) + decision
         │
         ├── Score ≥ threshold? → STOP (export best paper)
         └── Score < threshold? → Revise hypothesis → REPEAT
```

---

## 🛠️ Development

### Run Locally

```bash
git clone https://github.com/PranayMahendrakar/life-of-research-web.git
cd life-of-research-web
# Open index.html in your browser — no build step needed!
open index.html
# Or use a local server:
python -m http.server 8080
# Then visit http://localhost:8080
```

### CI/CD — GitHub Actions

Every push to `main` automatically deploys to GitHub Pages via `.github/workflows/deploy.yml`:

```yaml
on:
  push:
    branches: [main]
jobs:
  deploy:
    - Checkout code
    - Validate HTML
    - Upload artifact
    - Deploy to GitHub Pages
```

---

## 📦 Repository Structure

```
life-of-research-web/
├── index.html                    # Complete web application (single file)
├── README.md                     # This file
└── .github/
    └── workflows/
        └── deploy.yml            # GitHub Actions CI/CD pipeline
```

---

## 🔗 Related

| Project | Link |
|---|---|
| 🖥️ Desktop App (PySide6) | [life-of-research](https://github.com/PranayMahendrakar/life-of-research) |
| 🌐 Web App (this repo) | [life-of-research-web](https://github.com/PranayMahendrakar/life-of-research-web) |
| 🚀 Live Web App | [pranaymahendrakar.github.io/life-of-research-web](https://pranaymahendrakar.github.io/life-of-research-web/) |

---

## 👤 Author

**Pranay Mahendrakar**  
GitHub: [@PranayMahendrakar](https://github.com/PranayMahendrakar)

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

*"Automate the research process, amplify human intelligence."*
