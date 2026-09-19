# Ashesh Jain

Personal website for Ashesh Jain, co-founder and CEO of Coram.

## Local preview

This is a static HTML/CSS site with no build step or package dependencies.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000. The landing page, including the full publication list, is `index.html`; the publication and talk archive is `research.html`, and both use `css/site.css`. Existing project pages and research assets remain at their original paths.

## Production deployment

Production: https://asheshjain399.github.io/

GitHub Pages publishes the **root directory of `gh-pages`** using its standard Pages build. The repository default branch is **`master`**, which does not deploy by itself. No custom domain is currently configured in Pages.

After testing and committing a change on `master`, update both branches to the tested commit:

```sh
git fetch origin
git push --atomic origin HEAD:master HEAD:gh-pages
```

This must be a fast-forward update. If either remote branch has advanced, integrate and test those changes before pushing; do not force-push.

Check deployment configuration and the latest build:

```sh
gh api repos/asheshjain399/asheshjain399.github.io/pages
gh api repos/asheshjain399/asheshjain399.github.io/pages/builds/latest
```

Wait for the matching commit to report `built`, then verify the public page, stylesheet, portrait, and research archive. GitHub's CDN may take a few minutes to update.

## Content and assets

- Funding: $66 million total, supplied by Ashesh for this redesign; selected investors are 8VC and Battery Ventures.
- Coram platform description: https://www.coram.ai/
- Profile portrait: user-supplied 800 × 800 PNG, stored as `img/ashesh-portrait.png` and displayed at 220px on desktop and 144px on mobile.
- Prior publications, talks, PDFs, slides, and project assets remain available. The research archive preserves historical venue labels and links.

The legacy Bootstrap theme remains in the repository for existing project pages. Its original attribution and license are retained in `LICENSE` and the theme source files.
