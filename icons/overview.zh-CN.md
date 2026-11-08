---
title: 图标包开发
description: icon.json、目录位置与使用场景
---

图标包（Icon pack）将一套图标资源放在固定目录，由清单文件 **`icon.json`** 声明 `Package` 元数据。用户可在思源外观设置里选用（与内置方案并列）。

## 工作空间路径

`{工作空间}/data/icons/<包名>/`

与主题相同，第三方图标包位于 `data` 下，不在 `appearance` 内；内置 `litheness` 属于应用自带资源，位于 `{工作空间}/conf/appearance/icons/`。思源会扫描子目录并解析 `icon.json`，在设置中提供可选图标方案。

## 清单文件 icon.json

内置示例见 `app/appearance/icons/litheness/icon.json`：

```json
{
  "name": "litheness",
  "author": "Vanessa",
  "url": "https://github.com/Vanessa219",
  "version": "1.0.0"
}
```

与 `Package` 结构一致，可继续包含 **`minAppVersion`、`displayName`、`description`、`readme`、`funding`、`keywords`** 等字段，用于集市展示与搜索（见 [集市包总览](../bazaar/overview.zh-CN.md)）。

**没有** `modes` / `backends` / `frontends` 等主题或插件专有字段。

## 包内常见内容

除 `icon.json` 外，**必须**提供 **`icon.js`**（用 `<symbol id="...">` 定义各图标）；缺少 `icon.js` 的目录会被内核直接跳过，设置里不会出现该图标方案（内置 `litheness` 同样只有 `icon.json`、`icon.js` 与许可证文件）。其余图标资源的具体格式与命名需与内置图标包或官方示例保持一致。上架 zip 通常还要求 **`icon.png`、`preview.png`、`README.md`** 等，以集市当前校验为准。

## 与表情/资源的关系

设置里切换「图标方案」会走外观配置；若你仅想为笔记内容插入表情，可能属于另一条能力（`data/emojis` 等），与「图标包」不是同一套机制，开发前请确认产品需求。

## 下一步

- [icon.json 字段说明](./manifest.zh-CN.md)
