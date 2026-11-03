# Project Vedhak — Wi-Fi CSI Sensing

A responsive, projector-friendly research presentation website for the ESP32-based Wi-Fi Channel State Information (CSI) acquisition and exploratory visualization prototype.

## Features

- Black-and-white editorial design, responsive for desktop and mobile.
- Presentation mode: click **Present** or press `P`; use arrow keys to move between sections and `Esc` to exit.
- Interactive signal explainer for motion index, packet correlation, RSSI, heatmap, fluctuation spectrum and amplitude profile.
- Hardware photo gallery with click-to-expand images.
- Research evidence summary based on the supplied project report and paper.
- Working PDF links for the pitch deck, research paper and project report.
- IRIS 27 abstract-submission receipt image.
- No framework, build step, package installation or API key required.

## Run locally

Open `index.html` in a browser, or run a local static server from this directory:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deploy with GitHub Pages

1. Create a new GitHub repository, for example `project-vedhak`.
2. Upload the contents of this folder to the repository root (keep `assets/` and `docs/` folders).
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/ (root)`, then save.
5. Wait for the Pages deployment and open the generated URL.

### Push using Git

```bash
git init
git add .
git commit -m "Add Project Vedhak research website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/project-vedhak.git
git push -u origin main
```

## Repository structure

```text
project-vedhak/
├── index.html
├── styles.css
├── script.js
├── README.md
├── assets/
│   ├── csi-dashboard.png
│   ├── hardware-overview.png
│   ├── esp32-boards.png
│   ├── prototype-setup.png
│   └── iris27-submission.jpg
└── docs/
    ├── presentation.pdf
    ├── research-paper.pdf
    └── project-report.pdf
```

## Research integrity note

The site deliberately describes the work as an **acquisition and exploratory visualization prototype**. The supplied paper/report describe 16,660 parsed `CSI_DATA` records, 25 fields per record, RSSI from −73 to −29 dBm (approximately −42.45 dBm mean), a reported CSI length of 256, and 256 integers in the final field. The source materials state that the available log has no verified human-presence labels or environment identifiers, and the dashboard screenshot indicates calibration is required and receiver data are unavailable in that displayed state. Accordingly, the site does not claim a trained/validated detector, detection accuracy, through-wall performance or environmental robustness.

The pitch deck supplied as a PDF is included as-is. Replace `docs/presentation.pdf` if you later provide an updated slide deck.


## Latest visual update
- Animated dark opening scene showing TX → human interaction → dual RX nodes, with moving signal pulses.
- Replaced the former research overview with a concise explanation of propagation, interaction and interpretation.
- Expanded the next-experiments section into a three-phase equipment roadmap.
- Added S. Zigneswar as a co-author from VIT-AP University.
- Respects `prefers-reduced-motion` for accessibility.

## Run locally
Open `index.html` in a browser, or serve this folder with any static web server. All project PDFs and image assets are stored locally in `docs/` and `assets/`.


## November 2026 redesign
- Presentation flow: Introduction → Challenge → Architecture → Mathematics → Results → Future Scope → .
- Added protocol/frequency details based on the supplied report. Exact PHY mode, bandwidth, packet transport and CSI array mapping are explicitly marked as requiring firmware confirmation.
- Added equations for complex CSI, amplitude, phase, reference deviation, window mean and variance. Candidate processing is labelled as proposed, not completed.
- Expanded future equipment for multi-node CSI, calibrated RF capture, mmWave reference sensing and research-grade SDR.
- Added comparisons with Origin Wireless, Aqara FP2, Xandar Kardian and Vayyar using public technology descriptions.
- Removed the IRIS 27 abstract-submission screenshot and conference abstract section.
