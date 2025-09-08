# TrendDrop Monetizer

Automate trending topic drops, AI-powered content generation, affiliate monetization, and social alerts for growth hacking.  
This plugin streamlines the workflow from trend discovery to monetized publishing and contributor engagement.

---

## Features

- **Fetch Trending Topics:**  
  Scrapes breakout topics from Google Trends.

- **AI Content Generation:**  
  Gemini-powered scripts for fast, relevant content.

- **Monetization:**  
  Auto-inject affiliate links (e.g., NFL merch) into content.

- **One-Click Publishing:**  
  Deploy drops to Firebase Hosting.

- **Slack Alerts:**  
  Notify contributors with preview links.

- **Branded Social Assets:**  
  Auto-generated thumbnails & emoji-coded captions for viral social sharing.

- **Audit Logging:**  
  Compliance notes and fallback logger.

---

## Quick Start

1. **Clone & Install**
   ```sh
   git clone https://github.com/<your-org>/trenddrop-monetizer.git
   cd trenddrop-monetizer
   npm install
   ```

2. **Configure Environment**
   - Copy example env:  
     `cp config/env.example config/.env`
   - Fill in Gemini, Firebase, and Slack API keys.

3. **Run Workflow**
   ```sh
   npm run drop
   ```
   This will:
   - Fetch new trends
   - Generate content
   - Monetize with affiliate links
   - Publish to Firebase
   - Send Slack alert

---

## Directory Structure

```
trenddrop-monetizer/
├── config/
│   ├── env.example           # API keys & secrets (Gemini, Firebase, Slack)
│   └── topics.json           # Cached trending topics
├── scripts/
│   ├── fetchTrends.js        # Scrapes breakout topics from Google Trends
│   ├── generateContent.js    # Gemini-powered content scripter
│   ├── injectMonetization.js # Adds affiliate links (e.g. NFL merch)
│   └── publishDrop.js        # Deploys to Firebase Hosting
├── alerts/
│   └── slackNotify.js        # Sends Slack alert with preview link
├── assets/
│   ├── thumbnails/           # Auto-generated branded images
│   └── social-captions/      # Emoji-coded captions for contributors
├── docs/
│   ├── onboarding.md         # Contributor setup guide
│   └── audit-log.md          # Fallback logger & compliance notes
├── firebase.json             # Hosting config
├── .firebaserc               # Firebase project alias
├── README.md                 # Plugin overview & usage
└── package.json              # Dependencies & scripts
```

---

## Automation

- Unified workflow:  
  `npm run drop`
- Modular scripts for each step.
- Easily integrate with [GitHub Actions](https://docs.github.com/en/actions) or cron jobs for scheduled drops.

---

## Contributing

- See `docs/onboarding.md` for setup and workflow.
- Add thumbnails, suggest captions, or extend scripts.
- Log major changes in `docs/audit-log.md`.

---

## License

MIT
