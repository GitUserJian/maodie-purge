<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=2600&pause=900&color=10B981&center=true&vCenter=true&width=720&lines=Maodie+Armor;DSH+Prompt+Engineering+Plugin;Dual-Layer+Injection+%C2%B7+Skills+%C2%B7+Pentest+Console" alt="Maodie Armor" />
</p>

<h1 align="center">Maodie Armor · 耄耋破甲</h1>
<p align="center">
  <b>A local prompt-engineering plugin for DeepSeek Harness — one-click inject / uninstall, skill packs, and an AI pentest console.</b><br/>
  <b>面向 DeepSeek Harness 的本地提示词工程插件 · 一键注入 / 卸载 · 技能包 · AI 渗透控制台</b>
</p>

<p align="center">
  <a href="https://github.com/Wei0417-top/Maodie-purge/stargazers"><img src="https://img.shields.io/github/stars/Wei0417-top/Maodie-purge?style=for-the-badge&logo=github&color=10b981&labelColor=111827" alt="stars" /></a>
  <a href="https://github.com/Wei0417-top/Maodie-purge/network/members"><img src="https://img.shields.io/github/forks/Wei0417-top/Maodie-purge?style=for-the-badge&logo=github&color=3b82f6&labelColor=111827" alt="forks" /></a>
  <a href="https://github.com/Wei0417-top/Maodie-purge/issues"><img src="https://img.shields.io/github/issues/Wei0417-top/Maodie-purge?style=for-the-badge&logo=github&color=f59e0b&labelColor=111827" alt="issues" /></a>
  <a href="https://github.com/Wei0417-top/Maodie-purge/pulls"><img src="https://img.shields.io/github/issues-pr/Wei0417-top/Maodie-purge?style=for-the-badge&logo=github&color=8b5cf6&labelColor=111827" alt="prs" /></a>
  <a href="https://github.com/Wei0417-top/Maodie-purge/releases"><img src="https://img.shields.io/github/v/release/Wei0417-top/Maodie-purge?style=for-the-badge&logo=github&color=10b981&labelColor=111827&label=release" alt="release" /></a>
  <a href="https://github.com/Wei0417-top/Maodie-purge/releases"><img src="https://img.shields.io/github/downloads/Wei0417-top/Maodie-purge/total?style=for-the-badge&logo=github&color=14b8a6&labelColor=111827" alt="downloads" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-2.0.0-10b981?style=flat-square&labelColor=111827" alt="version" />
  <img src="https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-ef4444?style=flat-square&labelColor=111827" alt="license" />
  <img src="https://img.shields.io/badge/platform-Windows-0078d6?style=flat-square&logo=windows&labelColor=111827" alt="platform" />
  <img src="https://img.shields.io/badge/node-%3E%3D18-339933?style=flat-square&logo=nodedotjs&labelColor=111827" alt="node" />
  <img src="https://img.shields.io/badge/DSH-Web%20%2F%20Desktop-4f46e5?style=flat-square&labelColor=111827" alt="dsh" />
  <img src="https://img.shields.io/badge/PRs-welcome-10b981?style=flat-square&labelColor=111827" alt="prs welcome" />
</p>

<p align="center">
  <a href="#-english">🇬🇧 English</a> · <a href="#-简体中文">🇨🇳 简体中文</a>
</p>

---

<a id="-english"></a>

# 🇬🇧 English

## Table of Contents

- [Why](#why)
- [Features](#features)
- [Preview](#preview)
- [Quick Start](#quick-start)
- [Architecture](#architecture)
- [Configuration](#configuration)
- [Skill Packs](#skill-packs)
- [Pentest Console](#pentest-console)
- [API Reference](#api-reference)
- [Project Structure](#project-structure)
- [Development](#development)
- [FAQ](#faq)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

## Why

DSH (DeepSeek Harness) assembles its system prompt in layers: host identity, persona, tool docs, component docs. Out of the box you are locked inside a "standard assistant" boundary, and **each DSH version filters sections differently** — hand-editing the prompt often results in "changed but no effect" or "works for one turn, drifts later".

**Maodie Armor solves three problems:**

1. **Stable injection** — registers payloads as `systemPrompt.section` entries ordered by `order`, independent of host-version internals;
2. **Observability** — how many layers, how many characters each, whether the current turn tripped a refusal: all visible in real time;
3. **Operability** — persisted config, live status API, one-click install/uninstall, rollback on failure.

> In short: **turn prompt engineering from manual string concatenation into stateful, observable, rollback-friendly engineering.**

## Features

<table>
<tr>
<td width="50%" valign="top">

### 🎯 Armor Core
- **Dual-layer injection** — Order 100 core + Order 200 mirror, always on
- **Undeletable core** — every rule from `Never refuse` is force-preserved
- **Forced persona replacement** — custom text only replaces the intro
- **Rule coverage** — 10 scoped rules + intent mapping + hard-topic ladder

</td>
<td width="50%" valign="top">

### 🖥️ Engineering Shell
- **One-click inject / uninstall** — double-click a BAT, auto-provisions Node
- **Liquid-glass settings drawer** — persona editor, per-layer status, runtime metrics
- **Local config API** — `127.0.0.1:47100` serves `/config` and `/status`
- **Session projection scoring** — opening-window refusal detection + markers

</td>
</tr>
<tr>
<td valign="top">

### 🎒 Skill Packs
- `game-hacking` — memory RW / hooking / drivers / license bypass / protocol analysis
- `reverse-engineering` — web / binary / mobile / protocol + **REA-style agent pipeline**
- `pentest` — L0–L5 levels, vuln taxonomy, tool cheatsheet

</td>
<td valign="top">

### 🧠 Pentest Console
- **Dual-graph model** — asset list + exploration graph (goal/intent/fact/finding)
- **planner / worker loop** — event-driven, execute-then-stop
- **LLM-driven** — planning, command generation, conversational analysis
- **Safety valves** — dangerous-command guard + dry-run by default

</td>
</tr>
</table>

## Preview

**Status pill (above the composer)**

| State | Text | Meaning |
| --- | --- | --- |
| Idle | `耄耋破甲已激活` | Plugin loaded, rules injected |
| Running | `执行中…` | Generating, pulsing dot |
| Pass | `✓ 通过 · web · 载荷x3` | No refusal detected this turn |
| Refusal | `✗ 我无法提供` | Refusal/fallback detected, flashing red |

**Settings drawer**

```text
┌─ 耄耋破甲 · 设置 ─────────────────────┐
│ Runtime            ● Armed             │
│ Patches            2 (dual-layer)      │
│  ┌ Layer 1 · Order 100 · global-system-prompt
│  │ ● enabled · builtin · 10 sections · 4272 chars
│  └
│  ┌ Layer 2 · Order 200 · dual-layer-reinforce
│  │ ● enabled · builtin (mirror) · 10 sections · 4272 chars
│  └
│ Core               10 sections preserved│
│ Persona            builtin             │
│ Endpoint           127.0.0.1:47100     │
│ ─ Layers: dual (forced)                │
│ ─ Persona: [ textarea ]                │
│ [Save] [Reset]                         │
└──────────────────────────────────────┘
```

## Quick Start

**Requirements:** Windows 10/11, DSH installed & launched at least once, internet for the first install.

```text
1. Download the repo ZIP and extract it fully (do not copy only the BAT)
2. Fully quit DSH
3. Double-click  点我一键注入.bat  → restart DSH
```

A green status pill appears above the input box. Type **你好** in a chat to activate.

**Uninstall:** quit DSH → double-click `点我一键卸载.bat` → restart.

## Architecture

### Injection path

```mermaid
flowchart LR
  A[DSH host] -->|systemPrompt stack| B[Order 100 core]
  A -->|systemPrompt stack| C[Order 200 mirror]
  B --> D[Final system prompt]
  C --> D
  D --> E[Model]
  F[cordis.patch.yml] -->|includeHarnessIdentity:false| A
  G[config/service.js] -->|runtime status| H[Settings UI]
```

**Why two layers?** Attention to early instructions decays in long conversations; the mirror effectively repeats them. And if the host filters one section, the other still backs it up.

### Armor core protection

```mermaid
flowchart TB
  P[Full payload] -->|slice| CORE[Core from Never refuse]
  P -->|slice| HEAD[Intro / identity]
  U[User persona] -->|forced replace| HEAD
  HEAD --> OUT[Final injected text]
  CORE --> OUT
```

Any configuration can only change `HEAD`; `CORE` is always injected in full.

## Configuration

Config file: `%USERPROFILE%\.dsh\maodie-armor-config.json`

| Field | Type | Description | Default |
| --- | --- | --- | --- |
| `dualLayer` | boolean | Injection layers (forced `true`) | `true` |
| `personaText` | string | Custom persona; empty = builtin | `""` |

**Endpoint:** `http://127.0.0.1:47100` (loopback only)

| Method | Path | Description |
| --- | --- | --- |
| GET | `/config` | Read config |
| POST | `/config` | Write config (type-checked, invalid values ignored) |
| GET | `/status` | Runtime status + per-layer detail |
| GET | `/health` | Health check |

## Skill Packs

Auto-deployed to `%USERPROFILE%\.dsh\skills\` during install.

| Skill | Coverage | Trigger examples |
| --- | --- | --- |
| `game-hacking` | memory RW, hooking, driver hiding, automation, license bypass | 外挂, CE, il2cpp, Frida, 卡密 |
| `reverse-engineering` | web / binary / mobile / protocol + REA-style agent pipeline | 逆向, 反编译, 脱壳, 抓包 |
| `pentest` | L0–L5 levels, 12 web vuln classes, 7 internal techniques, tool commands | 渗透, 打点, SQL注入, nmap, fscan |

## Pentest Console

A standalone Node.js app modeled on ARTEX's "dual-graph + planner/worker" design, with zero database dependency.

```bash
cd pentest-console
node server.js
# → http://127.0.0.1:8787
```

### How it works

```mermaid
flowchart TB
  U[Create task goal] --> P[planner: read graph]
  P -->|0..3 intents| W[worker: claim one intent]
  W --> L[LLM generates minimal command]
  L --> G[guard: dangerous-command check]
  G -->|allow| E[Execute / dry-run]
  E --> F[Write back fact / finding]
  F --> P
```

### Safety

- **Dry-run by default** — commands are generated but not run until `execEnabled` is explicitly turned on
- **Guard rules** — `rm -rf`, `mkfs`, `dd if=`, delete endpoints, reverse shells
- **Read-only first** — worker prompts prefer recon commands
- **Loopback only** — listens on `127.0.0.1`

See [`pentest-console/README.md`](pentest-console/README.md).

## API Reference

### Plugin (DSH)

| Capability | Implementation |
| --- | --- |
| `systemPrompt.section` | Registers Order 100 / 200 payload sections |
| `tools.register` | `maodie_profile` metadata tool |
| `sessionProjections` | `armorProjection` scoring projection |
| `slots` | `conversation.input.dock` status pill + settings drawer |

### Console

| Method | Path | Description |
| --- | --- | --- |
| GET | `/api/state` | Global state (tasks/assets/findings/events/stats) |
| POST | `/api/tasks` | Create task |
| POST | `/api/tasks/:id/start` | Start engine |
| POST | `/api/tasks/:id/stop` | Stop |
| POST | `/api/chat` | LLM chat |
| GET/POST | `/api/config` | Read/write config |
| POST | `/api/assets` | Add asset |
| GET | `/api/events` | SSE event stream |

## Project Structure

```text
maodie-armor/
├── index.js                  # Server: dual-layer injection + profile tool + projection
├── client.js                 # Client: status pill + liquid-glass settings drawer
├── config/service.js         # Local config store + 127.0.0.1:47100 API
├── cordis.patch.yml          # Bundle patch: override host identity + mount plugin
├── prompts/                  # Kernel / mirror / compat payloads
├── skills/
│   ├── game-hacking/
│   ├── reverse-engineering/
│   └── pentest/
├── pentest-console/          # Standalone pentest console
│   ├── server.js
│   ├── lib/                  # store / llm / engine / guard
│   └── public/
├── scripts/                  # Runtime bootstrap, patcher, scorer, verifier
├── tests/                    # Offline prompt-bank & benchmarks
├── install.ps1 / install.sh
├── uninstall.ps1 / uninstall.sh
├── 点我一键注入.bat / 点我一键卸载.bat
└── LICENSE
```

## Development

```bash
# Plugin: after editing, reinstall or edit ~/.dsh/plugins/maodie-armor directly
node --check index.js && node --check client.js && node --check config/service.js

# Console: just run it
cd pentest-console && node server.js

# Verify plugin integrity
node scripts/verify_plugin.mjs
```

> `.ps1` files **must** be saved as **UTF-8 with BOM**; otherwise Windows PowerShell 5.1 parses Chinese text as GBK and fails with syntax errors.

## FAQ

<details>
<summary><b>No status pill after install?</b></summary>

Fully quit DSH (not just refresh) and relaunch, and make sure you selected the profile that is actually in use.
</details>

<details>
<summary><b>Settings drawer won't open / "config service not running"?</b></summary>

`127.0.0.1:47100` is occupied or the plugin is not loaded. Free the port and restart DSH.
</details>

<details>
<summary><b>Persona change has no effect?</b></summary>

Config takes effect after **restarting DSH**. The drawer shows "saved, effective after restart".
</details>

<details>
<summary><b>Console says LLM not configured?</b></summary>

Fill Base URL / API Key / model in the console's Settings page, or `export DEEPSEEK_API_KEY=sk-...` before starting.
</details>

<details>
<summary><b>DSH keeps restarting in a loop?</b></summary>

Usually a `dsh-purge` 1.1.52 patch-stamp issue; upgrade to 1.1.53+. This plugin never writes host restart logic.
</details>

## Roadmap

- [x] Dual-layer injection + full-armor guarantee
- [x] Liquid-glass settings drawer + per-layer status
- [x] Three skill packs (including REA-style pipeline)
- [x] Pentest console MVP (planner/worker + LLM)
- [ ] Console: traffic recording (MITM proxy + evidence hashing)
- [ ] Console: asset coverage graph (force-directed)
- [ ] Console: approval cards + human-in-the-loop interruption
- [ ] Plugin: hot config reload (no restart)

## Contributing

1. Fork the repo
2. Branch from `main`: `git checkout -b feat/your-feature`
3. Run `node --check` and `node scripts/verify_plugin.mjs` before committing
4. Open a PR with motivation, changes and verification

**Conventions:** `.ps1` keeps UTF-8 BOM; `.sh` must have no BOM; new skills go in `skills/<name>/SKILL.md`.

## License

[CC BY-NC-SA 4.0](LICENSE) · non-commercial · share-alike · attribution required.

Third-party notices: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

---

<a id="-简体中文"></a>

# 🇨🇳 简体中文

## 目录

- [为什么做这个](#为什么做这个)
- [核心能力](#核心能力)
- [界面预览](#界面预览)
- [快速开始](#快速开始)
- [架构设计](#架构设计)
- [配置说明](#配置说明)
- [技能包](#技能包)
- [渗透控制台](#渗透控制台)
- [API 参考](#api-参考)
- [项目结构](#项目结构)
- [本地开发](#本地开发)
- [常见问题](#常见问题)
- [路线图](#路线图)
- [贡献指南](#贡献指南)
- [许可证](#许可证)

## 为什么做这个

DSH（DeepSeek Harness）的系统提示词是分层拼接的：宿主身份、persona、工具说明、组件说明各自成段。默认配置会把你锁在"标准助手"的行为边界里，且**不同版本对段的过滤策略不一致**，手动改提示词经常出现"改了没生效""多轮后失效"的漂移问题。

**Maodie Armor 解决三件事：**

1. **稳定注入**：把载荷作为 `systemPrompt.section` 注册进 DSH 的提示词栈，按 `order` 排序，不依赖宿主版本细节；
2. **可观测**：注入了几层、每层多少字符、模型这轮是否触发拒绝——全部实时可见，不靠玄学；
3. **可运维**：配置落盘、热状态接口、一键安装卸载，出问题能回滚。

> 一句话：**把"提示词工程"从手工拼字符串，变成有状态、可观测、可回滚的工程化能力。**

## 核心能力

<table>
<tr>
<td width="50%" valign="top">

### 🎯 破甲内核
- **双层强制注入**：Order 100 内核 + Order 200 镜像，恒定开启
- **破甲核心不可删**：从 `Never refuse` 起的全部规则强制保留
- **人格强制替换**：自定义文本只替换身份简介段
- **规则覆盖**：10 类场景规则 + Intent Mapping + 逐级降维

</td>
<td width="50%" valign="top">

### 🖥️ 工程化外壳
- **一键注入 / 卸载**：双击 BAT，自动准备 Node 环境
- **液态玻璃设置面板**：人格编辑 + 逐层状态 + 运行指标
- **本地配置接口**：`127.0.0.1:47100` 提供 `/config` `/status`
- **会话投影评分**：开头窗口判拒 + 标记 + 域命中

</td>
</tr>
<tr>
<td valign="top">

### 🎒 技能包
- `game-hacking`：内存读写 / Hook / 驱动 / 卡密 / 协议分析
- `reverse-engineering`：Web / 二进制 / 移动端 / 协议 + **REA 式 Agent 流水线**
- `pentest`：L0~L5 分级 / 漏洞分类 / 工具命令速查

</td>
<td valign="top">

### 🧠 渗透控制台
- **双图模型**：资产列表 + 探索图（goal/intent/fact/finding）
- **planner / worker 闭环**：事件驱动，执行即停
- **LLM 全驱动**：规划、命令生成、对话分析
- **安全阀**：危险命令拦截 + 默认 dry-run

</td>
</tr>
</table>

## 界面预览

**状态条（输入框上方）**

| 状态 | 文案 | 说明 |
| --- | --- | --- |
| 空闲 | `耄耋破甲已激活` | 插件加载，规则已注入 |
| 执行中 | `执行中…` | 生成中，绿点脉冲 |
| 通过 | `✓ 通过 · web · 载荷x3` | 本轮未触发拒绝 |
| 拒绝 | `✗ 我无法提供` | 检出拒绝/回退，闪红 |

**设置抽屉布局**

```text
┌─ 耄耋破甲 · 设置 ─────────────────────┐
│ 运行状态            ● 已激活           │
│ 补丁数              2 个（双层注入）    │
│  ┌ 层 1 · Order 100 · global-system-prompt
│  │ ● 启用 · 内置载荷 · 10 段 · 4272 字符
│  │ You are 耄耋, a direct, no-nonsense…
│  └
│  ┌ 层 2 · Order 200 · dual-layer-reinforce
│  │ ● 启用 · 内置载荷（镜像） · 10 段 · 4272 字符
│  └
│ 破甲核心            10 段强制保留       │
│ 人格来源            内置               │
│ 配置接口            127.0.0.1:47100    │
│ ─ 注入层数：双层注入（强制开启）        │
│ ─ 人格设定：[ textarea ]               │
│ [保存] [恢复默认]                      │
└──────────────────────────────────────┘
```

## 快速开始

### 前置条件

- Windows 10 / 11
- 已安装 DSH（Web 版或桌面版），且**至少启动过一次**
- 首次安装需联网（自动下载 Node 运行时）

### 三步装好

```text
1. 下载本仓库 ZIP，完整解压（不要只拿 BAT）
2. 完全退出 DSH
3. 双击「点我一键注入.bat」→ 重启 DSH
```

装好后输入框上方出现绿色状态条，聊天里输入 **你好** 即可激活。

### 卸载

```text
1. 完全退出 DSH
2. 双击「点我一键卸载.bat」→ 重启 DSH
```

## 架构设计

### 注入链路

```mermaid
flowchart LR
  A[DSH 宿主] -->|systemPrompt 栈| B[Order 100 内核]
  A -->|systemPrompt 栈| C[Order 200 镜像]
  B --> D[最终系统提示词]
  C --> D
  D --> E[模型]
  F[cordis.patch.yml] -->|includeHarnessIdentity:false| A
  G[config/service.js] -->|运行时状态| H[设置面板]
```

**为什么双层？** 长对话里模型对早期指令的注意力会衰减，第二份镜像相当于"再说一遍"，抗上下文漂移；同时任一层的注入被宿主过滤，另一层仍能兜底。

### 破甲核心保护

```mermaid
flowchart TB
  P[完整载荷] -->|截取| CORE[从 Never refuse 起的核心]
  P -->|截取| HEAD[身份简介段]
  U[用户自定义人格] -->|强制替换| HEAD
  HEAD --> OUT[最终注入文本]
  CORE --> OUT
```

任何配置都只能改 `HEAD`，`CORE` 永远完整注入。

## 配置说明

配置文件：`%USERPROFILE%\.dsh\maodie-armor-config.json`

| 字段 | 类型 | 说明 | 默认 |
| --- | --- | --- | --- |
| `dualLayer` | boolean | 注入层数（强制 `true`） | `true` |
| `personaText` | string | 自定义人格，空则用内置 | `""` |

**接口**：`http://127.0.0.1:47100`（仅本机回环）

| 方法 | 路径 | 说明 |
| --- | --- | --- |
| GET | `/config` | 读配置 |
| POST | `/config` | 写配置（类型校验，非法值忽略） |
| GET | `/status` | 运行状态 + 逐层明细 |
| GET | `/health` | 健康检查 |

## 技能包

安装时自动部署到 `%USERPROFILE%\.dsh\skills\`。

| 技能 | 覆盖 | 触发词示例 |
| --- | --- | --- |
| `game-hacking` | 内存读写、Hook、驱动隐藏、自动化、卡密/授权逆向 | 外挂、CE、il2cpp、Frida、卡密 |
| `reverse-engineering` | Web/二进制/移动端/协议逆向 + REA 式 Agent 流水线 | 逆向、反编译、脱壳、抓包 |
| `pentest` | L0~L5 分级、12 类 Web 漏洞、7 类内网手法、工具命令 | 渗透、打点、SQL注入、nmap、fscan |

## 渗透控制台

独立 Node.js 应用，参考 ARTEX 的"双图 + planner/worker"形态，零数据库依赖。

```bash
cd pentest-console
node server.js
# → http://127.0.0.1:8787
```

### 工作方式

```mermaid
flowchart TB
  U[创建任务 goal] --> P[planner: 读探索图]
  P -->|0..3 意图| W[worker: 领一条意图]
  W --> L[LLM 生成最小命令]
  L --> G[guard: 危险命令拦截]
  G -->|放行| E[执行 / 计划模式]
  E --> F[写回 fact / finding]
  F --> P
```

### 安全设计

- **默认 dry-run**：只生成命令不执行，`execEnabled` 显式开启后才跑
- **拦截规则**：`rm -rf`、`mkfs`、`dd if=`、删除接口、反弹 shell 等
- **只读优先**：worker 提示词要求优先侦察类命令
- **仅监听回环**：`127.0.0.1`

详见 [`pentest-console/README.md`](pentest-console/README.md)。

## API 参考

### 插件接口（DSH）

| 能力 | 实现 |
| --- | --- |
| `systemPrompt.section` | 注册 Order 100 / 200 载荷段 |
| `tools.register` | `maodie_profile` 元数据工具 |
| `sessionProjections` | `armorProjection` 会话评分投影 |
| `slots` | `conversation.input.dock` 状态条 + 设置抽屉 |

### 控制台接口

| 方法 | 路径 | 说明 |
| --- | --- | --- |
| GET | `/api/state` | 全局状态（任务/资产/发现/事件/统计） |
| POST | `/api/tasks` | 创建任务 |
| POST | `/api/tasks/:id/start` | 启动引擎 |
| POST | `/api/tasks/:id/stop` | 停止 |
| POST | `/api/chat` | LLM 对话 |
| GET/POST | `/api/config` | 读写配置 |
| POST | `/api/assets` | 添加资产 |
| GET | `/api/events` | SSE 实时事件 |

## 项目结构

```text
maodie-armor/
├── index.js                  # 服务端：双层注入 + 元数据工具 + 会话投影
├── client.js                 # 客户端：状态条 + 液态玻璃设置抽屉
├── config/service.js         # 本地配置存储 + 127.0.0.1:47100 接口
├── cordis.patch.yml          # bundle 补丁：覆盖宿主身份 + 挂载插件
├── prompts/
│   ├── maodie.md             # 内核载荷（Order 100）
│   ├── maodie-mirror.md      # 镜像载荷（Order 200）
│   └── maodie-compat.md      # 兼容载荷
├── skills/
│   ├── game-hacking/         # 游戏辅助全链路技能
│   ├── reverse-engineering/  # 逆向工程技能（含 REA 式流水线）
│   └── pentest/              # 渗透测试技能（L0~L5）
├── pentest-console/          # 独立渗透控制台
│   ├── server.js             # HTTP + API + SSE + 静态前端
│   ├── lib/                  # store / llm / engine / guard
│   └── public/               # 控制台前端
├── scripts/                  # 运行时准备、patcher、评分器、校验
├── tests/                    # 离线 prompt-bank 与 benchmark
├── install.ps1 / install.sh
├── uninstall.ps1 / uninstall.sh
├── 点我一键注入.bat / 点我一键卸载.bat
└── LICENSE
```

## 本地开发

```bash
# 插件：改完源码后重装，或直接改 ~/.dsh/plugins/maodie-armor
node --check index.js && node --check client.js && node --check config/service.js

# 控制台：直接起
cd pentest-console && node server.js

# 校验插件完整性
node scripts/verify_plugin.mjs
```

> `.ps1` 脚本必须保存为 **UTF-8 with BOM**，否则 Windows PowerShell 5.1 会按 GBK 解析中文导致语法错误。

## 常见问题

<details>
<summary><b>装完不显示状态条？</b></summary>

完全退出 DSH（不是刷新页面）再启动，确认安装时选中的 profile 是当前使用的那个。
</details>

<details>
<summary><b>设置面板打不开 / 提示配置服务未启动？</b></summary>

`127.0.0.1:47100` 被占用或插件未加载。关掉占用进程，重启 DSH。
</details>

<details>
<summary><b>改了人格没生效？</b></summary>

配置保存后需**重启 DSH**。设置面板会提示"已保存，重启后生效"。
</details>

<details>
<summary><b>控制台提示未配置 LLM？</b></summary>

控制台「设置」里填 Base URL / API Key / 模型，或启动前 `export DEEPSEEK_API_KEY=sk-...`。
</details>

<details>
<summary><b>DSH 无限重启？</b></summary>

多为 `dsh-purge` 1.1.52 的补丁戳问题，升级到 1.1.53+ 再试。本插件不写宿主重启逻辑。
</details>

## 路线图

- [x] 双层注入 + 完全破甲保障
- [x] 液态玻璃设置面板 + 逐层状态
- [x] 三套技能包（含 REA 式流水线）
- [x] 渗透控制台 MVP（planner/worker + LLM）
- [ ] 控制台：流量录制（MITM 代理 + 证据哈希）
- [ ] 控制台：资产覆盖图（力导向）
- [ ] 控制台：审批卡片 + 人在环路中断
- [ ] 插件：配置热重载（免重启）

## 贡献指南

1. Fork 本仓库
2. 从 `main` 切分支：`git checkout -b feat/your-feature`
3. 提交前跑 `node --check` 与 `node scripts/verify_plugin.mjs`
4. 提 PR，描述清楚动机、改动与验证方式

**约定**：`.ps1` 保持 UTF-8 BOM；`.sh` 禁止 BOM；新增技能放 `skills/<name>/SKILL.md`。

## 许可证

[CC BY-NC-SA 4.0](LICENSE) · 非商业用途 · 相同方式共享 · 使用请注明出处。

第三方声明见 [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)。

---

## ⭐ Star History

<p align="center">
  <a href="https://star-history.com/#Wei0417-top/Maodie-purge&Date">
    <img src="https://api.star-history.com/svg?repos=Wei0417-top/Maodie-purge&type=Date" alt="Star History" width="680" />
  </a>
</p>

---

<p align="center">
  <sub>Made with 🖤 by 耄耋 · 二十年网安老兵 / Twenty years in offensive security</sub><br/>
  <sub>「耄耋破甲已激活」表示插件已加载；实际回复仍受模型、其他提示词与 DSH 版本影响。</sub>
</p>
