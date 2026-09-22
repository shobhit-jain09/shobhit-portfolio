# Shobhit Jain — Portfolio

A single-page portfolio site (plain HTML/CSS/JS, no build step, no dependencies)
modeled on the layout/style of khadkechetan.github.io, populated with content
from `assets/Shobhit_Jain_Resume.pdf`.

- Dark theme with an animated particle-network hero, gradient headline,
  animated stat counters, categorized skill chips, and a timeline-style
  experience section pulled directly from the resume.
- 100% static — free to host forever on GitHub Pages.

## Preview locally

No install needed — just open `index.html` in a browser. Or, for a proper
local server (recommended, avoids any relative-path quirks):

```bash
npx serve .
```

## Deploy to GitHub Pages (free)

### Option A — GitHub's web UI (no git command line needed)

1. Go to [github.com/new](https://github.com/new), create a new repository
   (e.g. `shobhit-portfolio`). Keep it **Public** (GitHub Pages' free tier
   requires public repos unless you're on GitHub Pro/Team).
2. On the new repo's page, click **uploading an existing file**.
3. Drag in `index.html`, `style.css`, `script.js`, and the `assets` folder
   (with `Shobhit_Jain_Resume.pdf` inside it). Commit the upload.
4. Go to **Settings → Pages** (left sidebar).
5. Under **Build and deployment → Source**, choose **Deploy from a branch**.
6. Under **Branch**, choose `main` and folder `/ (root)`, then **Save**.
7. Wait ~1 minute, refresh the page — GitHub shows your live URL:
   `https://<your-github-username>.github.io/shobhit-portfolio/`

### Option B — git command line

```bash
cd shobhit-portfolio
git init
git add -A
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/<your-github-username>/shobhit-portfolio.git
git push -u origin main
```

Then repeat steps 4–7 from Option A to turn on Pages for the repo.

### Custom domain (optional, still free)

If you own a domain, add a `CNAME` file at the project root containing just
your domain (e.g. `shobhitjain.dev`), then point your domain's DNS at GitHub
Pages per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
GitHub Pages itself stays free — you only pay your domain registrar.

## Updating content later

- Resume/experience content lives directly in `index.html` (search for the
  section you want, e.g. `id="experience"`).
- Colors and theme tokens are all at the top of `style.css` under `:root`.
- To swap the resume PDF, replace `assets/Shobhit_Jain_Resume.pdf` and keep
  the same filename (or update the two `href` references in `index.html`).
- After any edit, just commit and push — GitHub Pages redeploys automatically
  within about a minute.

## Privacy note

This site publishes your email and phone number publicly once deployed
(same as the resume). If you'd rather not expose your phone number on the
public web, remove the `tel:` button in the Contact section of `index.html`
before pushing live.
