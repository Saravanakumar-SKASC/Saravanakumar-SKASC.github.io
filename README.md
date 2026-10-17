# Portfolio · Saravanakumar Nagalingam

A one-page, recruiter-friendly portfolio. Plain HTML, CSS and a few lines of JavaScript: no frameworks, no build step, nothing to install. It is free to host.

```
index.html                         ← all content lives here
assets/css/styles.css              ← colours and layout (change --accent to re-theme)
assets/js/main.js                  ← theme toggle + active nav link
assets/Saravanakumar_Nagalingam_CV.pdf   ← the CV behind every "Download CV" button
assets/img/favicon.svg, og-image.png     ← browser tab icon + LinkedIn/Slack link preview
robots.txt, sitemap.xml            ← help Google index the site
```

## Preview locally

Double-click `index.html`, or run a tiny server:

```bash
python3 -m http.server 8000      # then open http://localhost:8000
```

## Publish free on GitHub Pages (about 5 minutes)

1. On GitHub, create a **public** repository named exactly **`Saravanakumar-SKASC.github.io`**.
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Portfolio"
   git branch -M main
   git remote add origin https://github.com/Saravanakumar-SKASC/Saravanakumar-SKASC.github.io.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source: Deploy from a branch → `main` / root → Save**.
4. After a minute or two the site is live at **https://saravanakumar-skasc.github.io/**.

Every later `git push` updates the live site automatically.

**Other free hosts** (if you prefer): Netlify (drag the folder onto app.netlify.com/drop), Vercel or Cloudflare Pages. If the URL changes, update it in `index.html` (`canonical`, `og:url`, `og:image`, JSON-LD), `robots.txt` and `sitemap.xml`.

**Custom domain (optional, ~€10/year):** buy e.g. `saravanakumar.dev`, add it under Settings → Pages → Custom domain, and point the DNS at GitHub as shown there.

## After it's live

- Put the link in your **LinkedIn** (Contact info → Website, and the Featured section), your **CV header**, your **GitHub profile** and your email signature.
- Paste the link into https://www.linkedin.com/post-inspector/ once, so LinkedIn picks up the preview image.
- Pin Document-Portal, Phishing_Website_Detection and Avatar-Reader on your GitHub profile so they match the site.

## Updating content

- **New project:** copy one `<article class="project">` block (featured) or one `<li class="mini">` block (smaller) in `index.html`.
- **New CV:** replace `assets/Saravanakumar_Nagalingam_CV.pdf`, keeping the same file name.
- **Different target role:** edit the headline (`.role`), the pitch (`.pitch`), the About paragraphs, and the `<title>`/`description` meta tags.
