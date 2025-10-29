# Deploy to GitHub Pages

Below are two simple ways to deploy this static site using GitHub Pages.

## Option A: User/Org site (recommended if you want username.github.io)
1. Create a new public repo named `<your-username>.github.io`.
2. Move the contents of this `portfolio` folder into the repo root (so `index.html` is at the root).
3. Commit and push.
4. Pages will auto-deploy from the `main` branch root. Visit `https://<your-username>.github.io` after 1–3 minutes.

## Option B: Project site (keep your current repo name)
1. In your current repo, move the `portfolio` folder contents into a new folder named `docs` (GitHub Pages supports root or `/docs`).
   - After moving: `docs/index.html`, `docs/styles.css`, `.nojekyll`.
2. Commit and push to `main`.
3. In GitHub → Settings → Pages:
   - Source: `Deploy from a branch`
   - Branch: `main`  Folder: `/docs`
4. Save. Your site will be at `https://<your-username>.github.io/<repo-name>/` in 1–3 minutes.

## Custom domain (optional)
- Add your domain in GitHub → Settings → Pages → Custom domain.
- Create a `CNAME` DNS record pointing to `<your-username>.github.io`.
- Enable "Enforce HTTPS" once the certificate is ready.

## Quick Git commands
```bash
# if creating a new repo
git init
git add .
git commit -m "Add ML portfolio"
git branch -M main
git remote add origin git@github.com:<your-username>/<repo-or-username>.github.io.git
git push -u origin main
```

## Notes
- The site uses Google Fonts (EB Garamond); it works out-of-the-box on GitHub Pages.
- The `.nojekyll` file prevents Jekyll from processing the site.
