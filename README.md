# Pavan Kotapati — Portfolio

A fast-loading, single-page portfolio highlighting Pavan Kotapati's work in AI-focused data engineering. The site is built with hand-crafted HTML, CSS, and a sprinkle of vanilla JavaScript for theme toggling, scroll spying, and smooth navigation.

## ✨ Features
- **Hero overview:** AI Data Engineer positioning with CTA buttons and badges for core skills.
- **Responsive layout:** CSS grid + media queries provide a fluid experience from mobile to desktop.
- **Interactive navigation:** Sticky header with active-section highlighting, smooth scrolling, and theme toggle with persistence.
- **Project deep dives:** Cards summarizing LLM-driven automation, real-time streaming, lineage discovery, and cost optimization initiatives.
- **Experience filters:** Quick pill filters to surface roles and projects by focus area.

## 📂 Project Structure
```
.
├── assets/                     # Static downloads exposed on the site
│   └── Pavan_Kotapati_Resume.pdf (add your latest resume here)
├── docs/                       # Supplemental project documentation
│   └── maintenance-guide.md
├── index.html                  # Portfolio landing page
├── LICENSE                     # MIT License
└── README.md                   # Project overview and usage
```

Additional guidance lives under `docs/`, while downloadable assets (resume, imagery) belong in `assets/`.

## 🚀 Getting Started
You only need a modern browser to preview the site locally.

1. Clone the repository:
   ```bash
   git clone https://github.com/kotapatipavan211195/kotapatipavan211195.github.io.git
   cd kotapatipavan211195.github.io
   ```
2. Open `index.html` directly in your browser:
   - macOS: `open index.html`
   - Windows: `start index.html`
   - Linux: `xdg-open index.html`

No build pipeline or bundler is required.

### Optional: Serve with Live Reload
For auto-refresh while editing, you can launch a lightweight HTTP server. Example using Python 3:
```bash
python3 -m http.server 8080
```
Visit <http://localhost:8080/index.html> and refresh to see your changes.

## 🛠️ Customization Tips
- **Branding:** Update colors and messages by editing the CSS variables defined in `index.html` under the `:root` selector.
- **Navigation:** Add or rearrange sections by updating the primary navigation inside the header and matching section IDs in the markup.
- **Projects & experience:** Modify the cards within the `#projects` and `#experience` sections to showcase new work.
- **Theme toggle:** The theme logic lives at the bottom of `index.html`. Extend it to support additional themes or analytics hooks.
- **Resume download:** Replace `assets/Pavan_Kotapati_Resume.pdf` with your latest résumé; the hero "Download Resume" button points to this exact path.

## 🧪 Testing & Validation
Because the site is static, the primary validation steps are manual:
- Load the page in light/dark mode to confirm theme switching.
- Scroll through sections to ensure navigation highlights correctly.
- Test buttons (LinkedIn, GitHub, Email, Resume) to ensure they open the correct targets.

Feel free to integrate a linting pass (e.g., `npm run lint` with stylelint/eslint) if you migrate to a build tool in the future.

## 🤝 Contributing
Contributions are welcome. Please fork the repository, make your changes, and open a pull request with a short description of the update. If you are changing the design significantly, include screenshots or short clips so reviewers can see the impact quickly.

## 📄 License
- **Code:** [MIT License](LICENSE)
- **Content (résumé PDF, written copy, images):** [CC BY-NC-ND 4.0](LICENSE-content)
