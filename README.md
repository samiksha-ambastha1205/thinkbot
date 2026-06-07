# ThinkBot 
A simple AI-powered learning tool built with HTML, CSS, and JavaScript. 

---

## What It Does

ThinkBot takes any text or topic you type and sends it to an AI model, then displays the response. It has 6 built-in modes:

| Mode | What it does |
|---|---|
|  Explain Concept | Clear definition + example |
|  Summarize | 3–5 key points from any text |
|  ELI5 | Explain Like I'm 5 |
|  Quiz Questions | 5 Q&As with answers |
|  Bullet Points | Convert any text to bullets |
|  Flashcards | 5 Front/Back study cards |

---

## Features

- 6 AI-powered modes
- Session history 
- Loading animation while waiting for response
- Empty input validation with error messages
- Character counter (max 2000)

---

## How to Run

1. Download `index.html`
2. Open it in any browser (Chrome, Firefox, Edge)
3. Pick a mode, type your topic, click **Run**


---

## API

Uses **OpenRouter** (`openrouter/auto`) which automatically picks the best available free model.

- API: [openrouter.ai](https://openrouter.ai)
- Cost: Free
- No credit card required

To get key:
1. Go to [openrouter.ai](https://openrouter.ai) → Sign up
2. Go to **Keys** → **Create Key**
3. Replace the key in `index.html` at the top of the `<script>` section:

```js
const API_KEY = "your-key-here";
```
## API Key Security

GitHub blocks commits that contain exposed API keys, and API keys should never be stored directly in public frontend code.

Since ThinkBot is built as a frontend-only project (HTML, CSS, and JavaScript) and does not use a backend server, there is no secure place to store secrets such as API keys using environment variables (`.env` files).

To keep API keys private:

* Users enter their own OpenRouter API key through the input field at the top of the application.
* The key is stored only in the browser session using `sessionStorage`.
* The key is never hardcoded into the source code or committed to GitHub.
* This approach prevents accidental exposure of API keys in public repositories.

In a production application, API requests would typically be routed through a backend server where API keys can be stored securely using environment variables.

---

## Project Structure

```
ai_tool/
├── index.html   ← entire app (HTML + CSS + JS in one file)
└── README.md    ← this file
```

---

## Demo Script (2 minutes)

1. Open the app — show the 6 mode buttons
2. **Explain Concept** → type `"What is recursion?"` → Run
3. **ELI5** → type `"What is photosynthesis?"` → Run
4. **Flashcards** → type `"Python lists"` → Run
5. Scroll down → show Session History → click a past result to reload it
6. Click Run with empty input → show the error message

---

## Built With

- HTML / CSS / JavaScript 
- [OpenRouter API](https://openrouter.ai) for AI inference
- [Google Fonts](https://fonts.google.com) — Syne + DM Mono

---

## Notes

- The API key in the code is for demo/learning purposes only
- Do not share your API key publicly
- Free tier has rate limits — if one model is busy, `openrouter/auto` switches automatically

---
