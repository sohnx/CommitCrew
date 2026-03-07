<div align="center">

```
 ██████╗ ██████╗ ██╗███╗   ██╗██████╗     ███████╗ ██████╗ ██╗   ██╗ █████╗ ██████╗ 
██╔════╝ ██╔══██╗██║████╗  ██║██╔══██╗    ██╔════╝██╔═══██╗██║   ██║██╔══██╗██╔══██╗
██║  ███╗██████╔╝██║██╔██╗ ██║██║  ██║    ███████╗██║   ██║██║   ██║███████║██║  ██║
██║   ██║██╔══██╗██║██║╚██╗██║██║  ██║    ╚════██║██║▄▄ ██║██║   ██║██╔══██║██║  ██║
╚██████╔╝██║  ██║██║██║ ╚████║██████╔╝    ███████║╚██████╔╝╚██████╔╝██║  ██║██████╔╝
 ╚═════╝ ╚═╝  ╚═╝╚═╝╚═╝  ╚═══╝╚═════╝     ╚══════╝ ╚══▀▀═╝  ╚═════╝ ╚═╝  ╚═╝╚═════╝ 
```

**Track · Compete · Dominate**

*A collaborative progress tracker built for BTech CSE squads — LeetCode streaks, project workspaces, and a shared blackboard. All in one file. No backend. No cost.*

---

[![Made with HTML](https://img.shields.io/badge/Made%20with-HTML%2FCSS%2FJS-orange?style=for-the-badge&logo=html5&logoColor=white)](.)
[![Powered by GitHub Gist](https://img.shields.io/badge/Database-GitHub%20Gist-black?style=for-the-badge&logo=github&logoColor=white)](https://gist.github.com)
[![Deploy on GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue?style=for-the-badge&logo=github-pages&logoColor=white)](.)
[![Zero Backend](https://img.shields.io/badge/Backend-None%20%E2%9C%93-brightgreen?style=for-the-badge)](.)
[![Single File](https://img.shields.io/badge/Size-1%20File-cyan?style=for-the-badge)](.)

<br/>

![Dashboard Preview](https://img.shields.io/badge/-%F0%9F%94%A5%20Live%20Streaks-ff8c00?style=flat-square) ![LeetCode](https://img.shields.io/badge/-%F0%9F%92%BB%20LeetCode%20Tracker-00f0ff?style=flat-square) ![Projects](https://img.shields.io/badge/-%F0%9F%9B%A0%20Project%20Workspace-b84fff?style=flat-square) ![Leaderboard](https://img.shields.io/badge/-%F0%9F%8F%86%20Leaderboard-aaff00?style=flat-square)

</div>

---

## ✨ What is Grind Squad?

Grind Squad is a **single-file web app** that your whole CSE squad can use to stay accountable together. Built specifically for engineering students who are grinding LeetCode, building projects, and need something more than a shared spreadsheet.

It uses **GitHub Gist as a live shared database** — meaning everyone reads and writes to the same data in real time, with zero server costs, zero setup headache, and it runs perfectly on GitHub Pages.

---

## 🚀 Features

### 📊 Dashboard
- **Daily streak tracker** with fire animations that level up at 7, 14, and 30 days
- **Monthly calendar heatmap** showing your coding activity
- **Taunt banner** — calls you out when a teammate has solved more problems than you today, or when your streak is about to break at midnight
- **Squad overview cards** — see everyone's progress, today's count, streaks, and a 14-day mini heatmap per person at a glance

### 💻 LeetCode Tracker
- Log Easy / Medium / Hard problems solved each day
- Add topic notes (e.g. *"practiced sliding window and two pointers"*)
- **7-day bar chart** showing your solve trend
- Difficulty breakdown bars
- Full history table with 30-entry log

### 🛠 Project Workspace
Full workspace per project with **5 tabs**:

| Tab | What it does |
|-----|-------------|
| **Overview** | Progress stats, task breakdown, recent blackboard preview |
| **Kanban** | Todo → In Progress → Done board with descriptions, due dates, priority, assignee |
| **Blackboard** | Shared live notepad — post Notes, Ideas, Code Snippets, Links, or Blockers |
| **Resources** | Add GitHub repos, docs, tutorials, tools with clickable links |
| **Settings** | Set phase, domain, deadline, GitHub URL, and custom team roles |

**11 project domains** — Web Dev, AI/ML, Mobile, Security, Game Dev, Data Science, Systems, Cloud/DevOps, Blockchain, IoT, Other

**5 project phases** — 💡 Ideation → 🏗️ Building → 🧪 Testing → 🚀 Deployed → ✅ Completed

### 🏆 Leaderboard
- **Streak Kings** — who has the longest active streak
- **LeetCode Warriors** — all-time total solved ranking
- **Today's Battle** — live daily competition board
- **😤 Shame Board** — shows who broke their streak and how many days they've been slacking

### 🔒 Security
- **PIN-protected profiles** — SHA-256 hashed in the browser, stored in the Gist. No one can log in as you without your PIN
- **Shared Squad Token model** — one owner token writes to the Gist; friends join with the same token so GitHub always accepts writes
- **Delete your own profile** — PIN-verified deletion that wipes only your data, leaving squadmates untouched

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                         Browser (You)                           │
│                                                                 │
│   index.html  ◄──── GitHub Pages (static hosting, free)        │
│       │                                                         │
│       │  GitHub API (fetch)                                     │
│       ▼                                                         │
│   GitHub Gist  ◄──── Shared JSON database for the whole squad  │
│                                                                 │
│   localStorage ◄──── Saves your token + session locally only   │
└─────────────────────────────────────────────────────────────────┘
```

**Why Gist as a database?**
- Free, no signup beyond GitHub
- Real-time reads (auto-syncs every 30 seconds)
- Private Gist = only people with the ID can find it
- No rate limit issues for small squads

---

## ⚡ Quick Start

### For the Squad Creator

**1.** Fork or create a new GitHub repo, upload `index.html`, enable GitHub Pages (`Settings → Pages → Deploy from branch → main`)

**2.** Create a GitHub Personal Access Token:
- Go to [github.com/settings/tokens](https://github.com/settings/tokens)
- Click **Generate new token (classic)**
- Check only the **`gist`** scope
- Copy the token

**3.** Open your live site, choose **Create Squad**, paste your token, and create your profile with a PIN

**4.** Share with your squad:
```
🌐 Site URL  : https://your-username.github.io/grind-squad/
🗃️ Gist ID   : (shown on the "All Set" screen)
🔑 Squad Token: (shown on the "All Set" screen — keep this within the squad)
```

### For Squad Members

**1.** Open the site URL your squad creator shared

**2.** Choose **Join Squad**, paste the Squad Token + Gist ID

**3.** Create your profile with a unique name, avatar emoji, and PIN

**4.** Start grinding 🔥

---

## 📁 Project Structure

```
grind-squad/
└── index.html      ← The entire app. That's it.
```

Everything — HTML, CSS, JavaScript, animations, charts, modals — lives in one self-contained file. No build step, no node_modules, no dependencies to install.

---

## 🔧 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Vanilla HTML5, CSS3, JavaScript (ES2020) |
| Fonts | Google Fonts — Orbitron, Share Tech Mono, Nunito |
| Charts | HTML5 Canvas (hand-drawn bar chart) |
| Database | GitHub Gist API (REST) |
| Auth | Browser Web Crypto API (SHA-256 PIN hashing) |
| Hosting | GitHub Pages |
| Storage | localStorage (session only) |

**Zero npm packages. Zero frameworks. Zero cost.**

---

## 🛡️ Privacy & Security Notes

- Your GitHub token is stored **only in your browser's localStorage** — it never leaves your device except to call the GitHub API directly
- PINs are hashed with **SHA-256 + salt** client-side before being stored in the Gist — the raw PIN is never saved anywhere
- The Gist is **private** by default — it won't appear in search results
- Anyone with the Squad Token can read/write the Gist at the API level — only share it with people you trust (same as sharing a Google Doc edit link)

---

## 🤝 How to Update

When a new version of the app is available, just replace `index.html` in your repo:

1. Go to your repo on GitHub
2. Click `index.html` → click the **pencil (edit) icon**
3. Select all → paste the new file contents
4. Click **Commit changes**
5. GitHub Pages redeploys in ~60 seconds ✅

Your squad's data lives in the Gist, not the file — so **updates never wipe any progress**.

---

## 💡 Roadmap Ideas

- [ ] Email/push reminders before streak breaks at midnight
- [ ] Weekly squad digest / report card
- [ ] LeetCode username integration for auto-sync
- [ ] Milestone celebrations (100 problems, 30-day streak)
- [ ] Custom squad goals and weekly targets
- [ ] Dark/light theme toggle

---

## 👥 Made For

> BTech CSE students who are serious about the grind but want to do it **together** — not alone with a spreadsheet.

---

<div align="center">

**Built with 🔥 for squads that refuse to slack**

*Star the repo if it helps your squad grind harder* ⭐

</div>
