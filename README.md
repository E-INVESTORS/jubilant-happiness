# E-Investors — Automatic Disco (Static frontend)

A lightweight static frontend and demo for the E-Investors platform. This repository contains a simple static UI demonstrating investor and company dashboards, a small mock dataset, and a GitHub Actions workflow to deploy the site to GitHub Pages.

## Project status
Prototype / demo. The repository currently hosts a static HTML demo intended for showcasing basic UI concepts for investor/company dashboards and a chat widget. This README replaces the raw HTML content with a concise project overview and instructions.

## Features
- Minimal static frontend demonstrating:
  - Investor, company, and admin dashboard cards
  - Simple charts (Chart.js)
  - Mock lists of companies and masked investor names
  - Lightweight chat widget demo
- CI: GitHub Actions workflow to deploy to GitHub Pages

## Demo
If GitHub Pages is configured for this repository, the site will be available at:
https://<your-org-or-username>.github.io/automatic-disco

(Replace `<your-org-or-username>` with the repository owner.)

## Getting started (local preview)
To preview the static site locally:

1. If the HTML is in the repo root as `index.html`, run:
   - Python 3: `python3 -m http.server 8000`
   - Then open: `http://localhost:8000`

2. Or open the HTML file directly in your browser.

If you want a simple Node-based preview:
- Install http-server: `npm install -g http-server`
- Run: `http-server -c-1`
- Open the displayed local URL.

## Deployment
This repository uses a GitHub Actions workflow at `.github/workflows/static.yml` to deploy directly to GitHub Pages when changes are pushed to the `main` branch or when the workflow is triggered manually.

Notes:
- The workflow uploads the repository artifact and calls the official `actions/deploy-pages` action.
- If your site build produces files in a `build/` or `docs/` folder, update the workflow `path` to point at that folder instead of `.`.

## Suggested next steps (recommended)
- Move the current HTML demo into a dedicated `docs/` or `public/` directory (e.g., `docs/index.html`) so Pages can serve it from `docs/` if you prefer that layout.
- Extract inline scripts and styles into separate files (`assets/js/`, `assets/css/`) for maintainability.
- Replace mock data with API-driven data and add basic form validation and accessibility improvements.
- Add a basic unit-test or linting workflow for HTML/CSS/JS quality checks.

## Contributing
Contributions are welcome. Typical flow:
1. Fork the repository.
2. Create a feature branch: `git checkout -b feat/my-feature`
3. Make changes and open a pull request.

Please include details of the change and any steps required to run or test.

## License
Add a license file (e.g., `LICENSE`) to clarify the terms. If you want, I can add an MIT or other license for you.

## Contact
For questions or help improving the UI, feel free to open an issue or request specific updates — for example: converting the demo into a production-ready static site, extracting assets, or enabling a staged build step.
