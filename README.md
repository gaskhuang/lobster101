# 🦞 龍蝦101 — 用 OpenClaw 做任何自動化

> 想用 AI 自動化某件事？來這裡找方法。

[![案例數](https://img.shields.io/badge/案例-118+-orange)](./cases/)
[![Skills](https://img.shields.io/badge/Skills-5494+-blue)](./skills/)
[![更新](https://img.shields.io/badge/持續更新-每週-green)]()

---

## 🤔 龍蝦101 是什麼？

這是一份由 **G大（gskgino）** 維護的 OpenClaw 自動化案例清單。

OpenClaw（又叫龍蝦🦞）是一個開源 AI 助手框架，可串接 Telegram、WhatsApp、Discord，能讀檔案、寫程式、呼叫 API、自動執行任務。

這裡收錄所有你能用龍蝦做的事，附上說明、工具與執行方式。

---

## 📋 案例庫（118+ 個）

### 📱 社群媒體（9 個）
| 案例 | 難度 | 工具 |
|------|------|------|
| 每日 Reddit 摘要 | 簡單 | daily-reddit-digest |
| 每日 YouTube 摘要 | 簡單 | summarize |
| X 帳號質性分析 | 中等 | x-account-analysis |
| 多來源科技新聞摘要 | 簡單 | news-aggregator |
| 品牌社群監控 | 中等 | Tavily + Telegram |
| 自動排程社群發文 | 簡單 | auto-social-posting |
| Instagram Story 管理 | 中等 | instagrapi |
| Reddit 產品聲量追蹤 | 中等 | Tavily |
| X 互動管理助手 | 中等 | twitter skill |

### 🎨 創意與內容製作（9 個）
| 案例 | 難度 | 工具 |
|------|------|------|
| YouTube 內容產線 | 中等 | notebooklm + summarize |
| Podcast 製作流水線 | 中等 | notebooklm |
| 電子報轉 Podcast | 簡單 | notebooklm |
| AI 寫作助手 | 簡單 | Claude 內建 |
| 一文多平台內容複製 | 中等 | auto-social-posting |
| 學術研究助手 | 中等 | Tavily + second-brain |
| 多代理內容工廠 | 困難 | multi-agent |
| 自主遊戲開發流水線 | 困難 | coding-agent |
| 目標驅動自主任務 | 困難 | proactive-agent |

### ⚡ 生產力工具（26 個）
| 案例 | 難度 | 工具 |
|------|------|------|
| 客製化晨間簡報 | 簡單 | weather + gog + news |
| 自動會議紀錄 | 簡單 | whisper + gog |
| 第二大腦 | 中等 | second-brain |
| 郵件自動分類器 | 中等 | gog Gmail |
| 語音筆記轉任務 | 簡單 | whisper |
| PDF 文件處理中心 | 簡單 | pdf tool |
| 個人 CRM | 中等 | gog Contacts |
| 行事曆衝突排解 | 中等 | gog Calendar |
| 看板自動整理 | 簡單 | GitHub Projects |
| 習慣追蹤與問責教練 | 簡單 | Telegram + cron |
| ...（更多） | | |

### 💼 商業、行銷與銷售（14 個）
### 🔧 DevOps 與工程（10 個）
### 🛡️ 安全與合規（6 個）
### 🖥️ 監控與維運（8 個）
### 🔬 研究與學習（9 個）
### 💰 金融與交易（6 個）
### 🏥 健康與個人成長（6 個）
### 🧠 AI 記憶與代理架構（5 個）

> 📄 完整 118 個案例詳情：[cases/claw101-cases.md](./cases/claw101-cases.md)

---

## 🛠️ Skills 分類（5,494 個精選）

| 分類 | Skills 數 | 說明 |
|------|-----------|------|
| 🤖 Coding Agents | 1,222 | AI 寫程式、IDE 整合 |
| 🌐 Web & Frontend | 938 | 網頁開發、爬蟲 |
| ☁️ DevOps & Cloud | 408 | CI/CD、雲端部署 |
| 🔍 Search & Research | 350 | 搜尋、資料蒐集 |
| 🖥️ Browser & Automation | 335 | 瀏覽器控制 |
| 🧠 AI & LLMs | 197 | AI 模型整合 |
| 📋 Productivity | 206 | 生產力工具 |
| 💬 Communication | 149 | Telegram/Email/Discord |
| 📈 Marketing & Sales | 104 | 行銷自動化 |
| 💰 Finance | 21 | 財務追蹤 |
| ...更多 32 類 | 5,494 總計 | |

> 📄 完整 Skills 分類：[skills/skills-categories.md](./skills/skills-categories.md)

---

## 🚀 快速上手

```bash
# 1. 安裝 OpenClaw
npm install -g openclaw

# 2. 安裝常用 skills
clawhub install tavily-search
clawhub install second-brain
clawhub install auto-social-posting

# 3. 啟動
openclaw start
```

---

## 📬 想讓我幫你做自動化？

**告訴我你想做什麼，我幫你用龍蝦實現。**

- 💬 Telegram：@gskgino
- 🐙 GitHub：[gaskhuang](https://github.com/gaskhuang)
- 🦞 OpenClaw 社群：[OpenClaw 中文社群](https://t.me/claw101)

---

## 📅 更新紀錄

| 日期 | 更新內容 |
|------|---------|
| 2026-03-07 | 初始化，收錄 118 個案例 + 32 類 5494 個 Skills |

---

*🦞 龍蝦101 由 G大 持續維護中 · MIT License*
