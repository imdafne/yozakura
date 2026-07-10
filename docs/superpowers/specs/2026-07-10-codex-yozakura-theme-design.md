# Codex Yozakura 主题设计

## 目标

将 Yozakura 的 Ghostty 深色夜樱配色适配为可导入 Codex Desktop 的深色界面主题。

## 范围

- 新增 Codex 主题目录和可读的主题定义文件
- 生成可直接粘贴到 Codex 导入主题窗口的 `codex-theme-v1` 字符串
- 在 README 中说明导入步骤和颜色映射

不修改 Ghostty 和 Obsidian 现有主题，也不改动用户的全局 Codex 配置。

## 配色映射

| Codex 语义 | 值 | Yozakura 来源 |
| --- | --- | --- |
| surface | `#1e1e2e` | 背景 |
| ink | `#cdd6f4` | 前景文字 |
| accent | `#f4b8e4` | 亮粉色 |
| diffAdded | `#81c8be` | 亮青绿 |
| diffRemoved | `#b69db8` | 柔和紫灰 |
| skill | `#cba6f7` | 紫色 |

主题对比度设为 `58`，窗口使用透明材质。代码高亮采用 Codex 自带的 `catppuccin` 预设。

## 产物

`codex/yozakura-dark.json` 保存无前缀的主题对象，便于审阅和复用。

`codex/yozakura-dark.txt` 保存 `codex-theme-v1:` 前缀的单行导入字符串。

README 增加导入路径和已知适配范围。

## 验证

1. 解析 JSON，确认包含完整必填字段。
2. 从 JSON 生成导入字符串，并确认前缀和 JSON 内容一致。
3. 使用 Codex Desktop 的导入主题窗口粘贴字符串，确认可导入。
