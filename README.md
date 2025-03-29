# CSIS4260_A2_TUSHAR

#  AI & The Future – Reddit Scraping & Text Analysis

##  Project Topic:
**Will AI Take Over the World?**  
This project explores Reddit discussions surrounding the future of Artificial Intelligence, including public fears, hopes, and predictions about AGI (Artificial General Intelligence) and AI takeover.

---

##  Part 1: Web Scraping

- Scraped 100+ Reddit posts using keywords:
  - `"AI takeover"`
  - `"AGI"`
  - `"AI future"`
- Used Reddit's public JSON API with `requests` + `pandas`
- Filtered out empty or very short content
- Posts were pulled from `r/artificial`

###  Scraping Tools Compared:

| Criteria        | BeautifulSoup + Requests       | Playwright (Headless Browser)     |
|----------------|----------------------------------|-----------------------------------|
| Ease of Setup  |  Simple Python-only setup       |  Requires Node.js               |
| Speed          |  Fast (<3 seconds for 100 posts)|  Slow (~10s per post)           |
| Use Case       |  Perfect for API/static pages   |  Needed for JavaScript-heavy    |
| Benchmark Used |  Yes (Reddit API)               |  No                             |
| Chosen?        |  Yes                            |  No                             |

---

## 🤖 Part 2: Text Analysis using Mistral (LLM)

- Used **Mistral 7B** via **Ollama (local LLM server)**
- Each post was analyzed for:
  1. **2–3 sentence summary**
  2. **Impact score** (-10 to +10)
  3. **Tone** – Hopeful or Fearful

###  Sample Prompt:
```
You are an AI analyst. Analyze the following Reddit post about the future of AI and humanity:

POST:
<text>

Tasks:
1. Give a 2–3 sentence summary.
2. Assign a score from -10 (very dangerous) to +10 (very beneficial).
3. Classify tone as Hopeful or Fearful.

Return in this exact format:
Summary: ...
Score: ...
Tone: ...
```

---

##  Files Included

| File                            | Description                               |
|---------------------------------|-------------------------------------------|
| `Tushar_A2.ipynb`            | Main notebook for scraping + analysis     |
| `analysis.csv` | Output with summaries, scores, tone       |
| `requirements.txt`            | Python dependencies                       |


---

## ▶ How to Run This Project

### 1. 🔧 Set up virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

### 2. 💬 Install & Run Ollama
Download: https://ollama.com  
```bash
ollama pull mistral
ollama serve
```

### 3.  Run Notebook
Open `Tushar_A2.ipynb` in Jupyter or VSCode, run all cells.

---

##  Submission Link

All files (code, CSV, report) are available here:  
 [GitHub Repository](https://github.com/tushaarrr/CSIS4260_A2_TUSHAR)



---

##  Author
**Tushar Shandilya 300378305**  
Douglas College – CSIS 4260

---

