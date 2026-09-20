<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0b1026,50:6d28d9,100:06b6d4&height=200&section=header&text=JCVERSA&fontSize=58&fontColor=e0e7ff&fontAlignY=32&desc=%F0%9F%8C%8C%20I%20build%20tools%20that%20work%20%E2%80%94%20not%20demos&descAlignY=56&descColor=a5b4fc&animation=fadeIn" width="100%"/>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1400&color=67E8F9&center=true&vCenter=true&random=false&width=900&lines=WhatsApp+bot+platforms+on+Baileys;Android+%2B+Compose+%C2%B7+Kotlin;TypeScript+strict+%C2%B7+439+tests+on+Nebula;Docker+%C2%B7+VPS+%C2%B7+Cloudflare+Tunnels;Offline-first+tools%2C+audited+before+shipped" alt="Typing SVG"/>
</a>

<br/>

[🚢 Shipping](#-currently-shipping) · [🌌 Flagship](#-flagship--nebula-bot) · [📚 Full catalog](#-the-full-catalog) · [📜 Archive](#-archive--earlier-iterations) · [🧰 Toolbox](#-toolbox) · [📊 Stats](#-github)

</div>

---

<div align="center">

```text
$ whoami
jcversa — self-hosted systems builder & product engineer.
46 public repos — 24 finished builds catalogued below, the rest are iterations
I keep public on purpose, plus 6 empty placeholders I should clean up.

$ ls ~/work --sort=finish-rate
nebula-p/     439 tests · TS strict · one-line idempotent VPS install
minen/        MiniCloud — gateway + 7 microservices, one storage volume
swiftslate/   Android + Windows desktop · 40 languages · release engineering
file/         full product: Express + React 19, security-modelled, e2e-tested
shipcheck/    zero-dependency repo production-readiness auditor
airqr/        100% offline file transfer over animated QR — phone and browser
sonic-bit/    acoustic modem — bytes over sound, in C and TypeScript

$ cat philosophy.txt
Ship small. Test everything. Label honestly.
If it can't survive a 1 GB container, it doesn't ship.
Every number on this page is checkable in the repo it links to.
```

</div>

---

## 🚢 Currently shipping

| | Project | One line | Proof of life |
|---|---|---|---|
| 🌌 | [**nebula-p**](https://github.com/JCVERSA/nebula-p) | Self-hosted WhatsApp media & AI command center | `439` tests / 47 files · TS `strict` · `manage.sh doctor` |
| ☁️ | [**minen**](https://github.com/JCVERSA/minen) | **MiniCloud** — private cloud suite on one shared VPS volume | gateway + 7 services · JWT cookie auth · AES-256-GCM vault |
| 🗂️ | [**file**](https://github.com/JCVERSA/file) | Password-protected temp file share + AI file assistant | e2e smoke suite · `timingSafeEqual` auth · traversal-safe FS |
| ⌨️ | [**swiftslate**](https://github.com/JCVERSA/swiftslate) | System-wide AI text assistant — Android + Windows desktop | R8 + release-signing config · 5 CI workflows · 40 languages |
| 🛡️ | [**shipcheck**](https://github.com/JCVERSA/shipcheck) | `pip install`-able repo production-readiness auditor | pure Python · `dependencies = []` · CI exit codes |
| 📡 | [**air-sahre-apk**](https://github.com/JCVERSA/air-sahre-apk) | **AirQR** — air-gapped file transfer over animated QR (Android) | Base45/RFC 9285 · 30 FPS streams · SHA-256 integrity |

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
| 🧪 Testing | `439` tests across 47 files; anime engine, ZIP writer and command registry locked by tests |

Every fix is traced in a **157 KB** download-pipeline audit log (`ANIME_DOWNLOAD_AUDIT.md`) — bugs, root causes, and the fix that closed each one.

---

## 📚 The full catalog

Twenty finished things, grouped by what they actually are.

### 🌐 Self-hosted web products

| Project | What it is | Evidence in the repo |
|---|---|---|
| [**minen**](https://github.com/JCVERSA/minen) · **MiniCloud** | Private cloud suite: files, notes, gallery, encrypted vault, bookmarks, admin — behind one gateway | `gateway:3000` + 7 independent services (`auth`…`admin`) sharing one `STORAGE_DIR`, stateless JWT, per-user quotas, `start.sh` |
| [**file**](https://github.com/JCVERSA/file) · **File Share + Smopi** | Password-protected temporary file sharing with an AI file-management assistant | 1 293-line `server.ts`, `crypto.timingSafeEqual` on every secret compare, path-traversal-safe resolution, HttpOnly `SameSite=Lax`, `fsd` CLI, `tests/smoke.test.mjs` |
| [**smopi**](https://github.com/JCVERSA/smopi) | Next iteration of File Share with the Smopi avatar rig baked into the workspace | adds `src/components/smopi/*` + `SmopiWorkspaceView` on top of the `file` codebase |
| [**air-share**](https://github.com/JCVERSA/air-share) · **AirQR Turbo** | The browser half of AirQR — two machines, no network | offscreen-canvas ring buffer for 0 ms frame swaps, ROI decode on the centre 70 % of the viewfinder, `BarcodeDetector` when available, Web Crypto SHA-256 |
| [**nebula-dashboard**](https://github.com/JCVERSA/nebula-dashboard) | Standalone HTML/Node control surface for the Nebula stack | `dashboard.html` + `server.js`, no build step |
| [**Pair**](https://github.com/JCVERSA/Pair) | Baileys pairing-session generator served as a tiny web app | `index.html` + `index.js`, self-hostable |

### 📱 Android & desktop

| Project | What it is | Evidence in the repo |
|---|---|---|
| [**swiftslate**](https://github.com/JCVERSA/swiftslate) | Type `?fix` at the end of any text, in any app, and it gets replaced. Gemini / Groq / any OpenAI-compatible endpoint — plus a **Windows desktop port** in the same repo | 215 files, Jetpack Compose + `desktop/` Python port, 5 workflows (`ci`, `build`, `release`, `desktop-ci`, `preview-comment`), fastlane, AES-256-GCM keystore storage |
| [**air-sahre-apk**](https://github.com/JCVERSA/air-sahre-apk) · **AirQR** | Kotlin + Compose optical transport: file → animated QR stream → camera → byte-for-byte verified file | Base45 alphanumeric mode, gzip chunking, pre-rendered BitMatrix buffer, CameraX ROI scanning, loopback self-test mode, CI `build.yml` |
| [**Kitsu**](https://github.com/JCVERSA/Kitsu) | Kotlin anime app (`com.neon.franimeapp`) carried alongside a 55-skill agent toolkit | Gradle app module + `.agents/skills/` library |
| [**franime-app**](https://github.com/JCVERSA/franime-app) | Java/Android anime client — Retrofit API layer, adapter-driven list UI, two GitHub Actions workflows | `ApiService` + `RetrofitClient` + `AnimeAdapter`, `main.yml` CI |

### 🐳 Containers & VPS infrastructure

| Project | What it is | Evidence in the repo |
|---|---|---|
| [**NAMI**](https://github.com/JCVERSA/NAMI) | Debian XRDP + XFCE4 remote desktop in Docker, with a security posture instead of "just expose 3389" | Compose + `.env` pattern, optional Wine/Firefox build args, persistent volume, explicit "trusted network only" notice |
| [**NIMO**](https://github.com/JCVERSA/NIMO) | Full Ubuntu desktop, in your browser, over noVNC | Single `Dockerfile`, published image, MIT |
| [**Neon-Space**](https://github.com/JCVERSA/Neon-Space) | Provisioning kit for a fresh box: RDP, Tailscale, user management, cleanup | PowerShell scripts + `rdp.yml` / `chill.yml` workflows |
| [**kwep**](https://github.com/JCVERSA/kwep) | Little toolbox of VPS shell utilities kept in one place | `Ai.sh`, `play`, `rdp`, `tail`, `tyop`, `vpsmaker`, `vsp908` |
| [**Ssh.jc**](https://github.com/JCVERSA/Ssh.jc) | Tunnel and file-share bootstrappers for a headless server | `Install.sh`, `fxtunnel-installer.sh`, `share-file-v2.sh` |
| [**Deb**](https://github.com/JCVERSA/Deb) | Minimal Debian base container | `Dockerfile` + `start.sh` |

### 🧰 CLI & developer tooling

| Project | What it is | Evidence in the repo |
|---|---|---|
| [**shipcheck**](https://github.com/JCVERSA/shipcheck) | Point it at any repository and it tells you what would embarrass you in production — hardcoded keys, committed `.env`, bare `except:`, missing LICENSE/CI | `dependencies = []`, `requires-python >= 3.9`, table/`--markdown`/`--json` output, `--fail-on` gating, exit `0`/`1`/`2`, pytest suite |
| [**sonic-bit**](https://github.com/JCVERSA/sonic-bit) | An acoustic modem — data over sound — implemented twice: a C library with its own test binary, and a TypeScript DSP front-end | `acoustic_modem/` (CMake, Makefile, `wav`/`stream`/`cli`, `tests/test_modem.c`) + `src/dsp/AcousticModemDSP.ts` |
| [**Ghgrab-termux-beta**](https://github.com/JCVERSA/Ghgrab-termux-beta) | GitHub content downloader built for Termux, with an explicit layered architecture | `ARCHITECTURE.md`, `src/{api_client,downloader,models,tui,utils}`, CLI entrypoint |

### 🧪 Experiments

| Project | What it is |
|---|---|
| [**interactive-smopi-ai-avatar**](https://github.com/JCVERSA/interactive-smopi-ai-avatar) | React avatar rig — geometry, a `useSmopiRig` hook and an animated SVG face driving a chat demo |
| [**ytmm-bot**](https://github.com/JCVERSA/ytmm-bot) | Single-file YouTube/Telegram bot, Dockerfile + Procfile, deployable as-is |

### 📦 Ports & upstream builds

Repos where the engineering is in the packaging, not the original code — listed honestly:

| Project | What it is |
|---|---|
| [**XOutput-3.32**](https://github.com/JCVERSA/XOutput-3.32) | Pinned working copy of the XOutput DirectInput → XInput mapper (C#, 242 files) |
| [**Franima**](https://github.com/JCVERSA/Franima) | Dockerised, pre-commit-configured build of the Scrapling scraping framework |

---

## 📜 Archive & earlier iterations

I keep these public instead of deleting them — the lineage is the point, and pretending 46 repos are 46 finished products would be dishonest.

| Lineage | Repos | What happened |
|---|---|---|
| 🌌 **Nebula Bot** | [`nebula-p-st`](https://github.com/JCVERSA/nebula-p-st) · [`oo-oo`](https://github.com/JCVERSA/oo-oo) · [`neb`](https://github.com/JCVERSA/neb) · [`nova`](https://github.com/JCVERSA/nova) · [`Na`](https://github.com/JCVERSA/Na) · [`bot`](https://github.com/JCVERSA/bot) · [`remix-nebula-bot`](https://github.com/JCVERSA/remix-nebula-bot) · [`nm`](https://github.com/JCVERSA/nm) · [`botn`](https://github.com/JCVERSA/botn) · [`nebula-bot-latest`](https://github.com/JCVERSA/nebula-bot-latest) · [`Nebula-bot-2.9`](https://github.com/JCVERSA/Nebula-bot-2.9) | 11 generations, from a 126-command fork through rewrites and Remix detours, until `nebula-p` became the one that passed its own tests |
| ⌨️ **SwiftSlate** | [`SwiftSlate-ng`](https://github.com/JCVERSA/SwiftSlate-ng) · [`swift`](https://github.com/JCVERSA/swift) | Earlier Android trees; the desktop port and locale set now live in `swiftslate` |
| 🗂️ **File Share** | [`file-share`](https://github.com/JCVERSA/file-share) | The Python-original implementation, kept as reference inside `file/cloned/` |

<details>
<summary><b>Placeholders I should clean up (6 empty repos)</b></summary>

<br/>

`nb` · `n` · `13` · `MCBE` · `template` · `gg-jjik-llop009-iiou0-hghn-opu` — created, never filled. Not linked on purpose.

</details>

---

## ⚡ How I work

| | |
|---|---|
| 🧪 **Tests before claims** | 439 automated tests on Nebula; e2e smoke suite on File Share; pytest + CI exit codes on shipcheck |
| 🛡️ **Security by default** | timing-safe compares, rate limits, path-traversal-safe resolution, SSRF guards, secrets kept out of source |
| 📏 **Honest labels** | a 403 MB "480P" gets downgraded to the real lightest variant — the bot never lies about what it delivered |
| 📦 **Container-first** | designed for ~1 GB RAM caps, streaming instead of loading, idempotent one-line installers |
| 🔍 **Audited, not assumed** | every number on this page traces to a file, a config value or a test in the linked repo |
| 🌍 **Ship to everyone** | 40 languages in SwiftSlate, derived from `res/` so nothing silently stops shipping |

---

## 🧰 Toolbox

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
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
     ▸ File Share + Smopi: a security-modelled product with an AI assistant
     ▸ MiniCloud: gateway + 7 microservices on one shared storage volume
     ▸ SwiftSlate: Android + desktop, release-audited, 40 languages
     ▸ shipcheck: auditing other repos for production-readiness
     ▸ AirQR + sonic-bit: offline transports — light and sound
next ▸ faster Nebula · published releases · more people actually using these tools
```

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0b1026,100:1b1140&height=3" width="85%"/>

*Built with curiosity, caffeine, and a VPS that survived it all.* 🚀

**⭐ Star [Nebula Bot](https://github.com/JCVERSA/nebula-p) if it saves you time.**

</div>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:06b6d4,50:6d28d9,100:0b1026&height=120&section=footer" width="100%"/>

</div>
