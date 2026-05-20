# 📐 Euler's Theorem — Homogeneous Functions Explorer

> An interactive, browser-based tool to **symbolically verify Euler's Theorem** for any multivariable function f(x, y) — hosted instantly via GitHub Pages.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=flat-square&logo=github)](https://your-username.github.io/eulers-theorem-explorer)
[![Math.js](https://img.shields.io/badge/Powered%20by-math.js-orange?style=flat-square)](https://mathjs.org)
[![KaTeX](https://img.shields.io/badge/Rendered%20with-KaTeX-green?style=flat-square)](https://katex.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)

---

## 🧮 What is Euler's Theorem?

A function **f(x, y)** is called **homogeneous of degree n** if scaling every variable by a constant λ scales the output by λⁿ:

$$f(\lambda x, \lambda y) = \lambda^n \, f(x, y) \qquad \forall\, \lambda > 0$$

**Euler's Theorem** states that any such function satisfies:

$$x \frac{\partial f}{\partial x} + y \frac{\partial f}{\partial y} = n \cdot f(x, y)$$

This elegant identity connects a function's partial derivatives back to itself, appearing throughout:

| Field | Application |
|---|---|
| **Thermodynamics** | Extensive vs. intensive state variables |
| **Economics** | Returns to scale in production functions |
| **Fluid Mechanics** | Dimensional analysis of flow equations |
| **Physics** | Scaling laws in classical mechanics |

---

## ✨ Features

- 🔣 **Symbolic differentiation** — computes `∂f/∂x` and `∂f/∂y` analytically using **math.js**
- 📐 **Beautiful math rendering** — all expressions displayed as proper mathematical notation via **KaTeX**
- ✅ **Step-by-step proof** — shows the full derivation: given → partials → LHS → RHS → verdict
- 🔢 **Numerical verification** — cross-checks equality at multiple test points for confidence
- 💡 **Built-in examples** — one click to try classic homogeneous functions
- ⚡ **Zero dependencies to install** — pure client-side HTML/CSS/JS, works offline after first load
- 🌑 **Dark theme** — easy on the eyes for extended study sessions

---

## 🚀 Live Demo & Deployment

### Option 1 — GitHub Pages (Recommended, free)

1. **Fork** this repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, root `/`
4. Your site will be live at:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```

### Option 2 — Run Locally

No build step, no server required:

```bash
git clone https://github.com/your-username/eulers-theorem-explorer.git
cd eulers-theorem-explorer

# Open directly in browser
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

Or serve with any static server:

```bash
# Python 3
python -m http.server 8080

# Node (npx)
npx serve .
```

Then visit `http://localhost:8080`.

---

## 🛠 Tech Stack

| Technology | Role | Version |
|---|---|---|
| [math.js](https://mathjs.org) | Symbolic differentiation & simplification | 12.x |
| [KaTeX](https://katex.org) | LaTeX math rendering in the browser | 0.16.x |
| HTML5 / CSS3 / Vanilla JS | UI, layout, animations | — |
| GitHub Pages | Free static hosting | — |

All libraries are loaded from CDN — no `npm install` needed.

---

## 📂 Repository Structure

```
eulers-theorem-explorer/
├── index.html          # Complete app (HTML + CSS + JS in one file)
├── README.md           # This file
└── LICENSE             # MIT License
```

---

## 🧪 Supported Function Syntax

The input field accepts standard mathematical notation (math.js syntax):

| Math | Input |
|---|---|
| x³ + y³ | `x^3 + y^3` |
| √(x² + y²) | `sqrt(x^2 + y^2)` |
| x²y | `x^2 * y` |
| (x² + y²)/(x + y) | `(x^2 + y^2) / (x + y)` |
| sin(x/y) · y² | `sin(x/y) * y^2` |
| eˣ/ʸ · y | `exp(x/y) * y` |

**Supported functions:** `sqrt`, `cbrt`, `exp`, `log`, `sin`, `cos`, `tan`, `abs`, and all standard math.js functions.

---

## 📖 Example Walkthrough

**Function:** `f(x, y) = x³ + xy² + y³` &nbsp;&nbsp; **Degree:** n = 3

| Step | Result |
|---|---|
| ∂f/∂x | 3x² + y² |
| ∂f/∂y | 2xy + 3y² |
| LHS = x·(∂f/∂x) + y·(∂f/∂y) | 3x³ + xy² + 2xy² + 3y³ = 3(x³+xy²+y³) |
| RHS = 3·f(x,y) | 3(x³+xy²+y³) |
| **Verdict** | ✅ LHS = RHS — Theorem verified! |

---

## 🤝 Contributing

Contributions are welcome! Ideas for improvement:

- [ ] Extend to 3-variable functions f(x, y, z)
- [ ] Add a plot of f(x, y) as a 3D surface
- [ ] Support complex-valued functions
- [ ] Add PDF export of the proof

Please open an issue or submit a pull request.

---

## 📄 License

[MIT License](LICENSE) — free to use, modify, and distribute.

---

*Built for learning · Computer Engineering & Multivariate Calculus*
