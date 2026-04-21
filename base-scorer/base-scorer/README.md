# Base Wallet Scorer

On-chain activity scorer for Base network. Works as a website and Farcaster Mini App.

---

## Deploy in 5 steps

### 1. Get a BaseScan API Key (free)
- Go to https://basescan.org/register and create an account
- Navigate to https://basescan.org/myapikey
- Create a new API key (free tier is fine)
- Open `index.html` and replace `YOUR_BASESCAN_API_KEY` with your key

### 2. Deploy to Vercel
**Option A — Drag & drop (easiest):**
- Go to https://vercel.com/new
- Drag the entire `base-scorer` folder into the upload area
- Click Deploy — done in ~30 seconds

**Option B — GitHub:**
- Push this folder to a GitHub repo
- Connect the repo on https://vercel.com/new
- Click Deploy

### 3. Update your domain
After deploying, Vercel gives you a URL like `base-scorer-abc.vercel.app`.
Replace `YOUR_DOMAIN` in these files with your real URL:
- `index.html` (3 places in the `<head>` meta tags)
- `.well-known/farcaster.json` (5 places)

### 4. Add an OG image (optional but recommended)
- Create a 1200×630px image named `og-image.png`
- Create a 200×200px icon named `icon.png`
- Place them in the root folder
- Redeploy

### 5. Register as a Farcaster Mini App
- Go to https://warpcast.com/~/developers/mini-apps
- Click "Add domain" and enter your Vercel URL
- Warpcast will verify your `.well-known/farcaster.json`
- Fill in the `accountAssociation` fields with the values Warpcast gives you
- Redeploy once more

---

## File structure
```
base-scorer/
├── index.html              ← Main app (website + mini app)
├── vercel.json             ← Vercel config
├── .well-known/
│   └── farcaster.json      ← Farcaster Mini App manifest
├── og-image.png            ← Add this yourself (1200×630)
├── icon.png                ← Add this yourself (200×200)
└── README.md
```

---

## Features
- Wallet activity scoring (0–100) using BaseScan API
- 6 verdict tiers from "Base Ghost" to "King of Base"
- Funny quotes per tier (randomized each search)
- BASE MODE — fireworks, rockets, exploding BASE letters
- Mobile-first, works inside Farcaster Mini App frame
- Dark theme with Base blue aesthetic
