# UbuntuSec – Cybersecurity Awareness Platform

> **NEMISA Discothon Hackathon Project**  
> **Challenge:** "Using available resources, create something to empower the youth in cybersecurity."  
> **Deliverable:** A web application that teaches core cybersecurity fundamentals, phishing defense, and actionable ways to protect communities.  
> **Author:** Bonga Manzini (UNISA BSc Informatics Student)  
> *"Umuntu ngumuntu ngabantu" — I am because we are.*

**UbuntuSec** is a South African cybersecurity awareness platform inspired by the Ubuntu philosophy. Built for the NEMISA Discothon, UbuntuSec empowers youth and communities across South Africa to recognise, respond to, and report cyber threats — together.

---

## Features

- **Interactive Dashboard** — Real-time national risk level, live stats on tutorials completed, estimated scam losses avoided, and mobile-targeting trends.
- **Interactive Tutorials** — Gamified, module-based learning across six core cybersecurity topics:
  - Phishing & Scams
  - Password Safety
  - Safe Browsing
  - Social Engineering
  - Ransomware & Malware
  - Mobile Security
- **Threat Map & Data** — Visual overview of active cyber threats across South African provinces and sectors.
- **Alerts & Notifications** — Live alerts on emerging scams (e.g. SMS banking fraud, fake EFT verification requests) targeting South African users.
- **Resources & Reporting** — Curated security resources and a streamlined incident-reporting flow.
- **Certifications & Pro Training** — Earn shareable digital certificates upon completing learning modules.
- **Admin & Security Logs** — Administrative view for monitoring platform activity and security events.
- **AI Cyber-Safety Agent** — Floating chat assistant that answers cybersecurity questions in a South African context, with voice input support.
- **Media Campaign Spotlight** — Short animated awareness campaigns (e.g. "Don't Click That Link!") targeting common local scams.
- **Fully Responsive** — Mobile-first design with a dedicated bottom navigation bar and a collapsible sidebar for desktop.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Markup | HTML5 |
| Styling | CSS3, [Tailwind CSS](https://tailwindcss.com/) (CDN) |
| Icons | [Lucide Icons](https://lucide.dev/) (CDN) |
| Scripting | Vanilla JavaScript (ES6+) |
| Analytics UI | [Recharts](https://recharts.org/) *(CybersecurityAwarenessPlatform prototype)* |
| Component Prototype | React + Vite *(CybersecurityAwarenessPlatform folder)* |
| Data Profiling | Python / Streamlit *(streamlit_files/)* |

> The primary deployable platform is the standalone HTML/CSS/JS build (`firstworld.html` and `../index.html`). The `CybersecurityAwarenessPlatform/` folder contains an earlier React prototype.

---

## Project Structure

```
UbuntuSec/
├── firstworld.html                        # Main platform (full multi-page SPA)
├── CybersecurityAwarenessPlatform/        # React/Vite prototype
│   ├── src/
│   │   ├── components/
│   │   │   ├── figma/                     # Figma-exported component specs
│   │   │   └── ui/                        # Reusable UI components
│   │   ├── guidelines/                    # Design system guidelines
│   │   └── styles/                        # Global styles
│   └── streamlit_files/                   # Python data profiling scripts
│       ├── app.py
│       ├── app_plots.py
│       ├── app_profiler.py
│       ├── app_profiler_menus.py
│       └── run_streamlit.py
└── README.md
```

The parent `NEMISA/index.html` serves as the **Cyber-Safe ZA** landing page and entry point to the full platform.

---

## Getting Started

### Option 1 — Open directly in a browser (zero setup)

```bash
# Clone or download the repository, then simply open:
open firstworld.html        # macOS
xdg-open firstworld.html    # Linux
start firstworld.html       # Windows
```

### Option 2 — Serve with any HTTP server

```bash
# Using Python (recommended for local dev)
python3 -m http.server 8080
# Then open http://localhost:8080/firstworld.html

# Using Node.js (npx)
npx serve .
# Then open http://localhost:3000/firstworld.html

# Using VS Code Live Server extension
# Right-click firstworld.html → "Open with Live Server"
```

> **No build step required.** Tailwind CSS and Lucide Icons are loaded from CDN. An internet connection is needed on first load.

### Option 3 — React prototype (CybersecurityAwarenessPlatform)

```bash
cd CybersecurityAwarenessPlatform
npm install
npm run dev
```

### Option 4 — Streamlit data profiler

```bash
cd CybersecurityAwarenessPlatform/streamlit_files
pip install streamlit pandas ydata-profiling
python run_streamlit.py
```

---

## Platform Pages

| Page | File / Route | Description |
|------|-------------|-------------|
| Home | `index.html` | Dashboard, stats, campaign spotlight |
| Full Platform | `firstworld.html` | Complete multi-view SPA |
| Tutorials | `#tutorials` view | Gamified cybersecurity modules |
| Threat Map | `#threat-map` view | SA province-level threat visualisation |
| Alerts | `#alerts` view | Live scam and threat notifications |
| Resources | `#resources` view | Guides, links, incident reporting |
| Certifications | `#certs` view | Digital certificates for completed modules |
| Admin Logs | `#admin-logs` view | Platform activity and security event logs |

---

## Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add: your feature description'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2025 NEMISA – National Electronic Media Institute of South Africa

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

*Built with Ubuntu spirit — because a safer internet for one South African is a safer internet for all.*
