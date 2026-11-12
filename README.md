<div align="center">

# 🧠 Rainbow Memory Game

**A colorful, animated emoji memory-matching game for your browser.**
Flip cards, find every pair, and climb the leaderboard. 🌈

</div>

---

## 📖 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Getting Started](#-getting-started)
- [How to Play](#-how-to-play)
- [Customization](#-customization)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Browser Support](#-browser-support)
- [Data & Privacy](#-data--privacy)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 About

Rainbow Memory Game is a classic card-matching game built with pure **HTML, CSS, and vanilla JavaScript**. There is nothing to install, no build step, and no frameworks. Just open the file and play.

It focuses on a delightful look and feel: smooth 3D card flips, sparkles, twinkling stars, a cursor sparkle trail, confetti on victory, and a light/dark theme.

---

## ✨ Features

| | Feature | Details |
|---|---|---|
| 🎮 | **Difficulty levels** | Easy (4 pairs), Medium (6 pairs), Hard (8 pairs) |
| 🎨 | **Emoji themes** | Animals 🐶, Food 🍔, Sports ⚽ |
| 🏆 | **Leaderboard** | Saves your top 10 scores, ranked by fewest moves, then fastest time |
| ⏱️ | **Live stats** | Move counter and running timer |
| 🌗 | **Light / dark mode** | One-click toggle (🌞 / 🌙) |
| 🃏 | **3D card flips** | Smooth flip animation with matched-card glow |
| 🎆 | **Visual effects** | Flip sparkles, twinkling stars, cursor trail, victory confetti |
| 📱 | **Responsive** | Cards scale for desktop, tablet, and mobile screens |
| 🪶 | **Zero dependencies** | One self-contained HTML file |

---

## 🚀 Getting Started

No installation or extra tools are required.

1. **Download or clone** this repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   ```
2. **Open `settings.html`** in any modern browser (double-click the file).
3. **Play!** 🎉

> 💡 An internet connection is needed on first load for the Google Fonts (Parisienne, Great Vibes, Dancing Script). Without it, the game still works and falls back to a default cursive font.

### 🌍 Host it online (optional)

Publish for free with **GitHub Pages**:

1. Go to **Settings → Pages** in your repository.
2. Under **Source**, choose your branch (e.g. `main`) and the `/ (root)` folder.
3. Save. Your game will be available at:
   `https://<your-username>.github.io/<your-repo>/settings.html`

> Tip: rename `settings.html` to `index.html` if you want the game to open at the root URL without a filename.

---

## 🕹️ How to Play

1. Enter your **name** (leave blank to play as "Player").
2. Choose a **difficulty** and an **emoji theme**.
3. Click **Start Game**. The timer begins immediately.
4. Click a card to flip it, then flip a second card.
   - ✅ **Match:** both cards stay face-up and glow.
   - ❌ **No match:** both cards flip back after one second.
5. Match every pair to win. Your result is saved to the leaderboard and confetti celebrates your win. 🎊

### Difficulty levels

| Difficulty | Pairs | Total cards |
|------------|:-----:|:-----------:|
| Easy       | 4     | 8           |
| Medium     | 6     | 12          |
| Hard       | 8     | 16          |

### Scoring

- Fewer **moves** ranks higher.
- If moves are tied, the faster **time** wins.
- A move is counted each time you flip a second card.

---

## 🎨 Customization

### Add a new emoji theme

Edit the `themes` object in the `<script>` section. Each theme needs **8 emojis** so that Hard mode works:

```js
const themes = {
  animals: ["🐶","🐱","🦊","🐻","🐼","🐨","🦁","🐸"],
  food:    ["🍔","🍕","🍟","🌭","🍣","🍦","🍩","🍫"],
  sports:  ["⚽","🏀","🏈","🎾","🏓","🏸","🥊","🏐"],
  space:   ["🚀","🌍","🌙","⭐","🪐","☄️","👽","🛸"]   
};
```

Then add it to the theme dropdown:

```html
<option value="space">🚀 Space</option>
```

### Change the number of pairs

In `setupBoard()`:

```js
let pairs = difficulty === "easy" ? 4 : difficulty === "medium" ? 6 : 8;
```

### Change colors and fonts

Edit the gradient values and `font-family` rules in the `<style>` section (for example `body`, `.card-front`, and `.card-back`) to create your own look.

---

## 🛠️ Tech Stack

- **HTML5** for structure
- **CSS3** for gradients, 3D transforms, keyframe animations, and media queries
- **Vanilla JavaScript (ES6)** for game logic, timer, and DOM effects
- **Web Storage (`localStorage`)** for leaderboard persistence
- **Google Fonts** for typography

---

## 📁 Project Structure

```
.
├── settings.html    # Markup, styles, and game logic (all in one file)
└── README.md        # Project documentation
```

---

## 🌐 Browser Support

Works on current versions of **Chrome, Edge, Firefox, and Safari**, on desktop and mobile.

---

## 🔒 Data & Privacy

Leaderboard scores are stored **only in your own browser** via `localStorage`. Nothing is sent to a server, and no personal data is collected. Click **Clear Leaderboard** at any time to erase your scores.

---

## 🗺️ Roadmap

- [ ] 🔊 Sound effects and music
- [ ] 👥 Two-player mode
- [ ] 💾 Separate leaderboards per difficulty
- [ ] 🎚️ Custom grid sizes and more themes
- [ ] ⌨️ Keyboard and screen-reader accessibility
- [ ] ⏸️ Pause button

---

## 🤝 Contributing

Contributions, issues, and feature ideas are welcome!

1. Fork the repository
2. Create a branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m "Add my feature"`
4. Push to your branch: `git push origin feature/my-feature`
5. Open a Pull Request

---

## 📄 License

Distributed under the **MIT License**. Add a `LICENSE` file to your repository to make this official, or replace this section with the license of your choice.

---

<div align="center">

Made with ❤️ and a lot of sparkles ✨

⭐ If you enjoyed this game, consider giving the repo a star!

</div>
