# wyattbrown.info

Source for my personal site. Static HTML, CSS, and a little JavaScript, served by GitHub Pages.

Live at [wrbr0wn.github.io](https://wrbr0wn.github.io) and [wyattbrown.info](https://wyattbrown.info).

## What is here

Two pages. The homepage lists my technical projects and links out to the code or the running app for each. `DrawnAtDusk.html` is my art gallery, 27 acrylic and scratchboard pieces with a lightbox viewer.

## Projects linked from the homepage

- **Hint Bank.** Real-time multiplayer web game. React, TypeScript, Cloudflare Workers. [Play it](https://wrbr0wn.github.io/hintbank/).
- **Vending Machine Assortment Optimization.** Predict-then-optimize over a 239-machine fleet. Python and Julia/JuMP. [Code](https://github.com/WRBr0wn/Vending-Machine-Sales-Public).
- **Pec-King Order.** Multi-agent reinforcement learning under uncertainty. JAX, Flax, gymnax. Course project, code not public.
- **Graphical Particle Simulator.** Java engine behind a Python Flask API, containerized. [Code](https://github.com/WRBr0wn/Particle-Simulator).

## Stack

No build step and no framework. A page loads its CSS, and the gallery additionally loads lightbox for the image viewer. Fonts come from Google Fonts. Every page sets a Content-Security-Policy that restricts scripts to same-origin.

```
├── index.html          Homepage
├── DrawnAtDusk.html    Art gallery
├── 404.html
├── css/
│   ├── modern.css      Layout, theme, all page styles
│   └── lightbox.min.css
├── js/
│   ├── reveal.js       Reveal-on-scroll, degrades to nothing without JS
│   └── lightbox-plus-jquery.min.js
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
