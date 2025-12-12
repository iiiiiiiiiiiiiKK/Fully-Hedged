<div align="center">
  <a href="https://x.com/0xkillcoin">
    <img src="https://img.shields.io/badge/CYBER.HEDGE-TERMINAL-00f3ff?style=for-the-badge&logo=probot&logoColor=black" alt="Logo">
  </a>

  <h1 align="center">Cyber Hedge Terminal</h1>

  <p align="center">
    <strong>极致的单文件加密货币对冲、解套与战术推演终端</strong>
    <br />
    <br />
    <a href="#-features">✨ 特性</a>
    ·
    <a href="#-quick-start">🚀 快速开始</a>
    ·
    <a href="#-usage-guide">📚 使用指南</a>
    ·
    <a href="#-privacy--security">🔒 隐私安全</a>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/version-v22.0-blue?style=flat-square" alt="Version">
    <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="License">
    <img src="https://img.shields.io/badge/platform-Web%20%7C%20Mobile-orange?style=flat-square" alt="Platform">
    <a href="https://x.com/0xkillcoin"><img src="https://img.shields.io/twitter/follow/0xkillcoin?style=social" alt="Twitter Follow"></a>
  </p>
</div>

---

## 📖 简介 (Introduction)

**Cyber Hedge Terminal** 是一个运行在浏览器端的**单文件 (Single-File)** 交易辅助工具。它专为从“天地锁”中突围的交易者设计，集成了实时风控、AI 视觉识别、智能策略推演和 Telegram 信号推送功能。

无需安装 Python 环境，无需配置后端服务器，下载即用，百分百保障 API Key 与隐私安全。

## ✨ 特性 (Features)

* **👁️ AI 视觉识别 (OCR)**：基于 `Tesseract.js`，支持直接上传/粘贴币安或 OKX 的持仓截图，自动解析多空仓位与均价。
* **⚡ 双路实时行情**：内置 **Binance** 和 **OKX** WebSocket 接口，毫秒级推送 50+ 热门币种价格。
* **🧠 战术推演沙盘 (Tactical Sim)**：
    * **模拟建仓**：输入目标点位与数量，实时计算**新均价**、**新强平价**与**新回本点**。
    * **动态策略**：自动生成基于斐波那契数列的支撑/阻力位矩阵，点击即可一键载入沙盘。
* **📊 核心风控仪表盘**：
    * 实时计算**净头寸 (Delta)**、**浮动盈亏 (PnL)** 与 **实时净值 (Equity)**。
    * **精准强平算法**：采用交易所标准的对冲维持保证金逻辑，拒绝虚假报警。
* **📡 Telegram 信号塔**：
    * 配置 Bot Token 后，可将实时行情简报推送到您的 TG 群组。
    * 内置 **CORS 中继**，解决纯前端无法调用 TG API 的问题。
* **🎨 赛博主题引擎**：
    * `Cyber Dark` (默认)：沉浸式霓虹黑。
    * `Tactical Light`：高亮日间模式，户外可视。
    * `Retro Pixel`：复古 8-bit 像素风，极客专属。

## 🚀 快速开始 (Quick Start)

### 方法一：直接运行
1.  下载本项目中的 `CyberHedgeTerminal_V22.html` 文件。
2.  双击使用 Chrome, Safari 或 Edge 浏览器打开。
3.  开始交易推演！

### 方法二：本地开发
```bash
# 克隆仓库
git clone [https://github.com/your-username/cyber-hedge-terminal.git](https://github.com/your-username/cyber-hedge-terminal.git)

# 进入目录
cd cyber-hedge-terminal

# 任何静态服务器均可运行 (例如 Python)
python3 -m http.server 8000
