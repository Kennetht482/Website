# GitHub Pages Image Gallery

This repository contains a simple static image gallery you can host with GitHub Pages.

How it works
- Put image files in the `images/` folder.
- Add an entry to `images.json` describing each image.
- The `index.html` reads `images.json` and renders a gallery.

Manifest (images.json) format
Example:
```json
[
  {
    "file": "images/example.jpg",
    "title": "My Example",
    "caption": "An example image",
    "alt": "Alt text for accessibility"
  }
]
```

Quick start (manual)
1. Create a new repository on GitHub:
   - For a user site: name it `your-username.github.io`
   - For a project site: any name, then enable Pages from the repo settings (choose branch `main` or `gh-pages`)
2. Add these files (index.html, assets/, images.json, README.md).
3. Upload image files:
   - Use the GitHub web UI: go to the repo → Add file → Upload files → upload into `/images/` folder.
4. Edit `images.json` (via web UI or locally) to add objects that point to the uploaded images.
5. Wait a minute for GitHub Pages to publish, then open:
   - https://your-username.github.io (user site) or
   - https://your-username.github.io/your-repo (project site)

Automated upload (optional)
A small helper script `upload.sh` is provided to push files to the repo using the GitHub API. This requires a Personal Access Token (PAT) with repo scope and is intended to be run locally (do not expose tokens in the browser).

Security note
- Do not store access tokens in the repo.
- If you want a web-based image uploader, you must implement server-side storage or use a trusted image host; GitHub Pages is static only.

If you'd like, I can:
- Add an optional upload script for local use with a PAT, or
- Make a GitHub Action that automatically updates images.json from a directory, or
- Convert this to a Jekyll site that uses data files and templates.

Tell me which option you prefer and I will produce the script or Action next.