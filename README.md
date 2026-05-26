# Eco-Pulse

![Eco-Pulse Banner](https://raw.githubusercontent.com/DavidAkerele/Eco-Pulse/main/assets/banner.png)

**Eco-Pulse** is a sleek, web‑based sandbox that lets developers and curious users interact with large language models while visualising the real‑time carbon impact of every query. The app pulls live grid‑intensity data from the UK National Grid Carbon Intensity API, compares your AI‑generated emissions to regional averages, and helps you stay within a daily carbon budget.

---

## 🎯 Goal
- **Raise awareness** of the environmental cost of AI.
- **Empower developers** to make greener choices (lighter models, optimal query times).
- **Provide instant feedback** via gorgeous, premium UI components (glass‑morphism, dynamic gradients, animated pulse rings).

---

## ✨ Key Features
- **Carbon Budget Tracker** – set daily limits, view streaks, and log each audit.
- **Local Carbon Impact Panel** – pick a UK region, fetch live carbon‑intensity, see fuel‑mix mini‑charts, and compare your emissions to the regional average.
- **Model Router** – instantly switch between Eco‑Router (auto‑select), Claude‑Opus, Claude‑Sonnet, Llama‑70B, Llama‑8B/Flash, etc.
- **Premium UI** – video background, glass‑cards, responsive bento‑grid layout, Lucide icons, custom gradients.
- **SEO‑Optimised** – descriptive `<title>`, meta description, keywords, and proper heading hierarchy.
- **Zero‑Backend** – pure HTML/CSS/JS; the only external call is the public Carbon Intensity API.

---

## 🛠️ Tech Stack
- **HTML5** – semantic structure, ARIA‑labelled UI.
- **Vanilla CSS** – custom design system, no Tailwind.
- **JavaScript (ES6+)** – state management, API fetching, DOM updates.
- **Lucide Icons CDN** – lightweight SVG icons.
- **Python SimpleHTTPServer** – static file server for local development.

---

## 🚀 Getting Started Locally
```bash
# Clone the repo
git clone https://github.com/DavidAkerele/Eco-Pulse.git
cd Eco-Pulse

# (Optional) Create a virtual env for the simple server
python3 -m venv .env && source .env/bin/activate

# Run the static server (default port 8080)
python3 -m http.server 8080

# Open in a browser
open http://localhost:8080
```
The app will load with the default region (Manchester) and a fresh carbon‑budget.

---

## 📊 How the Carbon Calculations Work
1. **Live Grid Intensity** – fetched from `https://api.carbonintensity.org.uk/regional/regionid/{id}` (gCO₂/kWh).
2. **Average Daily Digital Footprint** – 200 g CO₂ (based on Carbon Trust/IEA 2023 data).
3. **Your AI Audit Emissions** – accumulated in `budgetState.used` (grams CO₂) each time you run a prompt.
4. **Comparison Visuals** – percentage bar, per‑capita electricity context, and regional fuel‑mix breakdown.

---

## 📁 Repository Structure
```
Eco-Pulse/
├─ index.html          # Main markup, meta tags, UI layout
├─ styles.css          # Design system, glass‑morphism, animations
├─ app.js              # Core logic, budget system, local impact module
├─ green_landscape_bg.png # Background video placeholder image
├─ README.md           # This file (enhanced)
└─ .git/               # Version control metadata
```

---

## 🤝 Contributing
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/awesome‑feature`).
3. Make your changes and ensure they pass linting (`npm run lint` – optional). 
4. Submit a Pull Request with a clear description.

All contributions must follow the existing design language (glass‑cards, gradients, and accessible colour contrast).

---

## 📜 License
This project is licensed under the **MIT License** – feel free to use, modify, and share.

---

## 📞 Contact
**David Akerele** – [GitHub](https://github.com/DavidAkerele) – [Twitter @davidakerele](https://twitter.com/davidakerele)

---

*Built with love for a greener AI future.*
