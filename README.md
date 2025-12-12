# 📟 @oAdam TERMINAL V22

> **Next-Gen Crypto Risk Monitor & Tactical Simulator**
>
> 一个基于 Web 的单文件（Single-File）加密货币风控终端。集成了多空持仓管理、实时强平计算、策略沙盘推演以及 OCR 识别功能。无需后端，数据直连交易所 WebSocket。

![Version](https://img.shields.io/badge/Version-V22-00f3ff?style=flat-square)
![Build](https://img.shields.io/badge/Build-Single%20HTML-success?style=flat-square)
![Theme](https://img.shields.io/badge/Theme-Cyberpunk%20%7C%20Pixel-ff003c?style=flat-square)

---

## 📖 项目简介 (Introduction)

**@oAdam TERMINAL** 不仅仅是一个价格监视器，它是一个为高杠杆合约交易者设计的**辅助驾驶舱**。它解决了交易所原生界面信息过载的问题，专注于核心风控指标：**PNL (未结盈亏)**、**Equity (净值)** 和 **Delta (风险敞口)**。

[span_1](start_span)[span_2](start_span)系统通过 WebSocket 直接连接 Binance 或 OKX[span_1](end_span)[span_2](end_span)，在本地浏览器中实时计算复杂的双向持仓强平价格，并提供“What-If”沙盘模拟功能，帮助交易者在加仓前预知风险变化。

---

## ✨ 核心特性 (Features)

### 1. ⚡ 实时风控核心 (Core Monitor)
* **[span_3](start_span)[span_4](start_span)多源行情切换**：支持 **Binance** 和 **OKX** 实时 WebSocket 数据流，一键无缝切换[span_3](end_span)[span_4](end_span)。
* **智能风险计算**：
    * **[span_5](start_span)[span_6](start_span)动态强平 (Dynamic Liq)**：基于 MMR (1%) 模型，综合计算多空双向持仓后的强平点 [cite: 156-158]。
    * [cite_start]**风险进度条**：可视化展示当前价格距离强平点的安全缓冲区（Safe / Low / Critical）[span_5](end_span)[span_6](end_span)。
    * **[span_7](start_span)Delta 监控**：实时显示净多头或净空头敞口[span_7](end_span)。

### 2. 🛡️ 仓位与资产管理
* **[span_8](start_span)[span_9](start_span)双向持仓**：独立管理 Long (多) 和 Short (空) 的均价与数量[span_8](end_span)[span_9](end_span)。
* **[span_10](start_span)资金管理**：自定义钱包余额 (U) 与杠杆倍数 (Leverage)，实时联动计算净值[span_10](end_span)。
* **[span_11](start_span)[span_12](start_span)OCR 智能识别**：集成 `Tesseract.js`，支持上传持仓截图，自动识别价格与数量并填入系统[span_11](end_span)[span_12](end_span)。

### 3. ♟️ 战术沙盘 (Tactical Sim)
* **[span_13](start_span)[span_14](start_span)预演推算**：输入模拟价格和数量，立即预览加仓后的**新均价**和**新强平价** [cite: 118-122]。
* [cite_start]**策略矩阵 (Strategy Matrix)**：自动生成当前价格 ±1% ~ 5% 的支撑/阻力位，点击即可快速载入沙盘进行演练 [cite: 123, 179-181]。

### 4. 🤖 自动化与扩展
* [cite_start]**Telegram 机器人**：内置 TG 推送功能，支持发送包含 PnL、Equity、Delta 的实时简报[span_13](end_span)[span_14](end_span)。
* **[span_15](start_span)[span_16](start_span)CORS 代理支持**：解决浏览器端直接调用 Telegram API 的跨域问题[span_15](end_span)[span_16](end_span)。
* **多主题系统**：
    * [span_17](start_span)🌑 **Dark**: 赛博朋克深色模式（默认）[span_17](end_span)。
    * [span_18](start_span)☀️ **Light**: 高亮日间模式[span_18](end_span)。
    * [span_19](start_span)👾 **Pixel**: 复古 8-bit 像素模式[span_19](end_span)。

---

## 🛠️ 使用指南 (User Guide)

本终端采用单页应用设计，加载即用。以下是详细操作流程：

### 1. 基础设置 (Setup)
1.  **启动**：直接在浏览器打开 `index.html`。
2.  **[span_20](start_span)选择币种**：在右上角下拉菜单选择交易对（如 ETH, BTC, SOL 等）[span_20](end_span)。
3.  **配置资产**：
    * [span_21](start_span)在 **Wallet & Leverage** 面板中，输入你的当前 `钱包余额 (U)` 和 `杠杆倍数 (X)`[span_21](end_span)。

### 2. 录入持仓 (Positions)
你有两种方式录入当前的持仓数据：
* **[span_22](start_span)[span_23](start_span)手动模式**：在 **Positions** 面板，分别输入 `LONG` 和 `SHORT` 的 **均价** 和 **数量**[span_22](end_span)[span_23](end_span)。
* **OCR 自动模式**：
    1.  [span_24](start_span)点击底部 Dock 栏的 `📷 识别` 按钮[span_24](end_span)。
    2.  上传包含持仓信息的截图。
    3.  [span_25](start_span)系统将自动解析并在底部的 AI Log 中显示 "OCR Success"，数据会自动填充[span_25](end_span)。

### 3. 使用沙盘 (Simulation)
当你想加仓或通过对冲来移动强平价时：
1.  **[span_26](start_span)[span_27](start_span)手动模拟**：在 **TACTICAL SIM** 面板输入 `模拟价格` 和 `数量`（正数为多，负数为空）。观察下方的 `New AVG` 和 `New LIQ` 变化[span_26](end_span)[span_27](end_span)。
2.  **[span_28](start_span)策略加载**：查看 **STRATEGY MATRIX** 面板，点击任意一行（支撑或阻力位），系统会自动将该价格和预设数量填入沙盘[span_28](end_span)。

### 4. 配置 Telegram 推送
[span_29](start_span)[span_30](start_span)点击底部 Dock 栏的 `⚙️ TG` 按钮打开设置弹窗[span_29](end_span)[span_30](end_span)：
1.  **[span_31](start_span)Bot Token**：输入从 @BotFather 获取的 Token[span_31](end_span)。
2.  **[span_32](start_span)Chat ID**：输入接收消息的 User ID 或 Channel ID[span_32](end_span)。
3.  **[span_33](start_span)CORS Proxy**：**强烈建议开启**，否则浏览器可能会拦截请求[span_33](end_span)。
4.  [span_34](start_span)点击 `Test Send` 测试，成功后可点击主界面的 `📡 简报` 发送实时账户状态[span_34](end_span)。

---

## ⌨️ 快捷键与交互 (Controls)

| 区域 | 交互操作 | 功能 |
| :--- | :--- | :--- |
| **Header** | 点击 `☀️`/`🌙`/`👾` | [span_35](start_span)切换 Dark / Light / Pixel 主题[span_35](end_span) |
| **Header** | 点击 `BINANCE` / `OKX` | [span_36](start_span)切换 WebSocket 数据源[span_36](end_span) |
| **Strategy** | 点击表格行 | [span_37](start_span)将该行价格载入沙盘 (Load to Sim)[span_37](end_span) |
| **Dock** | 点击 `📷 识别` | [span_38](start_span)触发文件上传进行 OCR 识别[span_38](end_span) |
| **Dock** | 点击 `🔄 换源` | [span_39](start_span)快速轮换数据源[span_39](end_span) |

---

## 🏗️ 技术架构 (Architecture)

* **Frontend**: 原生 HTML5 / CSS3 (Grid & Flexbox) / Vanilla JavaScript ES6+
* **[span_40](start_span)[span_41](start_span)[span_42](start_span)Style**: CSS Variables (`:root`) 实现多主题切换[span_40](end_span)[span_41](end_span)[span_42](end_span)。
* **[span_43](start_span)[span_44](start_span)Networking**: `WebSocket` (WSS) 实时连接交易所公共流[span_43](end_span)[span_44](end_span)。
* **[span_45](start_span)AI/OCR**: 集成 `Tesseract.js v5` CDN 版本[span_45](end_span)。
* **[span_46](start_span)Persistence**: `localStorage` 保存 Telegram 配置[span_46](end_span)。

---

## ⚠️ 免责声明 (Disclaimer)

* **Risk Warning**: 加密货币合约交易具有极高风险。本工具提供的 PNL 和 LIQ 计算仅供参考，实际强平价格受交易所维持保证金率 (MMR) 和保险基金机制影响，请以交易所即时数据为准。
* **Security**: 本工具所有数据处理均在本地浏览器完成（Client-side），Bot Token 仅存储于本地 LocalStorage，不会上传至任何第三方服务器。
* **License**: MIT License.

---

<div align="center">
    <b>@oAdam TERMINAL V22</b><br>
    <i>Crafted for the Degens.</i>
</div>
# Fully-Hedged