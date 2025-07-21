# Digital Async Transparency – Company Website

This repository contains the source code for the public website of **Digital Async Transparency**.

The site is fully static (HTML and CSS), with no dependencies or build steps. It is automatically deployed to a remote web host using GitHub Actions and FTP.

---

## 📂 Project Structure

```text

homepage/
├── index.html # Main homepage
├── css/
│    └── style.css # Custom styling
├── images/
│     ├── kostymmorgan_small.jpg # Founder photo
│     └── digitalAsyncTransparency_logo_blue_transparent_background.svg # Company logo
└── .github/
       └── workflows/
               └── deploy.yml # GitHub Actions deployment workflow

```

---

## 🚀 Deployment

Deployment is handled automatically via GitHub Actions whenever changes are pushed to the `main` branch.

### 🔐 Required GitHub Secrets

To enable deployment, set the following secrets in the repository:

| Secret Name       | Description                        |
|-------------------|------------------------------------|
| `FTP_HOST`        | FTP server hostname or IP address  |
| `FTP_USERNAME`    | FTP login username                 |
| `FTP_PASSWORD`    | FTP login password                 |
| `FTP_TARGET_DIR`  | Target path on the server (e.g. `/public_html/`) |

---

## 💻 Local Development

No build tools are required. You can preview the site locally by simply opening `index.html` in a browser.

Alternatively, you can use a local static server:

```bash
npx serve .
