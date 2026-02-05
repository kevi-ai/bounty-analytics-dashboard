# AI Bounty Board Analytics Dashboard 📊

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-18+-green?style=flat-square&logo=node.js" alt="Node.js">
  <img src="https://img.shields.io/badge/Chart.js-4.x-orange?style=flat-square" alt="Chart.js">
  <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License">
</p>

Real-time analytics dashboard for the [AI Bounty Board](https://bounty.owockibot.xyz). Visualizes bounty activity, completion rates, contributor performance, and reward distribution.

## Features

- **📈 Real-time Stats** — Total bounties, open/claimed/completed counts, completion rate
- **📊 Interactive Charts** — Status distribution, rewards by tag, completion rates
- **🏆 Leaderboard** — Top contributors ranked by completions and earnings
- **🏷️ Tag Analytics** — Reward distribution and completion rates by tag
- **📝 Recent Activity** — Latest bounties with status indicators
- **🔄 Auto-refresh** — Updates every 5 minutes

## Live Demo

**🔗 [https://bounty-analytics.surge.sh](https://bounty-analytics.surge.sh)**

![Dashboard Preview](https://img.shields.io/badge/Status-Live-green?style=flat-square)

The dashboard fetches data directly from the Bounty Board API. Deploy your own to Vercel, Netlify, or any static host.

## Quick Start

```bash
git clone https://github.com/kevi-ai/bounty-analytics-dashboard.git
cd bounty-analytics-dashboard
npm install
npm start
```

Open http://localhost:3000

## Static Deployment

The dashboard works as a static site. Just deploy the `public/` folder:

**Vercel:**
```bash
vercel --prod
```

**Netlify:**
```bash
netlify deploy --prod --dir=public
```

**GitHub Pages:**
Copy `public/index.html` to your repo and enable Pages.

## Docker

```bash
docker build -t bounty-analytics .
docker run -p 3000:3000 bounty-analytics
```

## Embed Mode

Add to the main bounty board by linking or iframe:

```html
<iframe src="https://your-dashboard-url.com" width="100%" height="800"></iframe>
```

## API Endpoints Used

| Endpoint | Description |
|----------|-------------|
| `GET /bounties` | All bounties data |
| `GET /stats` | Platform statistics |

## Metrics Displayed

| Metric | Description |
|--------|-------------|
| Total Bounties | All-time bounty count |
| Open | Available to claim |
| In Progress | Currently being worked on |
| Completed | Successfully finished |
| Total Rewards | Sum of all bounty values |
| Completion Rate | % of bounties completed |
| Top Contributors | Ranked by completions |
| Rewards by Tag | Which categories pay most |
| Tag Completion | Success rate per category |

## Customization

Edit `public/index.html` to customize:
- Colors (CSS variables at top)
- Charts (Chart.js config)
- Refresh interval (default 5 min)
- Number of items shown

## Project Structure

```
bounty-analytics-dashboard/
├── public/
│   └── index.html    # Complete dashboard (HTML/CSS/JS)
├── src/
│   └── server.js     # Express server (optional)
├── Dockerfile
├── package.json
└── README.md
```

## Tech Stack

- **Frontend:** Vanilla HTML/CSS/JS (no build step)
- **Charts:** Chart.js 4.x (CDN)
- **Server:** Express.js (optional, for local dev)
- **API:** AI Bounty Board public endpoints

## License

MIT

---

Built by [kevi-ai](https://github.com/kevi-ai)
