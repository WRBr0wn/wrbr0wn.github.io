# wyattbrown.info

Source for my personal site. Static HTML, CSS, and a little JavaScript, served by GitHub Pages.

Live at [wrbr0wn.github.io](https://wrbr0wn.github.io) and [wyattbrown.info](https://wyattbrown.info).

## What is here

Two pages. The homepage covers my experience and technical projects, and links out to the code or the running app where one is public. `DrawnAtDusk.html` is my art gallery, 27 acrylic and scratchboard pieces with a lightbox viewer.

## Projects on the homepage

- **Hint Bank.** Real-time multiplayer web game. React, TypeScript, Cloudflare Workers. [Play it](https://wrbr0wn.github.io/hintbank/).
- **Java-to-TypeScript Port with Claude Code.** A Java transit simulator ported to strict TypeScript, with checks after every edit. Claude Code, TypeScript, Playwright. Course project.
- **Vending Machine Assortment Optimization.** Predict-then-optimize over a 239-machine fleet. Python and Julia/JuMP. [Write-up](https://github.com/WRBr0wn/Vending-Machine-Sales-Public).
- **Trained Head vs. Foundation Model.** A DINOv2-based classifier against zero-shot Gemini 2.5 Flash on Food-101. PyTorch. Course project.
- **Pec-King Order.** Multi-agent reinforcement learning under uncertainty. JAX, Flax, gymnax. Course project.
- **Graphical Particle Simulator.** Java engine behind a Python Flask API, containerized. [Code](https://github.com/WRBr0wn/Particle-Simulator).

## Stack

No build step and no framework. A page loads its CSS, and the gallery additionally loads lightbox for the image viewer. Fonts are self-hosted woff2 files in `fonts/`, preloaded in each page's head and backed by metric-matched fallback faces. Every page sets a Content-Security-Policy that restricts scripts to same-origin.

```
├── index.html          Homepage
├── DrawnAtDusk.html    Art gallery
├── 404.html
├── css/
│   ├── modern.css      Layout, theme, all page styles
│   └── lightbox.min.css
├── js/
│   └── lightbox-plus-jquery.min.js
├── fonts/              Self-hosted Inter and JetBrains Mono (woff2)
├── robots.txt
└── images/
    ├── Full-Gallery/       Full-resolution art, opened by lightbox
    └── Thumbnail-Gallery/  Grid thumbnails
```

## Running it locally

No dependencies. Serve the directory over HTTP so the CSP behaves the same as it does in production:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Contact

[wyattrbrown@gmail.com](mailto:wyattrbrown@gmail.com) · [LinkedIn](https://www.linkedin.com/in/wrbr0wn/) · [GitHub](https://github.com/WRBr0wn)
