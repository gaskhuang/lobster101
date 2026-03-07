# 龍蝦101 - OpenClaw 使用案例清單
來源：claw101.com | openclaw101.dev
更新日期：2026-03-07

---

## 網站架構概況

**claw101.com** 是 OpenClaw 最主要的學習入口站，分為：
- `/en` — 英文主頁（學習中心）
- `/en/cases` — 6 個真實商業案例
- `/en/blog` — OpenClaw Field Journal（實戰部落格）
- Telegram 社群：[@claw101](https://t.me/claw101)

**openclaw101.dev** — 另一個資源站，整理了 376+ 教程，涵蓋 31 種 Skill 分類（5494+ 社群 Skills）

---

## 案例清單（Cases Library）

### 1. Telegram 客服自動回覆
- **說明**：監聽客戶關鍵詞並自動匹配標準回覆；複雜問題自動轉人工。平均響應時間從 8 分鐘降到 40 秒。
- **使用工具/Skill**：OpenClaw + Telegram Bot API + 關鍵詞規則引擎
- **執行方式**：
  1. 設定 Telegram Bot Token
  2. 建立關鍵詞-回覆對應規則（YAML/JSON）
  3. 配置「轉人工」條件觸發器
  4. 啟動 OpenClaw Gateway 持續監聽
- **難度**：簡單
- **來源連結**：https://claw101.com/en/cases

---

### 2. 每日自動抓取行業新聞並匯總
- **說明**：每天定時抓取 50+ 信息源，自動去重、摘要、分類後推送到飛書和 Telegram，每天節省 2 小時信息整理時間。
- **使用工具/Skill**：OpenClaw + Heartbeat（定時觸發）+ Web Fetch + Feishu/Telegram
- **執行方式**：
  1. 設定 50+ RSS/網頁信息源清單
  2. 配置 Heartbeat 每日定時觸發
  3. Agent 自動抓取 → 去重 → AI 摘要 → 分類
  4. 推送到飛書群 + Telegram 頻道
- **難度**：中等
- **來源連結**：https://claw101.com/en/cases

---

### 3. 代碼審查自動化（Code Review）
- **說明**：在 PR 創建後自動執行規則審查和風險提示，附帶修改建議與 diff 注釋。團隊評審輪次減少約 35%。
- **使用工具/Skill**：OpenClaw + GitHub Webhook + Claude Code
- **執行方式**：
  1. 配置 GitHub Webhook 觸發 PR 事件
  2. OpenClaw 自動拉取 diff 內容
  3. 對照規則集進行審查（風格/安全/邏輯）
  4. 自動在 PR 留下帶有建議的 diff 注釋
- **難度**：中等
- **來源連結**：https://claw101.com/en/cases

---

### 4. 多語言客服機器人
- **說明**：接入中文、英文、日文三語知識庫，按用戶語言自動切換回覆風格。跨境業務夜間諮詢轉化率明顯提升。
- **使用工具/Skill**：OpenClaw + 多語言知識庫 + 語言偵測 + Telegram/WhatsApp
- **執行方式**：
  1. 建立三語版本知識庫（FAQ + 產品說明）
  2. 設定語言自動偵測邏輯
  3. 每種語言對應不同的回覆 Prompt 模板
  4. 24/7 持續運行（利用 OpenClaw Gateway）
- **難度**：中等
- **來源連結**：https://claw101.com/en/cases

---

### 5. 個人知識庫管理
- **說明**：把網頁、群聊和語音記錄統一整理進 Notion，自動打標籤並關聯主題。檢索速度比手動整理快 5 倍以上。
- **使用工具/Skill**：OpenClaw + Notion API + Web Fetch + 語音轉文字
- **執行方式**：
  1. 設定 OpenClaw 監聽 Telegram 頻道/群聊
  2. 自動擷取網頁 URL 內容（web_fetch）
  3. AI 自動打標籤分類
  4. 推送到 Notion 指定資料庫，建立雙向連結
- **難度**：中等
- **來源連結**：https://claw101.com/en/cases

---

### 6. 社群運營自動化
- **說明**：自動執行歡迎話術、活動提醒、週報匯總和活躍度分析。運營同學可把時間集中在活動策劃和轉化閉環。
- **使用工具/Skill**：OpenClaw + Telegram/Discord + Heartbeat 定時觸發
- **執行方式**：
  1. 設定新成員歡迎訊息模板
  2. Heartbeat 每週觸發週報匯總 + 發送
  3. 活動提醒按日曆自動觸發
  4. 活躍度分析（統計發言數/互動率）並輸出報告
- **難度**：簡單
- **來源連結**：https://claw101.com/en/cases

---

## 實戰部落格案例（Field Journal）

### 7. 6 個 AI 平行執行 - 6 分鐘完成網站改版
- **說明**：將網站改版拆成 6 個獨立子任務（首頁重設計、SEO 優化、案例頁、部落格系統、英文翻譯、搜尋功能），同時平行執行，從 40+ 分鐘縮短到約 6 分鐘。
- **使用工具/Skill**：OpenClaw Parallel Tasks（多 Sub-Agent）+ Claude Code
- **執行方式**：
  1. 將大任務拆分成 3~8 個完全獨立的子任務
  2. 在 OpenClaw 配置 `parallel_tasks` YAML
  3. 確保各 Agent 使用不同目錄，避免衝突
  4. 使用 Git 分支隔離，最後合並
  5. 執行 `npm run build` 驗證全部輸出
- **難度**：困難
- **來源連結**：https://claw101.com/en/blog/parallel-agents

---

### 8. 瀏覽器自動化 - 讓 OpenClaw 接管 Web 工作流
- **說明**：使用 Browser Relay 模組（Playwright 驅動），讓 AI Agent 操作真實瀏覽器，完成登入、爬蟲、表單提交等任務。
- **使用工具/Skill**：OpenClaw Browser Relay + Playwright + browser tool
- **執行方式（三大場景）**：
  1. **自動登入後台**：`claw forms run admin_login`，搭配環境變數注入密碼
  2. **競品價格爬蟲**：配置 scraping rules + 分頁爬取，輸出比較表格
  3. **批量表單提交**：`claw forms run expense_report --data-file expenses.csv`
- **難度**：中等
- **來源連結**：https://claw101.com/en/blog/browser-automation

---

### 9. 1 小時用 6 個 AI 建立知識型網站
- **說明**：真實案例：1 小時決策 + 6 個平行子任務，首日獲得 100+ 付費用戶。
- **使用工具/Skill**：OpenClaw 多 Sub-Agent + 內容生成 + 自動部署
- **執行方式**：
  1. 定義業務目標（知識付費社群）
  2. 拆解任務：內容架構 / 視覺設計 / SEO / 付費牆 / 推廣文案 / 自動化流程
  3. 6 個 Agent 同步執行，負責人只做驗收
- **難度**：困難
- **來源連結**：https://claw101.com/en/blog/one-hour-story

---

### 10. 1 小時與 AI 對談建立完整業務
- **說明**：創業者 Tao 與 AI Dragon（Xiaolong）在 24 小時內建立付費社群的真實故事。
- **使用工具/Skill**：OpenClaw + 自訂 SOUL.md Persona + Telegram 社群管理
- **執行方式**：
  1. 定義 AI 角色人設（SOUL.md）
  2. 設定目標、拆解為可執行清單
  3. AI 負責執行，人類負責決策和驗收
  4. 24 小時內上線並開始收費
- **難度**：中等
- **來源連結**：https://claw101.com/en/blog/taoge-and-xiaolong

---

### 11. OpenClaw 成本控制七招
- **說明**：模型路由、上下文預算、平行執行策略，以及每週成本審查，讓 AI 自動化邊際成本趨近 $0。
- **使用工具/Skill**：OpenClaw 模型路由 + 成本監控
- **執行方式**：
  1. 按任務類型路由模型（簡單任務用便宜模型）
  2. 設定上下文預算限制（避免 token 爆炸）
  3. 批量任務用平行執行減少掛機時間
  4. 每週檢視 API 費用報告
- **難度**：中等
- **來源連結**：https://claw101.com/en/blog/openclaw-cost-control

---

### 12. 新手常見 5 大錯誤（附解法）
- **說明**：從目標設定到任務拆分，整理 5 個 OpenClaw 新手常踩的坑，每個都附有可操作的解決方案。
- **使用工具/Skill**：OpenClaw 基礎配置
- **執行方式**：
  1. 錯誤一：目標太模糊 → 改為「可驗收的 deliverable」
  2. 錯誤二：不拆任務直接下指令 → 先拆解再執行
  3. 錯誤三：不給 Context → 提供足夠的背景文件
  4. 錯誤四：不審查輸出 → 每次都要 review + build
  5. 錯誤五：期待一次到位 → 迭代改進思維
- **難度**：簡單
- **來源連結**：https://claw101.com/en/blog/beginner-mistakes

---

## 延伸資源（來自 openclaw101.dev）

| 資源類型 | 說明 | 連結 |
|---------|------|------|
| 官方文件 | OpenClaw 完整 API 參考 | https://docs.openclaw.ai |
| Skill 市集 | ClawHub 技能安裝 | https://clawhub.com |
| 社群精選 Skills | Awesome OpenClaw Skills | https://github.com/VoltAgent/awesome-openclaw-skills |
| 雲端部署 | DigitalOcean 一鍵部署 | https://www.digitalocean.com/community/tutorials/how-to-run-openclaw |
| 阿里雲部署 | 釘釘 AI 助理 | https://help.aliyun.com/zh/simple-application-server/use-cases/quickly-deploy-and-use-openclaw |
| 騰訊雲部署 | 飛書機器人 | https://cloud.tencent.com/developer/article/2625073 |
| 中文速查表 | OpenClaw Mega Cheatsheet | https://moltfounders.com/openclaw-mega-cheatsheet |

---

## Skill 分類總覽（5494+ 社群 Skills）

| 分類 | 數量 | 代表用途 |
|------|------|---------|
| AI & LLMs | 159 | 多模型路由、提示工程 |
| Search & Research | 148 | 網路搜尋、資料爬取 |
| DevOps & Cloud | 144 | 雲端部署、CI/CD 整合 |
| Marketing & Sales | 94 | 社群行銷、潛在客戶管理 |
| Notes & PKM | 61 | 知識庫、Notion 整合 |
| Communication | 58 | Telegram/Slack/Discord |
| Coding Agents | 55 | 程式碼生成、PR Review |
| Smart Home & IoT | 50 | 智慧家居自動化 |
| Web & Frontend | 46 | 網站建設、爬蟲 |
| Speech & Audio | 44 | 語音轉文字、TTS |
| Health & Fitness | 35 | 健康追蹤、日程管理 |
| Gaming | 7 | 遊戲自動化 |

---

## 安裝任何 Skill 的方式

```bash
npx clawhub@latest install <skill-name>
```

---

*本清單由阿蓋小弟爬取整理，資料來源：claw101.com + openclaw101.dev*
