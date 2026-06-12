# ✦ stellaire — daily tarot

> *a quiet bloom tarot ritual. ask, draw three cards, and receive an answer for your day.*

**🔮 Live Demo: https://jdoobleu.github.io/stellaire-tarot/**

A daily tarot reading web app with a full 78-card deck and dreamy silver-fog aesthetics. Write today's question (or leave it blank), draw three cards, and receive a personalized reading — the app detects what your question is about (love, work & study, money, or a decision) and composes a synthesized answer from your card combination. Two questions per day, in Korean or English.

---

## ✦ Features

- **Ask the cards** — type today's question or mood; the app analyzes its topic (love · work/study · money · decisions · general) and the three cards you draw compose a tailored answer in **"Today's Message"**
- **Full 78-card deck** — 22 Major Arcana + 56 Minor Arcana (Wands · Cups · Swords · Pentacles), each with original AI-generated artwork and hand-written interpretations in both Korean and English
- **Three-card spread** — Today's Flow · Gentle Advice · Lucky Key
- **Two readings per day** — each reading is saved on your device (localStorage); ask once more if you need, then the deck rests until tomorrow
- **Interactive animations** — cards fan out from a shuffled deck, fly to their slots when picked, and flip open with a burst of stars
- **Today's luck** — a lucky color & number generated from the date + your card combination
- **Daily affirmation** — tap for a gentle one-line affirmation
- **Card library** — browse all 78 cards with imagery, keywords and meanings in an in-page overlay, filterable by suit
- **Share your fortune** — the full reading (question, all three interpretations, today's message, and your luck) via the native share sheet or clipboard
- **KO / EN toggle** — fully bilingual interface and readings
- **Mobile-first & installable** — swipe through the deck on your phone; add to home screen for an app-like experience (PWA)

## ✦ How it works

- Pure **HTML / CSS / vanilla JavaScript** in a single file — no frameworks, no backend
- **Question topic detection**: keyword analysis (KO/EN) routes the question to one of five topics, which shapes the closing message of the reading
- **Reading synthesis**: the lead keywords of the three drawn cards are woven into a composed "Today's Message" paragraph that answers the question
- **Fisher–Yates shuffle** for unbiased card randomization
- **FLIP-style animations**: picked cards animate from the spread to their slot using measured coordinates
- **3D card flips** via CSS `transform-style: preserve-3d` with overshoot easing, plus radial star-particle bursts
- **Date-seeded luck**: lucky color/number derive deterministically from today's date + drawn card indices
- **localStorage** powers the two-readings-per-day limit and same-day restore
- **Paper-grain texture** generated with an inline SVG `feTurbulence` filter
- Card images created with **Midjourney** from custom prompts, connected by a filename convention (`major_00.jpg`, `cups_07.jpg`, …)

## ✦ File structure

```
stellaire-tarot/
├── index.html      # the entire app — markup, styles, card data, logic
├── manifest.json   # PWA manifest (add-to-home-screen)
└── images/         # 78 card artworks (.jpg) + app icons
```

## ✦ Run / Deploy

No build step. Open `index.html` in a browser, or deploy by enabling **GitHub Pages** (Settings → Pages → main branch).

> Testing tip: readings are limited to two per day. To reset during development, run `localStorage.clear()` in the browser console and refresh.

## ✦ Credits

- Concept, design direction, interpretations & code: **Jeongwon Kim**
- Card artwork: generated with Midjourney from original prompts
- Typefaces: Cormorant Garamond, Gowun Batang (Google Fonts)

---

*✦ have a soft day ✦*
