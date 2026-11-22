# Richard Lutendo Mudau — Portfolio

A lightweight personal portfolio for **Richard Lutendo Mudau**, an aspiring professional software developer based in Pretoria, South Africa. Built with semantic HTML and CSS; no framework, external fonts, CDN scripts, or build step is required.

## Live site

After deployment, the GitHub Pages address is:

**https://luumost.github.io/**

The GitHub Pages user-site repository must be named `LuuMost.github.io`. The old `lutendo.netlify.app` address is owned/managed by Netlify and cannot be assigned to GitHub Pages. It can remain live separately.

## Publish with GitHub Pages

1. Create a **public** GitHub repository named `LuuMost.github.io`.
2. Push the contents of this repository to its `main` branch.
3. On GitHub, open **Settings → Pages** and choose **GitHub Actions** as the build and deployment source if it is not already selected.
4. Open **Actions** and wait for **Deploy portfolio to GitHub Pages** to complete successfully.
5. Visit `https://luumost.github.io/`. The first deployment may take a few minutes.

The included workflow deploys the repository contents as a static site. Edit `index.html` to update page content. Replace the CV or project PDFs under `assets/` when those documents change, then push to `main` to redeploy.

## Public information check

GitHub Pages is public. This site intentionally displays the contact details supplied for the portfolio and links to the supplied CV and project reports. Some project PDFs/screenshots include AWS account, instance, or IP details. Review the public files before publishing; if you remove or redact anything, do so **before the first public push**, because removing a file later does not erase it from Git history.

## Technology

- HTML5 and CSS3
- GitHub Actions + GitHub Pages
- Responsive layout, accessible navigation, reduced-motion support
- Local PDFs; no external runtime dependencies
