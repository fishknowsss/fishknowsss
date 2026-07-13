<picture>
  <source media="(max-width: 640px) and (prefers-color-scheme: dark)" srcset="./assets/hero-mobile-dark.svg">
  <source media="(max-width: 640px) and (prefers-color-scheme: light)" srcset="./assets/hero-mobile-light.svg">
  <source media="(prefers-color-scheme: dark)" srcset="./assets/hero-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/hero-light.svg">
  <img alt="鱼谙 · Yu An — UI/UX, interaction, product engineering, and new media practice" src="./assets/hero-light.svg" width="100%">
</picture>

<h1 align="center">鱼谙 · Yu An</h1>

<p align="center">
  <a href="#selected-work">Projects</a> &nbsp;·&nbsp;
  <a href="#repository-atlas">Repository Atlas</a> &nbsp;·&nbsp;
  <a href="#methods--tools">Methods &amp; Tools</a> &nbsp;·&nbsp;
  <a href="mailto:imnothapi@gmail.com">Email</a>
</p>

## About

> 我把界面结构、系统行为和真实交付放在同一条工作链上。

I'm a Digital Media student working across **UI/UX**, **interaction research**, **visual prototyping**, **product engineering**, and **new media practice**.

My work focuses on how interfaces balance **usability**, **effectiveness**, and **aesthetic quality** — and how media experiences negotiate **expression**, **experience**, and **practical value**. I move from information architecture and interaction states into domain rules, storage, APIs, packaging, updates, and release verification.

My recent projects include **Windows and macOS desktop software**, **local-first studio systems**, **AI video workflows**, **media-processing utilities**, and **Cloudflare-backed operational tools**. Design is not treated as a surface layer; it stays connected to system behavior, failure states, data ownership, and the full task flow.

I'm especially interested in **digital audiovisual interaction**, **new media art**, and the ways **philosophy, literature, and culture** can inform interface and experience design. I'm currently preparing for **graduate study in Japan**, with long-term interests in UI/UX, interaction, frontend, and cross-cultural art and design.

**Current direction** — Research-oriented design · Product systems · Local-first software · New media · Japan

---

## Practice Map

**Desktop systems** — Electron applications for Windows and macOS, plus native C# / WPF tooling. I work through renderer boundaries, local persistence, operating-system integration, packaging, updates, and installed-app verification.

**Local-first studio tools** — Planning, scheduling, account coordination, production tracking, and file organization. Local data remains the default when ownership and continuity matter; cloud sync is added as a deliberate capability rather than an assumption.

**AI and media workflows** — Material upload, prompt annotation, task queues, video download, ffmpeg processing, shot/version organization, and repeatable delivery for real creative-production work.

**Product design to delivery** — Interface structure, business rules, safe credential handling, test gates, release packaging, deployment, and the final path people actually use.

---

## Selected Work

### 01 · YouYu — Windows Mihomo Desktop Client

`Windows x64` · `Electron` · `React` · `TypeScript` · `Mihomo` · `Cloudflare Worker` · `NSIS`

<img src="https://raw.githubusercontent.com/fishknowsss/YouYu/main/docs/screenshots/home-advanced.png" alt="YouYu professional dashboard" width="100%">

YouYu is a Windows x64 Mihomo desktop client designed around two levels of complexity: a single-action beginner mode and a full professional workspace. It brings proxy control, node selection, health checks, TUN, DNS and system-network repair into one coherent desktop experience.

The current product includes:

- Single-node and batch latency testing, subscription refresh, and saved health results.
- Sixteen connectivity checks spanning game platforms, AI services, global sites, and verification services.
- Daily and cumulative traffic analytics, node-usage tracking, and idempotent remote synchronization.
- A 24-state desktop pet with drag, edge, idle, sleep, fall, and expression behaviors.
- Standard, internal-channel, and no-pet editions with independent update metadata.
- Differential updates, integrity validation, full-package fallback, and release checks for public installers.

This project is where product interface, network behavior, operating-system recovery, release engineering, and playful interaction meet in one maintained system.

[Project Site](https://fishknowsss.github.io/YouYu/) · [Repository](https://github.com/fishknowsss/YouYu) · [Latest Release](https://github.com/fishknowsss/YouYu/releases/latest) · [Changelog](https://github.com/fishknowsss/YouYu/blob/main/CHANGELOG.md)

---

### 02 · 118 Studio Manager — Local-first Studio Operations

`React` · `TypeScript` · `IndexedDB` · `PDF.js` · `Cloudflare Worker / KV` · `Vitest` · `Playwright`

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/fishknowsss/118-Studio-Manager/vc/docs/screenshots/vc-dashboard-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/fishknowsss/118-Studio-Manager/vc/docs/screenshots/vc-dashboard-light.png">
  <img src="https://raw.githubusercontent.com/fishknowsss/118-Studio-Manager/vc/docs/screenshots/vc-dashboard-light.png" alt="118 Studio Manager dashboard" width="100%">
</picture>

118 Studio Manager is a browser workspace for small video, design, and content teams. It organizes daily focus, projects, tasks, people, client requirements, shared accounts, schedules, short-drama production, course information, tools, and relationship graphs without requiring a central server for everyday use.

The product is split into seven working areas — home, materials, productivity, short drama, graph, tools, and settings — while keeping IndexedDB as the default data layer. JSON and CSV exchange, PDF schedule parsing, search and focus tools, multiple graph layouts, and optional Cloudflare backup extend the local-first core without changing its ownership model.

The repository includes light and dark interfaces, domain tests, and browser-level coverage. Its value is less about the number of modules than the way a dense studio domain is made navigable without turning into a generic admin panel.

[Repository](https://github.com/fishknowsss/118-Studio-Manager)

---

### 03 · YQhub — Local Seedance Video Workspace

`Electron` · `React` · `TypeScript` · `Seedance 2.0` · `safeStorage` · `Vitest` · `electron-builder`

YQhub is a local Electron workstation for generating video through the Xiaoyunque Skill API. It handles account profiles, drafts, image/video/audio materials, prompt annotations, task queues, current work, history, export naming, and automatic video download.

The renderer never talks to the remote API directly. Credentials and long-running work stay behind a deliberate desktop boundary:

```text
React renderer → preload bridge → Electron IPC → main-process services
               → Xiaoyunque API → task polling → verified local download
```

API keys are encrypted with Electron `safeStorage`; the renderer receives only a masked preview. The project also normalizes remote task states, blocks duplicate active submissions, deduplicates completed downloads, and packages for both macOS Apple Silicon and Windows x64.

[Repository](https://github.com/fishknowsss/YQhub)

---

### 04 · BatchWM — macOS Batch Video Watermark Tool

`macOS arm64` · `Electron` · `React` · `ffmpeg` · `H.264 / AAC` · `Node Tests`

BatchWM is a local media utility for adding text, built-in image, or custom image watermarks to multiple videos. It supports nine-position placement, opacity and size controls, multiple blend modes, landscape/portrait/rotated previews, progress tracking, and remaining-time estimates.

Preview and final export share the same sizing model, including display dimensions for rotated media. `ffmpeg-static` ships with the application, so the user does not need to install a separate media runtime.

```text
Local media → metadata and display dimensions → shared preview/export rules
            → ffmpeg processing → progress reporting → verified output
```

The repository includes automated checks and a release workflow that publishes a macOS arm64 archive with a SHA-256 file.

[Repository](https://github.com/fishknowsss/BatchWM) · [Latest Release](https://github.com/fishknowsss/BatchWM/releases/latest)

---

## More Systems

### ReSeq — Safe Shot and Version Reordering

`Windows` · `C#` · `WPF` · `.NET 8` · `PowerShell`

ReSeq is a native Windows tool for managing short-drama files named by shot and version number. It turns `X-Y` filenames into a thumbnail matrix, lets editors drag a new clip into a row or version position, and shows the complete rename result before touching the file system.

The execution model uses conflict detection, two-stage temporary renaming, best-effort rollback, and a visible log. Tests cover insertion, duplicate numbering, external target conflicts, temporary-file residue, and failed-operation recovery. A self-contained Windows x64 build is available for machines without a preinstalled .NET desktop runtime.

`Folder scan → visual matrix → drag insertion → full preview → two-stage rename → rollback / log`

[Repository](https://github.com/fishknowsss/ReSeq)

### AccMGMT — Runway Resource Scheduling Board

`React` · `TypeScript` · `Tailwind CSS` · `Cloudflare Pages Functions` · `D1` · `Wrangler`

AccMGMT coordinates shared Runway accounts across studio members and projects. It shows availability, active use, future reservations, renewal reminders, project assignments, member groups, and group concurrency limits.

Account status is derived from reservation time rather than stored as a mutable flag. Pages Functions provide the API, D1 stores scheduling data, migrations control schema changes, and session secrets stay outside the public repository. The central business rule is explicit overlap detection: a new reservation is rejected when its time range intersects an existing one for the same account.

`React view model → Pages Functions API → domain rules → D1 repository`

[Repository](https://github.com/fishknowsss/AccMGMT)

### Flowish — Daily Focus and Planning

`React` · `TypeScript` · `Vite` · `GitHub Pages`

Flowish is a lightweight planning space for daily focus, backlog management, recurring rituals, calendar signals, and countdown events. It is intentionally smaller than the studio systems above: a static product with one-click local launchers for macOS and Windows, automatic port selection, and a straightforward GitHub Pages delivery path.

[Open Flowish](https://fishknowsss.github.io/Flowish/) · [Repository](https://github.com/fishknowsss/Flowish)

---

## Repository Atlas

| Repository | Product boundary | Runtime and data | Delivery surface |
|---|---|---|---|
| [YouYu](https://github.com/fishknowsss/YouYu) | Windows proxy, diagnostics, traffic, updates, desktop pet | Electron, React, TypeScript, Mihomo, Worker | Windows x64 installers, project site, GitHub Releases |
| [118 Studio Manager](https://github.com/fishknowsss/118-Studio-Manager) | Studio projects, tasks, people, schedules, production and graphs | React, IndexedDB, optional Worker / KV | Local-first web workspace, protected hosted instance |
| [YQhub](https://github.com/fishknowsss/YQhub) | Local Seedance material-to-video task flow | Electron, safeStorage, local queues and history | macOS arm64 and Windows x64 packages |
| [BatchWM](https://github.com/fishknowsss/BatchWM) | Batch text and image watermarking | Electron, React, bundled ffmpeg | macOS arm64 archive with SHA-256 |
| [ReSeq](https://github.com/fishknowsss/ReSeq) | Shot/version insertion and safe file reordering | WPF, .NET 8, local file system | Self-contained Windows x64 portable build |
| [AccMGMT](https://github.com/fishknowsss/AccMGMT) | Shared account reservations and concurrency rules | React, Pages Functions, D1 | Cloudflare Pages deployment |
| [Flowish](https://github.com/fishknowsss/Flowish) | Personal focus, rituals, calendar signals and countdowns | React, TypeScript, browser-local state | GitHub Pages and one-click local launchers |

These are public repositories, but they do not all carry the same license. **BatchWM currently uses MIT**; the others should not be assumed to grant reuse rights unless their repositories add a license.

---

## How I Work

1. **Start with the real flow.** Map what the user is trying to finish, not only the screen they are looking at.
2. **Model the domain.** Separate interface composition from rules such as reservation overlap, file conflicts, task deduplication, node health, and release-channel identity.
3. **Choose ownership deliberately.** Keep data local when continuity and control matter; introduce cloud storage or backup only where it improves the workflow.
4. **Make trust boundaries visible in the architecture.** Renderers do not receive raw credentials, APIs stay behind main-process or server boundaries, and public repositories are designed to exclude runtime secrets and user data.
5. **Design failure states with the main path.** Network repair, download fallback, rename rollback, conflict prevention, and incomplete-task recovery are part of the product rather than afterthoughts.
6. **Ship the whole path.** Tests, builds, installers, checksums, update metadata, deployment, and final installed/live verification are included in the definition of done.

```text
Interface structure → domain rules → local or cloud data → package / deploy
                    → installed or live verification → usable delivery
```

---

## Methods & Tools

### Evidenced in public repositories

**Product and interface engineering** — `React 19` · `TypeScript` · `JavaScript` · `Vite` · `Tailwind CSS` · `Information Architecture` · `Responsive UI` · `Light / Dark Themes`

**Desktop and operating systems** — `Electron` · `C#` · `WPF` · `.NET 8` · `Windows x64` · `macOS arm64` · `NSIS` · `electron-builder` · `PowerShell`

**Data, cloud, and security** — `IndexedDB` · `electron-store` · `safeStorage` · `Cloudflare Pages` · `Pages Functions` · `D1` · `Workers` · `KV` · `Access` · `Wrangler`

**Media and AI workflows** — `Mihomo` · `ffmpeg` · `Seedance 2.0` · `Xiaoyunque Skill API` · `PDF.js` · `Media Metadata` · `Task Queues` · `Automatic Downloads`

**Testing and delivery** — `Vitest` · `Playwright` · `Node Test Runner` · `.NET Tests` · `ESLint` · `Prettier` · `TypeScript Checks` · `GitHub Actions` · `GitHub Releases` · `SHA-256`

### Design and media practice

**Design / Prototype** — `Figma` · `Framer` · `ProtoPie` · `Sketch` · `Axure RP`

**Visual / Media** — `After Effects` · `Photoshop` · `Illustrator` · `DaVinci Resolve` · `Lightroom` · `FFmpeg`

**Creative Technology** — `Processing` · `p5.js` · `TouchDesigner` · `Unity` · `Three.js` · `Creative Coding`

**Code / Frontend** — `JavaScript` · `TypeScript` · `React` · `Node.js` · `Python` · `Swift` · `Electron` · `Vite` · `Cloudflare` · `C# / .NET`

**3D / Spatial** — `Blender` · `Maya` · `Cinema 4D`

**AIGC / Workflow** — `Midjourney` · `ComfyUI` · `Suno` · `Claude` · `Seedance 2.0`

---

## Research & Practice

| Interface | Experience | Media | Context |
|---|---|---|---|
| UI/UX Design | Interaction Design | Digital Audiovisual Interaction | Cross-cultural Design |
| Information Architecture | Experience Design | New Media Art | Philosophy and Literature |
| Human-Computer Interaction | Visual Prototyping | Creative Coding | Art and Cultural Thinking |
| Product Interface | Local-first Experience | AI Video Workflow | Studio Systems |

My recurring questions are practical and cultural at the same time: how interfaces create trust, how systems shape attention and collaboration, how creative tools reduce or introduce friction, and how visual form changes the way a process is understood.

### Ongoing

**Building**

- YouYu's Windows desktop experience, diagnostics, network safety, and multi-channel release flow.
- YQhub's local AI video workflow, from material annotation to queueing, download, and export.
- 118 Studio Manager's local-first operations model, backup coverage, and small-team information design.
- Practical media tools for watermarking, shot/version organization, and repeatable delivery.
- A research portfolio connecting interaction design, system behavior, and new media practice.

**Preparing**

- Graduate study in Japan, focused on UI/UX and interaction.
- Cross-cultural art and design research.
- Design practice connecting media, philosophy, and interface.

---

## Writing & Other Media

Beyond design, I write on **philosophy**, **literature**, **media**, **contemporary life**, and **social structure**. These reflections shape how I think about interfaces, interaction, and the cultural role of design.

Current notes often return to **interface trust**, **local-first software**, **creative-tool friction**, and the ways systems shape attention, collaboration, and everyday decision-making.

I also work across interface concepts, interaction prototypes, creative coding, audiovisual works, and AIGC-assisted media — each a different way of investigating how experience is **structured**, **perceived**, and **communicated**.

**Independent long-form writing project:** *《满盈》*

---

## FISHKNOWSSS

> A name is a philosophy.

| Letter | Word | Meaning |
|:---:|---|---|
| **F** | Focus | Direct attention with intention, not distraction |
| **I** | Identity | Know who you are before you design for others |
| **S** | Syntonize | Tune in — to context, to users, to the unsaid |
| **H** | Heart | Let feeling inform thinking, not replace it |
| **K** | Kindle | Ignite curiosity, creativity, and care |
| **N** | Nirvana | Seek clarity beyond noise — design toward stillness |
| **O** | Observe | See before you speak. Watch before you make |
| **W** | Wish | Hold a vision of what could be |
| **S** | Simultaneously | Hold contradictions. Live in-between |
| **S** | Sacredly | Treat experience — of others and your own — as worth protecting |
| **S** | Stoically | Persist. Create without attachment to outcome |

***F**ocus **I**dentity. **S**yntonize **H**eart. **K**indle **N**irvana. **O**bserve **W**ish.*<br>
*——— **S**imultaneously, **S**acredly, **S**toically.*

---

## Contact

[GitHub](https://github.com/fishknowsss) · [Email](mailto:imnothapi@gmail.com)

`Designing between function, perception, media, and expression.`
