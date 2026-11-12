# 🧠 Rainbow Memory Game

A colorful, animated emoji memory-matching game that runs entirely in the browser. It is a single HTML file, so it needs no installation, build step, or dependencies.

Flip the cards, find all the matching pairs, and beat your own best score. 🌈

---

## ✨ Features

- 🎮 **3 difficulty levels**: Easy (4 pairs), Medium (6 pairs), Hard (8 pairs)
- 🎨 **3 emoji themes**: Animals 🐶, Food 🍔, Sports ⚽
- 🏆 **Persistent leaderboard**: saves your top 10 scores, ranked by fewest moves and then fastest time
- ⏱️ **Live tracking** of moves and elapsed time
- 🌙 **Light and dark mode** toggle (🌞 / 🌙)
- 🃏 **Smooth 3D card flip** animations
- 🎆 **Visual effects**: card-flip sparkles, twinkling stars, a cursor sparkle trail, and a confetti celebration on win
- 📱 **Responsive design** that works on desktop, tablet, and mobile

---

## 🚀 Getting Started

### Option 1: Open directly
1. Save the code as `index.html`.
2. Double-click the file to open it in any modern browser.

### Option 2: Serve locally (optional)
```bash
# Python 3
python -m http.server 8000

# or Node.js
npx serve .
```
Then visit `http://localhost:8000`.

> 💡 An internet connection is needed on first load for the Google Fonts (Parisienne, Great Vibes, Dancing Script). If they cannot load, the game falls back to a default cursive font.

---

## 🕹️ How to Play

1. Enter your **name** (or leave it blank to play as "Player").
2. Choose a **difficulty** and an **emoji theme**.
3. Click **Start Game**.
4. Click cards to flip them and find matching pairs.
5. Match all pairs to win. Your score is saved to the leaderboard automatically.

| Difficulty | Pairs | Cards |
|------------|:-----:|:-----:|
| Easy       | 4     | 8     |
| Medium     | 6     | 12    |
| Hard       | 8     | 16    |

**Scoring:** fewer moves is better. If two players tie on moves, the faster time wins.

---

## 🛠️ Built With

- **HTML5**: structure
- **CSS3**: gradients, 3D transforms, keyframe animations, responsive media queries
- **Vanilla JavaScript**: game logic, timer, DOM effects
- **localStorage**: leaderboard persistence
- **Google Fonts**: Parisienne, Great Vibes, Dancing Script

---

## 🎨 Customization

### Add a new emoji theme
Edit the `themes` object in the script. Each theme needs **8 emojis** (so Hard mode works):

```js
const themes = {
  animals: ["🐶","🐱","🦊","🐻","🐼","🐨","🦁","🐸"],
  food:    ["🍔","🍕","🍟","🌭","🍣","🍦","🍩","🍫"],
  sports:  ["⚽","🏀","🏈","🎾","🏓","🏸","🥊","🏐"],
  space:   ["🚀","🌍","🌙","⭐","🪐","☄️","👽","🛸"]   // new theme
};
```

Then add a matching option to the theme dropdown:

```html
<option value="space">🚀 Space</option>
```

### Change difficulty sizes
In `setupBoard()`, adjust the number of pairs:

```js
let pairs = difficulty === "easy" ? 4 : difficulty === "medium" ? 6 : 8;
```

### Change colors
Edit the gradient values in the CSS (for example the `body`, `.card-front`, and `.card-back` rules) to create your own palette.

---

## 📁 Project Structure

```
rainbow-memory-game/
├── index.html    # Everything: markup, styles, and game logic
└── README.md     # You are here
```

---

## 🔒 Data & Privacy

Leaderboard scores are stored **only in your browser** using `localStorage`. Nothing is sent to any server. Use the **Clear Leaderboard** button to reset your scores at any time.

---

## 🌐 Browser Support

Works on the latest versions of Chrome, Edge, Firefox, Safari, and their mobile counterparts.

---

## 💡 Ideas for Future Improvements

- 🔊 Sound effects and background music
- 🎚️ More themes and a custom grid size
- 👥 Two-player mode
- 💾 Separate leaderboards per difficulty
- ⌨️ Keyboard accessibility for card selection

---

## 📄 License

This project is free to use, modify, and share. Have fun! 🎉
