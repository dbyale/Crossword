# Lions Crossword Creator

> A complete, browser-based crossword puzzle system built entirely with vanilla HTML, CSS, and JavaScript.

[lionscrossword.com](https://lionscrossword.com)

## Overview

This project consists of two interconnected applications:

- **Crossword Creator** — A full-featured tool for creating crossword puzzles. Build puzzles from scratch, choose from multiple grid sizes (Standard 15×15, Magazine 17×17, Sunday 21×21, Mini 5×5, French 9×9, Italian 13×21, and more), manage across and down hints, generate answer keys, and export puzzles as images or custom `.cswd` files.

- **Crossword Player** — A companion application for solving crosswords. Load `.cswd` files created in the Creator or pick from pre-made puzzles. Tracks unique puzzles completed and weekly streaks.

This project was my experience learning to build a full website from bare JavaScript, CSS, and HTML — before AI became a widespread coding tool. It was also my contribution to **Lions Crossword**, the school club I was part of, dedicated to creating and sharing crossword puzzles.

## Technical Highlights

- **Dynamic DOM rendering** — Grid generation and real-time cell manipulation without any frameworks
- **Custom `.cswd` file format** — Designed and implemented full import/export support for user-created puzzles
- **Grid traversal algorithm** — Extracts valid across and down words from a 2D grid layout
- **Canvas API integration** — Exports puzzles and answer keys as downloadable images via `html2canvas`
- **Cookie-based persistence** — Auto-saves progress and tracks statistics (unique puzzles, streaks) client-side
- **Fully responsive UI** — Built entirely with raw CSS and vanilla JavaScript, no frameworks

## How to Run

```bash
git clone https://github.com/dbyale/crossword.git
cd crossword
# Open index.html in your browser
# Or serve locally (requires Node.js):
npx http-server -p 8000
```

## Project Structure

```
crossword/
├── index.html              # Crossword Creator entry point
├── about.html              # About / club info page
├── createBoard.js          # Grid generation logic
├── hints.js                # Hint management
├── answerKey.js            # Answer key generation & export
├── autoSaveCookie.js       # Local persistence layer
├── player/                 # Crossword Player application
│   ├── player.html
│   ├── loadCrossword.js
│   └── crosswordCookies.js
├── assets/
│   ├── css/                # Stylesheets
│   ├── libraries/          # html2canvas
│   └── preMadeFiles.js     # Pre-made puzzle data
└── LICENSE
```

## License

This project is licensed under the [MIT License](LICENSE).
