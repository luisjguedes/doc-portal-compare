# Doc Portal Launcher

A lightweight, browser-based tool to quickly **open and compare documentation environments** (PROD, STAGING, UAT) using the **same page path**.

Designed to remove friction when validating documentation changes across environments—without iframe issues, cookie blockers, or CSP limitations.

---

## What this tool does

### Check a single environment
Open one documentation environment for the exact page you’re working on.

- Opens in a reusable pop-up window  
- Uses the same path as the URL you paste  
- Ideal for fast verification  

### Compare environments side-by-side
Open two environments at once for direct comparison.

- Same page path in both environments  
- Two reusable pop-up windows  
- Best for spotting content, navigation, or UI differences  

---

## Why this approach

This tool intentionally avoids iframes.

Modern documentation portals rely on strict cookie policies, consent banners, and CSP/X-Frame-Options that break embedded views. Using browser pop-ups ensures:

- Full scrolling and interaction  
- Cookie consent works as expected  
- Authentication and sessions are preserved  
- No maintenance when portal security settings change  

---

## How to use

1. Open the tool  
   https://luisjguedes.github.io/doc-portal-compare

2. Paste a full documentation URL  
   Example:
   ```
   https://docs.reltio.com/en/products/agentflow/...
   ```

3. Choose a mode  
   - **Check an environment** → opens a single environment  
   - **Compare environments** → opens two environments side-by-side  

4. Click **Open**

---

## Supported environments

- **PROD**  
  https://docs.reltio.com/en

- **STAGING**  
  https://reltio-staging.portal.heretto.com/en  
  https://docstaging.reltio.com/en

- **UAT**  
  https://reltio-preview.portal.heretto.com/en

Environment mappings live directly in `index.html` and can be extended easily.

---

## One-time browser setup

This tool requires pop-ups.

When prompted, allow pop-ups for:
```
https://luisjguedes.github.io
```

Once allowed, no further setup is needed.

---

## Project structure

```
/
├─ index.html
├─ reltio_doc_banner.png
└─ README.md
```

- No build step  
- No dependencies  
- Runs entirely in the browser  
- Hosted via GitHub Pages  

---

## Known limitations

- Window positioning is best-effort and depends on browser and OS behavior  
- Some systems may stack windows instead of placing them side-by-side  
- OS window snapping always works as a fallback  

These are browser security constraints, not code issues.

---

## Why this is useful

- Faster documentation reviews  
- Safer pre-release validation  
- Easier collaboration between writers, PMs, QA, and support  
- No reliance on internal tooling or special permissions  

---

## License

MIT — free to use, adapt, and extend.
