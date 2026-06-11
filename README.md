# ✦ stellaire — daily tarot

> *a quiet bloom tarot ritual. three cards for your day.*

**🔮 Live Demo: https://jdoobleu.github.io/stellaire-tarot/**

A daily tarot reading web app with a full 78-card deck, dreamy silver-fog aesthetics, and a one-reading-per-day ritual. Open it every morning, draw three cards, and receive a gentle fortune for your day — in Korean or English.

---

## ✦ Features

- **Full 78-card deck** — 22 Major Arcana + 56 Minor Arcana (Wands · Cups · Swords · Pentacles), each with original AI-generated artwork and hand-written interpretations in both Korean and English
- **Daily three-card reading** — Today's Flow · Gentle Advice · Lucky Key
- **One reading per day** — your reading is saved on your device (localStorage); revisit anytime today, draw again tomorrow
- **Interactive animations** — cards fan out from a shuffled deck, fly to their slots when picked, and flip open with a burst of stars
- **Today's luck** — a lucky color & number generated from the date + your card combination
- **Daily affirmation** — tap for a gentle one-line affirmation
- **Card library** — browse all 78 cards with imagery, keywords, and meanings, filterable by suit
- **KO / EN toggle** — full bilingual interface and readings
- **Mobile-first & installable** — swipe through the deck on your phone; add to home screen for an app-like experience (PWA)

## ✦ How it works

- Pure **HTML / CSS / vanilla JavaScript** — no frameworks, single-page
- **Fisher–Yates shuffle** for unbiased card randomization
- **FLIP-style animations**: picked cards animate from the spread to their slot using measured coordinates
- **3D card flips** via CSS `transform-style: preserve-3d` with overshoot easing
- **Date-seeded luck**: lucky color/number derive from today's date + drawn card indices
- **localStorage** powers the one-reading-per-day lock and same-day restore
- **Paper-grain texture** generated with an inline SVG `feTurbulence` filter
- Card images created with **Midjourney** from custom prompts, then connected by a filename convention (`major_00.jpg`, `cups_07.jpg`, …)

## ✦ File structure

```
stellaire-tarot/
├── index.html      # the entire app — markup, styles, data, logic
├── manifest.json   # PWA manifest (add-to-home-screen)
└── images/         # 78 card artworks (.jpg)
```

## ✦ Run / Deploy

No build step. Open `index.html` in a browser, or deploy by enabling **GitHub Pages** (Settings → Pages → main branch).

## ✦ Credits

- Concept, design direction, interpretations & code: **kiwouie**
- Card artwork: generated with Midjourney from original prompts
- Typefaces: Cormorant Garamond, Gowun Batang (Google Fonts)

---

*✦ have a soft day ✦*
