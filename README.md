<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=4000&pause=1000&color=A177FE&center=true&vCenter=true&random=false&width=640&lines=%F0%9F%91%8B+Hey%2C+I'm+Nixo;%F0%9F%96%A5%EF%B8%8F+ICT+Technician+%7C+%F0%9F%8F%A0+Homelab+Operator;%F0%9F%A4%96+I+build+the+tools+I+need%2C+then+I+host+them;%F0%9F%94%B4+And+I+play+Minecraft+on+TikTok+Live" alt="Typing SVG" />

<br/>

[![TikTok](https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white)](https://tiktok.com/@thanixontiktok)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@tha_nixo)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/tha_nixo_tv)
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/skC9z79Xwf)
[![Twitter](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/tha_nixo)

</div>

---

## 🧑‍💻 About Me

I'm **Nicola** — ICT technician in Italy, and the sysadmin of a homelab that never asked to get this big.

Everything I build ends up on the same box: a **10-year-old Intel i5-6500T** running Ubuntu 24.04 with dozens of Docker services, each one behind a reverse proxy with SSO, monitored by Prometheus/Grafana and audited by a SIEM. If a workflow annoys me twice it becomes a service. If a service breaks at 3 AM, a Telegram bot tells me before I notice.

- 🔧 **Day job:** Windows 11 / Microsoft 365 / Active Directory / SharePoint — endpoint, identity and support work
- 🌙 **Night job:** Linux, Docker, reverse proxies, AI agents and trading bots running on my own metal
- 🔴 **Evenings:** Minecraft 1.8.9 PvP on TikTok Live
- 🎹 Piano by ear (*Nuvole Bianche*, *River Flows in You*) · 🏐 volleyball 3×/week · 🎵 trap enjoyer

---

## 🚀 What I'm Building

| Project | What it actually does |
|---|---|
| 🧠 **MERLINO** | Personal "Jarvis": drives headless AI coding agents across my infrastructure. Every tool call goes through a pre-execution hook that can hard-deny it — a permission callback alone isn't a real chokepoint. |
| 🛡️ **Server hardening** | Full-server security audit turned into **34 shipped fixes**: secret rotation, SIEM deployment, host firewall and intrusion-banning rules, least-privilege cleanup across every unattended process. |
| 📈 **Golden-Cross bot** | BTC/USDT trend-following bot on Binance, systemd-managed. Live trading sits behind **two independent gates**, so no single config slip can start spending real money. |
| 🎲 **Polymarket 5m bot** | Copy-trader and scalper on BTC/ETH/SOL/XRP 5-minute markets, with an adverse-continuation exit rule and a slimmed visual-data pipeline feeding the decision model. |
| 🧰 **[techtool.site](https://techtool.site)** | **50 developer tools** in one static, dependency-free site — hashing, encoding, converters, generators — served with a strict CSP and HSTS. |
| 🕸️ **FileGraph** | Live 3D WebGL map of an entire server filesystem: **139,000 nodes rendered in 38 draw calls**, via server-side layout, a binary wire protocol (2.9 MB instead of 46 MB of JSON) and GPU instancing. |
| 📊 **DevSync Hub** | Homelab dashboard wired to real service state — no mock data, no decorative uptime numbers. |
| 🛒 **amazon-ram-monitor** | DDR5 price tracker polling EU storefronts hundreds of times a week, with detection and back-off for every shape of soft-block Amazon throws at it. |
| 🏆 **supercell-stats** | Clash Royale / Brawl Stars stats site, routed through a fixed-IP proxy because Supercell pins API keys to an IP. |
| 🤖 **Telegram bots** | Four of them: infra alerts, media requests, the daily server report, and a shared control bot. |

> Most of these live in private repos — they hold live credentials for my own infrastructure. Everything below is public and browsable.

### 📂 Public repos

- **[ThePasswordCrack](https://github.com/Tha-Nixo/ThePasswordCrack)** — Chrome extension that auto-solves [The Password Game](https://neal.fun/password-game/): a constraint solver, a runtime memory spy and a network interceptor, **29 of 35 rules** beaten. `TypeScript` · `Manifest V3`
- **[ClaudeCodeManager](https://github.com/Tha-Nixo/ClaudeCodeManager)** — A desktop compositor for Claude Code sessions on Windows. Tiling and floating panes, each with its own terminal and `claude` process, drag-to-rearrange, fuzzy project picker, session resume. `TypeScript` · `Electron`

> Nearly all of it runs on my own hardware, behind my own reverse proxy, watched by my own dashboards — including the GitHub stats cards further down this page.

---

## 🏠 Homelab — `hydrogenomb`

**Intel i5-6500T · Ubuntu 24.04 · Docker · Caddy + Authelia in front of everything · Wazuh watching it all**

<details>
<summary>📦 <b>Click to see the full stack</b></summary>
<br/>

| Category | Services |
|---|---|
| 🔒 **Auth & Security** | Authelia (SSO + 2FA, deny-by-default) · Wazuh SIEM · Fail2ban · UFW |
| 🌐 **Networking & DNS** | Caddy (per-host ACME) · AdGuard Home · Cloudflare DDNS · Tailscale |
| 📊 **Monitoring** | Prometheus · Grafana (custom dashboards) · Uptime Kuma · Scrutiny (disk SMART) · cAdvisor · Dozzle |
| 🎬 **Media** | Jellyfin (Intel QuickSync transcoding) · Radarr / Sonarr / Prowlarr · Decluttarr · Immich · RomM · Kavita |
| 🎮 **Gaming** | Minecraft Paper server on Pterodactyl (AuthMe + FastLogin) · mc-router |
| 🤖 **Automation** | n8n · custom Telegram bots · nightly health-report cron · Watchtower |
| 🛠️ **Tools** | Portainer · Dockge · Code Server · IT-Tools · Zipline · Umami |
| 📚 **Docs** | MkDocs at `docs.nixospace.it` — service pages generated automatically from the running stacks |

</details>

**Three things this box taught me the hard way:**

- 🕵️ AdGuard Home's `ratelimit` is **per-server, not per-client** — the default silently throttled my whole LAN and looked exactly like flaky Wi-Fi for weeks.
- 🎨 Draw calls, not GPUs, kill a 139k-node WebGL scene: **24,566 → 38** through batching and instancing, with zero hardware changes.
- 🧾 `set -e` in a cron'd shell script fails *silently* — my documentation generator had been dead for two months before anything surfaced it. Now every scheduled job reports, success or failure.

---

## 🛠️ Tech Stack

<div align="center">

**Languages I actually ship in**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

**Infrastructure & Ops**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1F88C0?style=flat-square&logo=caddy&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![systemd](https://img.shields.io/badge/systemd-30D475?style=flat-square&logo=systemd&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**AI & Automation**

![Claude](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram_Bots-26A5E4?style=flat-square&logo=telegram&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)

**Day job**

![Windows 11](https://img.shields.io/badge/Windows_11-0078D4?style=flat-square&logo=windows11&logoColor=white)
![Microsoft 365](https://img.shields.io/badge/Microsoft_365-D83B01?style=flat-square&logo=microsoft&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active_Directory-0078D4?style=flat-square&logo=microsoft&logoColor=white)
![SharePoint](https://img.shields.io/badge/SharePoint-0078D4?style=flat-square&logo=microsoftsharepoint&logoColor=white)

</div>

---

## 🔴 Streaming & Gaming

<div align="center">

| | |
|---|---|
| 📡 **Where** | [TikTok Live](https://tiktok.com/@thanixontiktok) — most evenings |
| 🎯 **What** | Minecraft **1.8.9 PvP** on Lunar Client, Fortnite, horror runs (Visage) |
| 🌐 **My server** | Self-hosted Paper server on Pterodactyl, AuthMe + FastLogin |
| 🖥️ **Rig** | Ryzen 9 7900X · RX 9070 · RTX 3050 as a dedicated encoder · 270 Hz |

</div>

---

## 📊 GitHub Stats

<div align="center">

<!-- Self-hosted github-readme-stats on my own homelab — the public Vercel instance is permanently rate-limited (503). -->
<img src="https://stats.nixospace.it/api?username=Tha-Nixo&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A177FE&icon_color=A177FE&text_color=C9D1D9" alt="GitHub Stats" height="170"/>
<img src="https://stats.nixospace.it/api/top-langs?username=Tha-Nixo&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A177FE&text_color=C9D1D9" alt="Top Languages" height="170"/>

<br/>

<img src="https://streak-stats.demolab.com/?user=Tha-Nixo&theme=tokyonight&hide_border=true&background=0D1117&ring=A177FE&fire=A177FE&currStreakLabel=A177FE" alt="GitHub Streak"/>

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Tha-Nixo&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=A177FE&line=A177FE&point=FFFFFF" alt="Activity Graph" width="100%"/>

<sub>☝️ The top two cards are rendered by my own homelab, not by the public instance. Fitting, I think.</sub>

</div>

---

## 🐍 Contribution Snake

<div align="center">

<!-- Requires the Platane/snk workflow in this repo, output pushed to the `output` branch -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Tha-Nixo/Tha-Nixo/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Tha-Nixo/Tha-Nixo/output/github-snake.svg" />
  <img alt="github-snake" src="https://raw.githubusercontent.com/Tha-Nixo/Tha-Nixo/output/github-snake-dark.svg" />
</picture>

</div>

---

<div align="center">

<img src="https://komarev.com/ghpvc/?username=Tha-Nixo&style=for-the-badge&color=A177FE" alt="Profile Views"/>

**Thanks for stopping by!** 💜

*Come break something with me on [TikTok](https://tiktok.com/@thanixontiktok) or in the [Discord](https://discord.gg/skC9z79Xwf).*

</div>
