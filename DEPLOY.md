# Deploy to Railway (or any Node host)

## Quick setup

1. **Create a GitHub repo**
   - Go to github.com → New repository
   - Name it e.g. `btc-short-straddle-dashboard`
   - Make it public or private

2. **Upload these files**
   Upload the entire folder contents:
   - `index.html`
   - `server.js`
   - `package.json`
   - `README.md`

3. **Deploy on Railway**
   - Go to [railway.app](https://railway.app)
   - Sign in with GitHub
   - New Project → Deploy from GitHub repo
   - Select the repo
   - Railway auto-detects Node and runs `npm start`
   - It will give you a public URL

## Alternative: GitHub Pages (free, pure static)
- Push the files to a GitHub repo
- Settings → Pages → Deploy from branch (main) → / (root)
- Your site will be at `https://yourusername.github.io/repo-name/`

The dashboard is a single HTML file that talks directly to Deribit, so either method works.
The Node server is only needed if you want a proper backend host like Railway.

## Environment
No API keys or secrets required. Everything is public Deribit data computed in the browser.
