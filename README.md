# ⚡ PromptForge

**lazy input → precise output**

Transform vague coding task descriptions into precise, professional prompts optimized for Cursor, Claude, ChatGPT, v0, and Bolt.

---

## Deploy to Railway (via GitHub)

### 1. Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/promptforge.git
git push -u origin main
```

### 2. Deploy on Railway

1. Go to [railway.app](https://railway.app) and sign in
2. Click **New Project → Deploy from GitHub repo**
3. Select your `promptforge` repository
4. Railway auto-detects Node.js and uses `railway.toml` config
5. Click **Deploy** — it will be live in ~60 seconds

### 3. Set Environment Variables (optional)

PromptForge stores API keys in the **browser's localStorage** — no server-side env vars needed for the API key.

If you want to pre-configure anything server-side, add variables in:
Railway Dashboard → Your Project → Variables

---

## Local Development

```bash
npm install
npm start
# Open http://localhost:3000
```

---

## How It Works

- Single HTML file served by Express
- User enters their Anthropic API key once → stored in browser localStorage
- API calls go directly from the browser to `api.anthropic.com`
- No data touches the server after initial page load

---

## Stack

- **Frontend**: Vanilla HTML/CSS/JS (no framework)
- **Server**: Node.js + Express (serves static file)
- **AI**: Anthropic Claude API (`claude-sonnet-4-20250514`)
- **Hosting**: Railway
