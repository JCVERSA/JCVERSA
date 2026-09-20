<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0b1026,50:6d28d9,100:06b6d4&height=200&section=header&text=JCVERSA&fontSize=58&fontColor=e0e7ff&fontAlignY=32&desc=%F0%9F%8C%8C%20I%20build%20tools%20that%20work%20%E2%80%94%20not%20demos&descAlignY=56&descColor=a5b4fc&animation=fadeIn" width="100%"/>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1400&color=67E8F9&center=true&vCenter=true&random=false&width=860&lines=WhatsApp+bot+platforms+on+Baileys;Android+%2B+Compose+%C2%B7+Kotlin;TypeScript+strict+%C2%B7+439%2F439+tests;Docker+%C2%B7+VPS+%C2%B7+Cloudflare+Tunnels;Offline-first+tools%2C+audited+before+shipped" alt="Typing SVG"/>
</a>

</div>

---

<div align="center">

```text
\$ whoami
jcversa — self-hosted systems builder & product engineer.

\$ ls ~/work --sort=finish-rate
nebula-p/     439/439 tests · TS strict · one-line VPS install
file/         full product: Express + React 19, security-modeled, e2e-tested
swiftslate/   Android + desktop · release engineering · 43 locales
shipcheck/    zero-dependency repo production-readiness auditor
air-sahre-apk 100% offline file transfer over animated QR

\$ cat philosophy.txt
Ship small. Test everything. Label honestly.
If it can't survive a 1 GB container, it doesn't ship.
```

</div>

---

## 🚢 Currently shipping

| | Project | One line | Proof of life |
|---|---|---|---|
| 🌌 | [**nebula-p**](https://github.com/JCVERSA/nebula-p) | Self-hosted WhatsApp media & AI command center | `439/439` tests · TS strict · `manage.sh doctor` exit 0 |
| 🗂️ | [**file**](https://github.com/JCVERSA/file) *(Smopi)* | Password-protected temp file share + AI file assistant | e2e smoke suite · timing-safe auth · traversal-safe FS |
| ⌨️ | [**swiftslate**](https://github.com/JCVERSA/swiftslate) | AI command palette for Android + Windows desktop | R8-shrunk APK · release-signing guardrails · 43 locales |
| 🛡️ | [**shipcheck**](https://github.com/JCVERSA/shipcheck) | `pip install`-able repo production-readiness auditor | pure Python · zero runtime deps · CI exit codes |
| 📡 | [**air-sahre-apk**](https://github.com/JCVERSA/air-sahre-apk) | AirQR — air-gapped file transfer over animated QR | Base45/RFC 9285 · 30 FPS streams · SHA-256 integrity |

---

## 🌌 Flagship — Nebula Bot

<div align="center">

**A WhatsApp media & AI command center in one ~1 GB container, behind a Cloudflare Tunnel.**

*VF anime downloader with honest size labels · screenshot-to-anime ID · new-episode watcher ·
Gemini AI with NVIDIA NIM fallback · sandboxed panel-created commands · full React panel ·
one-line idempotent install.*

`curl -fsSL "https://raw.githubusercontent.com/JCVERSA/nebula-p/main/scripts/install.sh" | sh`

</div>

**What "battle-tested" actually means here:**

| Layer | What was engineered |
|---|---|
| 📺 Media engine | HLS segment downloader → ffmpeg remux → streaming ZIP writer, disk-streamed with backpressure |
| 🔗 Delivery | Tokenized 2 h download links, HTTP range streaming, offline HTML batch pages |
| 🔐 Security | HttpOnly session auth + CSRF checks, SSRF guard w/ DNS pinning, host-header guard, sandboxed `vm` commands |
| 🧠 AI | Gemini chat/image/voice + per-user daily budgets, NVIDIA NIM fallback for outages, persistent memory |
| 🛠️ Ops | `manage.sh start/stop/update/doctor/env/logs/clean` — a full VPS lifecycle in one script |
| 🧪 Testing | 439 tests across 47 files; anime engine, ZIP writer and command registry locked by tests |

Every fix is traced in a 157 KB engineering audit log — bugs, root causes, and the fix that closed each one.

---

## 🧩 The rest of the shelf

| Project | What it is | Stack |
|---|---|---|
| [**NAMI**](https://github.com/JCVERSA/NAMI) | Debian XRDP + XFCE4 in Docker — a remote desktop with a real security posture, not "just expose 3389" | Docker · Shell |
| [**NIMO**](https://github.com/JCVERSA/NIMO) | Ubuntu Desktop in Docker, in your browser | Docker · Shell |
| [**docker-vscode-server**](https://github.com/JCVERSA/docker-vscode-server) | VS Code Server, containerized | Docker |
| [**web-to-app**](https://github.com/JCVERSA/web-to-app) | Any URL → standalone Android app | Kotlin |
| [**FileToLink**](https://github.com/JCVERSA/FileToLink) | Telegram file → direct link bot on pyrofork | Python |
| [**interactive-smopi-ai-avatar**](https://github.com/JCVERSA/interactive-smopi-ai-avatar) | Interactive AI avatar experiment | TypeScript |

---

## ⚡ How I work

| | |
|---|---|
| 🧪 **Tests before claims** | 439 automated tests on Nebula; e2e smoke suites on File Share; CI-gated exit codes on shipcheck |
| 🛡️ **Security by default** | timing-safe compares, rate limits, path-traversal-safe resolution, SSRF guards, secrets never committed |
| 📏 **Honest labels** | a 403 MB "480P" gets downgraded to the real lightest variant — the bot never lies about what it delivered |
| 📦 **Container-first** | everything designed for ~1 GB RAM caps, streaming instead of loading, idempotent one-line installers |
| 🌍 **Ship to everyone** | 43 locales in SwiftSlate, derived from `res/` so nothing silently stops shipping |

---

## 🧰 Toolbox

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Shell](https://img.shields.io/badge/Shell-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Baileys](https://img.shields.io/badge/Baileys-25D366?style=flat-square&logo=whatsapp&logoColor=white)
![ffmpeg](https://img.shields.io/badge/ffmpeg-007EC7?style=flat-square&logo=ffmpeg&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

</div>

---

## 📊 GitHub

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=JCVERSA&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=8b5cf6&icon_color=06b6d4&text_color=c9d1d9" alt="JCVERSA stats"/>
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=JCVERSA&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=8b5cf6&text_color=c9d1d9&langs_count=8" alt="top languages"/>

<br/>

<img width="95%" src="https://github-readme-activity-graph.vercel.app/graph?username=JCVERSA&theme=react-dark&hide_border=true&bg_color=0D1117&color=a5b4fc&line=8b5cf6&point=06b6d4&area=true&area_color=6d28d9" alt="activity graph"/>

</div>

---

## 🗺️ The map so far

```text
2025 ▸ first commits — Telegram bots, pairing servers, YouTube tooling
2026 ▸ the Nebula ecosystem: from a bot that OOM-crashed → 439-test,
       TS-strict platform with a one-line installer
     ▸ File Share + Smopi: a security-modeled product with an AI assistant
     ▸ SwiftSlate: Android + desktop, release-audited, 43 locales
     ▸ shipcheck: auditing other repos for production-readiness
next ▸ faster Nebula · more people actually using these tools
```

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0b1026,100:1b1140&height=3" width="85%"/>

*Built with curiosity, caffeine, and a VPS that survived it all.* 🚀

**⭐ Star [Nebula Bot](https://github.com/JCVERSA/nebula-p) if it saves you time.**

</div>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:06b6d4,50:6d28d9,100:0b1026&height=120&section=footer" width="100%"/>

</div>
