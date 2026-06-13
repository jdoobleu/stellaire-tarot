# ✦ stellaire — daily tarot

> *a quiet bloom tarot ritual. ask, draw three cards, and receive an answer for your day.*

**🔮 Live: https://jdoobleu.github.io/stellaire-tarot/**

A daily tarot reading web app with a full 78-card deck and dreamy silver-fog aesthetics. Write today's question (or leave it blank), draw three cards, and receive a personalized reading. The app detects what your question is about and weaves your three cards into a synthesized answer — and because every reading is composed from a large pool of sentence variations, the same card rarely reads the same way twice. Two readings per day, fully bilingual (Korean / English), installable on your phone.

*Final project for AAT2004 <Introduction to Creative Computing>, Sogang University (2026) — Jeongwon Kim*

---

## ✦ Features

- **Ask the cards** — type today's question or mood; the app analyzes its topic (love · work/study · money · decision · general) and your three cards compose a tailored answer in **"Today's Message"**
- **Full 78-card deck** — 22 Major Arcana + 56 Minor Arcana (Wands · Cups · Swords · Pentacles), each with original AI-generated artwork and hand-written interpretations in Korean and English
- **Three-card spread** — Today's Flow · Gentle Advice · Lucky Key
- **Upright / reversed cards** — each card may appear reversed (30% chance), adding a distinct reversed reading
- **Sentence variation** — readings assemble from 6 intros × 10 closers × 6 synthesis templates, so a card reads differently each day
- **Two readings per day** — saved on your device; ask once more if you need, then the deck rests until tomorrow
- **Today's record** — every reading taken today (question + answer) accumulates below the result
- **Today's luck** — a lucky color & number from the date + your card combination
- **Daily affirmation** — tap for a gentle one-line affirmation
- **Save as image** — export the reading as a 1080×1920 image for social sharing
- **Share & compare** — share the full reading; the link lets a friend open it and compare their own draw side by side
- **One-card quick answer** — a mini mode answering a short question with a single card
- **Card of the week** — one card fixed for the week, refreshing each Monday
- **Reading history** — your last 30 readings in an overlay
- **Card library** — browse all 78 cards (imagery, keywords, meanings), filter by suit, search by name/keyword
- **Time-of-day background** — the fog palette shifts by access time (dawn / day / evening / night)
- **Ambient sound** — optional synthesized chimes on shuffle, pick, and flip (Web Audio, no files)
- **KO / EN toggle** — full bilingual interface and readings
- **Mobile-first & installable** — swipe deck on phone; add to home screen for an app-like PWA

## ✦ How it works

- Pure **HTML / CSS / vanilla JavaScript** in a single file — no frameworks, no backend
- **Fisher–Yates shuffle**; deck assembled from an object array (Major) + a nested suit×rank loop (Minor)
- **Topic detection + reading synthesis**: keyword analysis routes the question to a topic; a seeded template weaves the three cards' keywords into the answer
- **FLIP-style animation**: picked cards fly from spread to slot using measured coordinates; **3D flips** via `preserve-3d`; radial **star-particle bursts** with cos/sin
- **Date-seeded luck** from the date + drawn card indices
- **localStorage** for the two-per-day limit, same-day restore, history, weekly card, and sound preference
- **Canvas API** for save-as-image, **Web Audio** for synthesized sound, **Web Share / Clipboard** for sharing, **Base64 URL** for friend comparison
- **Inline SVG feTurbulence** paper-grain texture; **PWA** manifest for home-screen install
- Card images created with **Midjourney** from custom prompts, linked by filename convention

## ✦ File structure

```
stellaire-tarot/
├── index.html      # the entire app — markup, styles, card data, logic
├── manifest.json   # PWA manifest (add-to-home-screen)
└── images/         # 78 card artworks (.jpg) + app icons
```

## ✦ Run / Deploy

No build step. Open `index.html` in a browser, or deploy via **GitHub Pages** (Settings → Pages → main branch).

> Dev tip: readings are limited to two per day. To reset during testing, run `localStorage.clear()` in the browser console and refresh.

## ✦ Credits

- Concept, design direction, interpretations & code: **Jeongwon Kim**
- Card artwork: generated with Midjourney from original prompts
- Typefaces: Cormorant Garamond, Gowun Batang (Google Fonts)

---

*✦ have a soft day ✦*
