# MyDigitalMuse

A responsive website for MyDigitalMuse, automatically deployed to [Hostinger](https://www.hostinger.com) via GitHub Actions on every push to `main`.

---

## 📁 Project Structure

```
.
├── index.html          # Main HTML page
├── css/
│   └── style.css       # Stylesheet
├── js/
│   └── main.js         # Client-side JavaScript
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions deployment workflow
```

---

## 🚀 Deployment to Hostinger

The site is deployed automatically through a GitHub Actions workflow (`deploy.yml`) that uses FTP to upload files to Hostinger whenever changes are pushed to the `main` branch.

### Required GitHub Secrets

Before deployment can succeed, add the following secrets to your repository under **Settings → Secrets and variables → Actions**:

| Secret name       | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| `FTP_SERVER`      | Your Hostinger FTP hostname (e.g. `ftp.yourdomain.com`)                     |
| `FTP_USERNAME`    | Your Hostinger FTP username                                                 |
| `FTP_PASSWORD`    | Your Hostinger FTP password                                                 |
| `FTP_SERVER_DIR`  | Remote directory on the server (e.g. `public_html/` or `domains/yourdomain.com/public_html/`) |

### Finding FTP credentials on Hostinger

1. Log in to [hPanel](https://hpanel.hostinger.com).
2. Navigate to **Files → FTP Accounts**.
3. Use the credentials shown there (or create a new FTP account).

---

## 🛠 Local Development

No build step is required. Simply open `index.html` in your browser, or serve it with any static file server:

```bash
# Python 3
python -m http.server 8080

# Node.js (npx)
npx serve .
```

---

## 📄 License

© MyDigitalMuse. All rights reserved.

