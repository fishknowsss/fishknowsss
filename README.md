<div align="center">

# 鱼谙 · Yu An

**数字媒体 · 交互设计 · 产品工程**

把界面研究、视听媒介与工程实现，做成可运行、可验证的产品。

[![Email](https://img.shields.io/badge/Email-imnothapi%40gmail.com-5C5470?style=flat-square&logo=gmail&logoColor=white)](mailto:imnothapi@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-fishknowsss-24292F?style=flat-square&logo=github&logoColor=white)](https://github.com/fishknowsss)

</div>

## 关于我

我是一名数字媒体方向的学习者，关注 **UI/UX、交互设计、信息架构、视觉原型与新媒体实践**。我在意界面如何在可用性、效率与审美之间取得平衡，也在持续探索哲学、文学和跨文化语境如何进入产品体验。

目前的实践以本地优先桌面工具、AI 视频工作流和小型团队协作系统为主。除了设计界面，我也会完成领域建模、前后端实现、桌面打包、自动更新、云端部署和发布验证，让想法真正进入可使用的状态。

正在准备赴日继续学习，研究方向聚焦 UI/UX、交互与数字视听媒介。

## 当前方向

- **桌面产品**：Electron、Windows WPF、本地存储、系统能力与跨平台交付。
- **AI 与视频工作流**：生成任务编排、素材处理、视频工具和安全的本地凭据管理。
- **工作室系统**：项目、任务、成员、账号资源、排期、备份与轻量云同步。
- **设计研究**：人机交互、信息组织、视觉原型、新媒体艺术与跨文化设计。

## 项目

### 桌面工具

#### [YouYu](https://github.com/fishknowsss/YouYu) · Windows Mihomo 客户端

面向 Windows x64 的 Mihomo 桌面客户端，支持代理管理、节点测速、16 项连通性检测、TUN、网络修复、流量统计、三套独立更新通道与 24 种状态的桌宠。

`Electron` `React` `TypeScript` `Mihomo` `NSIS`

[项目主页](https://fishknowsss.github.io/YouYu/) · [最新版本](https://github.com/fishknowsss/YouYu/releases/latest)

#### [YQhub](https://github.com/fishknowsss/YQhub) · Seedance 本地生成工作台

通过小云雀 Skill API 调用 Seedance 2.0 的本地 Electron 工作台，覆盖账号密钥、素材上传与标注、任务队列、生成历史和视频自动下载。敏感凭据由 Electron `safeStorage` 在本机加密保存。

`Electron` `React` `TypeScript` `Vite` `Vitest`

#### [BatchWM](https://github.com/fishknowsss/BatchWM) · macOS 批量视频水印

本地运行的 macOS arm64 视频处理工具，支持文字与图片水印、九宫格位置、横竖屏预览、批量进度和剩余时间估算。预览与导出共用尺寸规则，由内置 ffmpeg 完成 H.264/AAC 输出。

`Electron` `React` `JavaScript` `ffmpeg` `GitHub Actions`

[下载](https://github.com/fishknowsss/BatchWM/releases/latest)

#### [ReSeq](https://github.com/fishknowsss/ReSeq) · 分镜视频安全重排

Windows 原生 WPF 工具，以 `分镜号-版本号` 管理短剧视频。支持缩略图矩阵、拖拽插入镜头或版本、执行前预览，以及带冲突检查和失败回滚的两阶段安全重命名。

`C#` `.NET 8` `WPF` `PowerShell`

### Web 与工作室系统

#### [118 Studio Manager](https://github.com/fishknowsss/118-Studio-Manager) · 本地优先工作室管理

面向小型视频、设计和内容团队的浏览器应用，覆盖每日排班、项目任务、成员状态、甲方资料、账号素材、工效课表、短剧制作、关系图谱和备份同步。数据默认保存在 IndexedDB，可选接入自托管 Cloudflare Worker。

`React` `TypeScript` `IndexedDB` `Cloudflare Workers` `Playwright`

#### [AccMGMT](https://github.com/fishknowsss/AccMGMT) · Runway 账号资源看板

用于集中查看账号空闲、占用与预约状态的工作室看板，支持时间冲突检测、成员小组并发限制、项目管理和使用记录。前端部署在 Cloudflare Pages，数据由 Pages Functions 与 D1 管理。

`React` `TypeScript` `Tailwind CSS` `Cloudflare Pages` `D1`

#### [Flowish](https://github.com/fishknowsss/Flowish) · 日常规划面板

围绕每日焦点、待办池、日常仪式、日历信号和倒数事件构建的静态 React 应用，可在本地运行，也可通过 GitHub Pages 使用。

`React` `TypeScript` `Vite` `GitHub Pages`

[在线使用](https://fishknowsss.github.io/Flowish/)

## 技术与方法

**产品工程**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Electron](https://img.shields.io/badge/Electron-2B2E3A?style=flat-square&logo=electron&logoColor=9FEAF9)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)

**设计与研究**

`UI/UX` · `Interaction Design` · `Information Architecture` · `Visual Prototyping` · `Design Research` · `Digital Audiovisual Interaction` · `New Media Art`

---

<div align="center">

*Designing between function, perception, media, and expression.*

</div>
