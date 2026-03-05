# Yozakura

Ghostty 视觉配置 + Claude Code 一键安装工具，包含主题、窗口、排版等 Ghostty 视觉配置及 Claude Code statusline。

## 安装

```bash
npx yozakura
```

交互选择要安装的配置组，直接回车全部安装。

跳过交互，全部安装：

```bash
npx yozakura --all
```

## 配置组

| # | 分组 | 说明 |
|---|------|------|
| 1 | 主题 | Yozakura (dark) + Sakura (light) 自动切换 |
| 2 | 窗口 | 毛玻璃 + 内边距 + tabs 标题栏 |
| 3 | 排版 | 字号、加粗、行高、CJK 字体、光标 |
| 4 | Claude Code | Tab 重命名快捷键 + Statusline |

## 工作原理

- 自动备份已有 `~/.config/ghostty/config`
- 智能合并：只修改选中的配置项，保留你的快捷键、shell 等个人设置
- 管理区块标记 `# --- yozakura (managed) ---`，重复运行安全更新
- 零依赖，仅用 Node.js 内置模块

## 前提

- macOS + [Ghostty](https://ghostty.org/) 已安装
- Node.js >= 16
- `jq`（Claude Code statusline 需要）：`brew install jq`
