---
title: Home
description: Entry point for SiYuan plugin, marketplace package, and theme authors
---

This handbook is for developers who extend **SiYuan** with **plugins, themes, icon packs, template packs, or widgets**, or who need the **local HTTP API** (see [`docs/API.md`](https://github.com/siyuan-note/siyuan/blob/master/docs/API.md) in the official repo). Pages use clear headings, tabular field descriptions, and runnable examples where possible.

Sources: the **SiYuan open-source repo** and the **official plugin-sample**; if marketplace indexing or publishing changes, follow official announcements.

---

## Doc map

### Introduction

| Page | Description |
| --- | --- |
| [How to read and contribute](./intro/docs-style.zh-CN.md) | Conventions and chapter structure |
| [Marketplace packages overview](./bazaar/overview.en.md) | **Five** package types, paths, shared `Package` fields |
| [Publishing and versions](./bazaar/publishing.zh-CN.md) | `package.zip`, GitHub Release, listing notes |

### Plugins (Petal)

| Page | Description |
| --- | --- |
| [Plugin development overview](./plugin/overview.en.md) | Runtime, `index.js` load chain, lifecycle |
| [Quick start](./plugin/quickstart.zh-CN.md) | Template repo, `pnpm`, local debugging |
| [plugin.json](./plugin/manifest.zh-CN.md) | Manifest and environment fields |
| [Frontend Plugin API](./plugin/frontend-api.zh-CN.md) | `Plugin` class, commands, Dock, storage, `fetchPost` |
| [HTTP API and data rules](./plugin/http-api.zh-CN.md) | HTTP, auth, `/api/file/*`, daily note attributes |
| [Debugging](./plugin/debugging.zh-CN.md) | Console, common errors |
| [Events reference](./plugin/events.zh-CN.md) | **`TEventBus`** event tables |
| [Packaging and publishing](./plugin/packaging.zh-CN.md) | zip, Release |

### Themes

| Page | Description |
| --- | --- |
| [Theme overview](./theme/overview.en.md) | `data/themes`, vs plugins |
| [theme.json](./theme/manifest.zh-CN.md) | `modes`, manifest fields |
| [Styling and CSS variables](./theme/styling.zh-CN.md) | `--b3-*` variables and customization |

### Icon packs · Templates · Widgets

| Page | Description |
| --- | --- |
| [Icon packs](./icons/overview.en.md) | `data/icons`, `icon.json` |
| [Template packs](./templates/overview.en.md) | `data/templates`, `/api/template/render` |
| [Template syntax](./templates/authoring.zh-CN.md) | `.action{}` Go templates |
| [Widgets](./widgets/overview.en.md) | `data/widgets`, `/widgets/` iframe |

---

## Official repos quick reference

| Resource | Link |
| --- | --- |
| SiYuan main app source | [github.com/siyuan-note/siyuan](https://github.com/siyuan-note/siyuan) |
| HTTP API manual | [docs/API.md](https://github.com/siyuan-note/siyuan/blob/master/docs/API.md) · [docs/API.zh-CN.md](https://github.com/siyuan-note/siyuan/blob/master/docs/API.zh-CN.md) |
| Official plugin sample | [github.com/siyuan-note/plugin-sample](https://github.com/siyuan-note/plugin-sample) |
| npm `siyuan` (types and exports) | Match the SiYuan version you target; see the sample `package.json` |

---

## Source anchors (handy when debugging)

Paths below are in the main SiYuan repo:

| Topic | Path |
| --- | --- |
| `Plugin` base class | `app/src/plugin/index.ts` |
| Plugin loading | `app/src/plugin/loader.ts` |
| Marketplace `Package` model | Go structs aligned with manifest JSON (see the open-source repo) |

---

## Other languages

Chinese pages sit next to their English counterparts in the same folders (for example `plugin/overview.zh-CN.md` beside `plugin/overview.en.md`), with the language in the filename suffix. Today only some pages have an English edition; see [`nav.yml`](nav.yml) and the `*.en.md` files in each folder.
