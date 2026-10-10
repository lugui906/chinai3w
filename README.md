# ChinAI3 · Windows 版

常驻桌面的 AI 助手 —— **会聊天，更会帮你动手**。

本仓库是 ChinAI3 Windows 版的**单文件落地页**（GitHub Pages 主页）：
`index.html` 内联全部样式与脚本、图标以 base64 内嵌，不依赖任何外部资源。

- 在线访问：<https://lugui906.github.io/chinai3w/>
- 下载：见 [Releases](https://github.com/lugui906/chinai3w/releases)

## 它能帮你做什么

**四个开箱即用的 AI 应用**

| 应用 | 作用 |
|---|---|
| 💬 AI 助手 | 通用对话：搜索、答疑、写作、分析文档；支持上传任意文件让它读取 |
| 🖥️ 桌面控制 | 一句话让 AI 操作电脑：开应用、点按钮、填表单、截图排障 |
| 🤖 自动化 | 把口头描述变成可执行的脚本 / 规则并跑起来 |
| 🗓️ 日程 | 自然语言安排当天任务；每天定点 / Cron / 打开某应用时触发，到点自动执行 |

**更多能力**

- 👀 截图提问 + 认字：一键截屏识别文字，直接随问题发给 AI
- 🧭 读取界面上下文：让 AI 先“看到”当前界面再回答或动手
- 🔊 一键朗读：任意回复可读出来、可停止
- 🧠 AI 记忆：记住你的习惯、职业、常用软件，可每天/每周/每月/每季自动更新
- 🗂️ 活动记录：窗口日志 + 最近文件作为上下文，可选最近 5 分钟到一整天
- 🎛️ 模型随你挑：自动检测可用模型并记住选择，多厂商一键接入
- 🔑 API Key 管理：添加 / 查看（脱敏）/ 删除，只保存在本机
- 🗨️ 多会话管理、🔍 历史搜索与收藏、🧩 系统 AI 应用一览

## 安装（Windows 10 / 11 · 64 位）

1. 下载 `chinai3-1.0.0-x64.msi`，双击按提示安装（**免管理员**）。
2. 启动后到「设置 → 模型 / API Key」填好 Key，即可开始对话。

也可以下载免安装包 `chinai3-win-1.0.0.zip`，解压后直接运行。

> 安装包体积较大（>100 MB），超过 GitHub 单文件 100 MB 限制，因此不放进仓库，
> 统一发布到 **Releases**；页面上的下载按钮指向 `releases/latest`。

## 本地预览

```bash
python3 -m http.server 8080   # 打开 http://localhost:8080
```

直接双击 `index.html` 也可以（纯静态、无外部请求）。

## 发布到 GitHub Pages

1. 推送到 `main`；
2. 仓库 **Settings → Pages** → Source 选 `Deploy from a branch` → `main` / `/(root)`；
3. 访问 <https://lugui906.github.io/chinai3w/>。

---

同系列：<https://lugui906.github.io/chin>（TSAI-OS 官网） · <https://lugui906.github.io/tsai>（TSAI-AI · AI 应用集合）
