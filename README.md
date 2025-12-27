# Doc Portal Compare (Side-by-side)

A tiny GitHub Pages tool to compare two documentation portal environments (e.g., PROD vs STAGING, UAT vs PROD) **side-by-side** using the same path.

## Features
- Paste any full URL from one environment → the tool keeps the path and loads it in two environments
- Choose **Left** and **Right** environments
- Swap sides
- Copy a shareable link (stores path + selected envs in query params)
- Open both URLs in new tabs (fallback if iframe embedding is blocked)

## Quick start (local)
Open `index.html` in your browser.

## Deploy on GitHub Pages
1. Create a new repo (e.g., `doc-portal-compare`)
2. Add `index.html` (and this README) to the repo root
3. GitHub → **Settings** → **Pages**
4. Set **Build and deployment** → **Deploy from a branch**
5. Select branch: `main`, folder: `/root`
6. Your URL becomes: `https://<username>.github.io/<repo>/`

## Configure environments
Edit the `envMap` and `envPatterns` objects inside `index.html`.

> Note: If your portal blocks iframes via `X-Frame-Options` or CSP `frame-ancestors`, the panes may remain blank.
Use **Open tabs** instead.
