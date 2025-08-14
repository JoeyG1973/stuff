# GitHub Pages — User Site (joeyg1973.github.io)

This repository serves files at `https://joeyg1973.github.io`. For large/binary files, use GitHub Releases for reliable downloads.

## Direct files (small)
- `https://joeyg1973.github.io/path/to/file.ext`
- Prompt save from a page:
  ```html
  <a href="/path/to/file.ext" download>Download file</a>
  ```
- Force download:
  - `https://joeyg1973.github.io/download.html?file=path/to/file.ext&name=MyFile.ext`

## Large/binary files via Releases
- Browse downloads: `https://joeyg1973.github.io/downloads.html`
- Direct asset links (auto-download):
  - `https://github.com/JoeyG1973/joeyg1973.github.io/releases/download/<tag>/<asset-name>`
- How to publish:
  1. Put files in `release-assets/`.
  2. Commit and push.
  3. Create a tag like `v1.0.0` and push it. The workflow creates a Release and uploads files from `release-assets/**`.
     ```bash
     git tag -a v1.0.0 -m "Initial release"
     git push origin v1.0.0
     ```
  4. Visit `downloads.html` or the Release page to get links.

Notes:
- GitHub Pages does not support Git LFS; pointer files would be served instead of content. Use Releases for large assets.
- Release assets typically serve with Content-Disposition=attachment, so browsers download them directly.
- Unauthenticated GitHub API calls on `downloads.html` are rate-limited (60/hour per IP).

## Setup (Pages)
1. Enable Pages: Repo → Settings → Pages → Build and deployment → Source: **Deploy from a branch** → Branch: **main**, Folder: **/** (root).
2. Wait 1–2 minutes, then visit:
   - Site: `https://joeyg1973.github.io/`
   - Downloads: `https://joeyg1973.github.io/downloads.html`