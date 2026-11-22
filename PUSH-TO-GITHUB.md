# Publish this portfolio to GitHub Pages (Windows PowerShell)

## Important: check the files before making the site public

This is a public portfolio. It displays the email address and phone number from the supplied CV, and includes the CV and three project-report PDFs. Some project reports contain AWS account/instance/IP details. Review those files first. If you want to redact or remove anything, do it **before pushing**, since Git history can retain removed files.

The desired address is **https://luumost.github.io/**. The repository must be named **`LuuMost.github.io`**. The existing `lutendo.netlify.app` address remains a Netlify address and cannot be assigned to GitHub Pages.

## 1. Download and extract the source ZIP

Download `luumost.github.io.zip`, then right-click it in Downloads → **Extract All**. The extracted files may be inside a nested `luumost.github.io` folder.

## 2. Go to the project root

```powershell
cd "$env:USERPROFILE\Downloads\luumost.github.io\luumost.github.io"
dir
```

Before continuing, confirm `dir` shows `index.html`, `assets`, `.github`, and `README.md`. **Do not run Git commands from `C:\Users\Mudau` or another parent folder.**

## 3. Initialize and commit the website

The ZIP intentionally excludes `.git`:

```powershell
git init
git branch -M main
git add -A
git status --short
git commit -m "Create Richard Mudau portfolio for GitHub Pages"
```

Check `git status --short` before committing. It should list only this website's files.

## 4. Create the public user-site repo and push

Your GitHub CLI should already be authenticated. Create the repo and push:

```powershell
gh repo create LuuMost.github.io --public --source=. --remote=origin --push
```

If GitHub says the repository name already exists, **do not create another repo**. Connect to the existing one and push:

```powershell
git remote add origin https://github.com/LuuMost/LuuMost.github.io.git
git push -u origin main
```

## 5. Enable Pages and verify

1. Open `https://github.com/LuuMost/LuuMost.github.io`.
2. Go to **Settings → Pages** and set the deployment source to **GitHub Actions**.
3. Open **Actions** and wait for **Deploy portfolio to GitHub Pages** to finish successfully.
4. Visit **https://luumost.github.io/**.

To publish changes later, edit the files, then run `git add -A`, `git commit -m "Update portfolio"`, and `git push` from this project folder. Do not paste access tokens into chat or commands.
