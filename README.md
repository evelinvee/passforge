# 🔐 PassForge

A password generator and strength checker in a single HTML file. It produces cryptographically secure passwords, shows each one's entropy in bits, and rates any password you paste — all locally, with nothing ever sent anywhere.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=black)
![No dependencies](https://img.shields.io/badge/dependencies-0-3ce6ff)
![License](https://img.shields.io/badge/license-MIT-9b5cff)

> **Try it live:** https://evelinvee.github.io/passforge/ — or download `index.html` and run it fully offline. Nothing leaves your browser.

---

## ✨ Features

- **10 passwords at once**, each showing its **entropy in bits** with colour-coded digits & symbols
- **Adjustable length** (6–48) and toggles for character sets (A–Z, a–z, 0–9, symbols)
- **Exclude look-alikes** (`il1IoO0…`) and brackets for easier typing
- **Guaranteed mix** — at least one character from each selected set
- **Cryptographically secure** via `crypto.getRandomValues` (rejection sampling — no modulo bias)
- **Strength checker** — paste any password to see its rating and entropy update live
- **100% offline & private** — no network requests, no tracking, no storage

**How strength is measured** — entropy in bits (`length × log₂(poolSize)`):

| Entropy | Rating |
| --- | --- |
| under 40 bits | Weak |
| 40–60 bits | Fair |
| 60–90 bits | Strong |
| 90+ bits | Very strong |

## ▶️ Use it

- **Live:** https://evelinvee.github.io/passforge/
- **Locally:** download `index.html` and open it in any modern browser.

## 🗂️ Structure

```
index.html   # generator + strength checker, all in one file
README.md
LICENSE
```

## 🛠️ Tech

Pure **HTML5 + vanilla JavaScript**, single file, no libraries or build step. The Web Crypto API does the heavy lifting.

## 📄 License

MIT © [evelinvee](https://github.com/evelinvee)
