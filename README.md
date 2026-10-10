# ChinAI3 · Windows 版

本仓库是 **ChinAI3 Windows 版** 的单文件下载落地页（GitHub Pages 主页）。

- 页面：`index.html` —— **单文件**，内联 CSS / JS，图标为 base64 内嵌，不依赖任何外部资源。
- 下载：见 [Releases](https://github.com/lugui906/chinai3w/releases)。

## 关于 ChinAI3 Windows 版

把 TSAI-OS 上的 ChinAI3 移植到 Windows：

| 部分 | Linux 版 | Windows 版 |
|---|---|---|
| 图形外壳 | GTK4 + WebKit6 | **Edge WebView2**（pywebview） |
| 界面 | Flask Web UI | **完全复用同一套** |
| 后端 | `server.py` / `backends.py` / `chindshell` | **同一套** + Windows 分支 |
| AI 引擎 | `aim` | **`aim.exe`**（Go 交叉编译） |
| 引擎依赖 | `opencode2` | `opencode2`（随包内嵌 Node + opencode） |

特性：内置 Node 运行时与 opencode v2（装完即用）、离线安装包、免管理员 MSI、
模型 / API Key 管理、截图提问、活动记录、桌面控制。

## 本地预览

```bash
python3 -m http.server 8080
# 打开 http://localhost:8080
```

直接双击 `index.html` 也可以（纯静态、无外部请求）。

## 发布到 GitHub Pages

1. 推送本仓库到 `main` 分支；
2. 仓库 **Settings → Pages** → Source 选 `Deploy from a branch` → `main` / `/(root)`；
3. 访问 <https://lugui906.github.io/chinai3w/>。

## 发行物

| 文件 | 说明 |
|---|---|
| `chinai3-1.0.0-x64.msi` | MSI 安装包（WiX 构建，按用户安装到 `%LOCALAPPDATA%\Programs\ChinAI3`） |
| `chinai3-win-1.0.0.zip` | 免安装包（自带嵌入式 Python 3.12 与依赖 wheel） |

> 安装包体积较大（>100 MB），GitHub 单文件限制 100 MB，因此不放在仓库里，
> 统一发布到 **Releases** 页；`index.html` 里的下载按钮指向 `releases/latest`。
