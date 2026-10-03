# Sundior Legal & Support Portal

Official legal, privacy, terms, and support documentation for **Sundior Lead Management CRM**, developed and maintained by **Sundior Technologies Private Limited**.

This repository is designed to be hosted as a completely static website via **GitHub Pages** with zero build steps, frameworks, or server-side dependencies. It provides permanent canonical URLs suitable for linking from:
* Google Play Console (Store Listing & Data Safety requirements)
* The Sundior mobile application
* The Sundior official website

---

## Folder Structure

```text
sundior-legal/
│
├── index.html                     # Portal landing page
│
├── privacy-policy/
│   └── index.html                 # Privacy Policy page
│
├── terms-and-conditions/
│   └── index.html                 # Terms & Conditions page
│
├── delete-account/
│   └── index.html                 # Google Play account deletion instructions
│
├── contact/
│   └── index.html                 # Contact & support information
│
├── assets/
│   ├── css/
│   │   └── style.css              # Shared central stylesheet
│   │
│   ├── images/
│   │   └── .gitkeep               # Directory for logos, screenshots, etc.
│   │
│   └── icons/
│       └── .gitkeep               # Directory for custom icons / favicons
│
├── README.md                      # Project documentation
└── .gitignore                     # Git ignore rules for static projects
```

---

## Page URLs

Using directory-based `index.html` files produces clean URLs on GitHub Pages:

| Page | URL Path | Description |
| :--- | :--- | :--- |
| **Home** | `/` | Portal overview and links to all documents |
| **Privacy Policy** | `/privacy-policy/` | Privacy Policy and data handling disclosures |
| **Terms & Conditions** | `/terms-and-conditions/` | Terms of service and usage guidelines |
| **Account Deletion** | `/delete-account/` | Account & user data deletion instructions |
| **Contact** | `/contact/` | Official support channels and inquiries |

All navigation links and asset references use relative paths (e.g., `../assets/css/style.css` from subdirectories and `assets/css/style.css` from the root). This ensures the site resolves correctly regardless of whether it is hosted at a domain root or a GitHub Pages subpath (e.g., `https://<USERNAME>.github.io/sundior-legal/`).

---

## Legal Content Notice

> **Important:** This repository is currently initialized with foundational structure and layout placeholders (`<!-- CONTENT WILL BE PROVIDED LATER -->`). Actual legal terms, policies, retention periods, compliance statements, account deletion procedures, and contact details will be added separately.

---

## Where to Add Future Assets & Content

* **Legal Content**: Replace the `<!-- CONTENT WILL BE PROVIDED LATER -->` placeholder blocks inside the corresponding `index.html` file in each page directory (`privacy-policy/`, `terms-and-conditions/`, `delete-account/`, `contact/`). The shared stylesheet already includes standard typography styling for headings (`h2`, `h3`), paragraphs, bulleted/numbered lists, tables, and blockquotes.
* **Custom Styling**: Add or modify rules in `assets/css/style.css`.
* **Images & Logos**: Place image assets in `assets/images/`.
* **Icons & Favicons**: Place icon files in `assets/icons/`.

---

## Running Locally

Because this is a pure static website with no build step, you can preview it locally using any static web server:

### Option 1: Python HTTP Server
```bash
# In the repository root:
python -m http.server 8000
```
Then navigate to: `http://localhost:8000/`

### Option 2: Node `serve` or `http-server`
```bash
npx serve .
```

### Option 3: VS Code Live Server
Right-click `index.html` in VS Code and select **"Open with Live Server"**.

---

## GitHub Pages Deployment

To publish this website using GitHub Pages:

1. Push the repository to GitHub on the `main` branch.
2. In the GitHub repository, navigate to **Settings** > **Pages**.
3. Under **Build and deployment**:
   * **Source**: `Deploy from a branch`
   * **Branch**: `main`
   * **Folder**: `/ (root)`
4. Click **Save**.
5. Once deployment completes, your site will be live at:
   ```text
   https://<USERNAME>.github.io/<REPOSITORY-NAME>/
   ```
