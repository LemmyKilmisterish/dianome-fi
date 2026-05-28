# Dianome Oy website

Static website for Dianome Oy, prepared for GitHub Pages with the custom domain `dianome.fi`.

## Local preview

Open `index.html` directly in a browser, or run a simple local server:

```bash
python3 -m http.server 8080
```

## Publishing

The repository is ready for GitHub Pages. Authenticate GitHub CLI with the `lemmy1975@gmail.com` GitHub account first:

```bash
gh auth login -h github.com
```

Then create and push the repository:

```bash
git add .
git commit -m "Launch Dianome website"
gh repo create dianome-fi --public --source=. --remote=origin --push
```

Enable GitHub Pages from the repository settings, publishing from the `main` branch root. The included `CNAME` file sets the custom domain to `dianome.fi`; DNS still needs to point the domain to GitHub Pages.
