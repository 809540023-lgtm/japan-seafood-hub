# 日本海產出口 AI 統籌中心

以 AI Agent 為核心的日本海產（→全球）出口統籌平台。單一檔案純靜態網站（`index.html`），無需後端、無需建置。

## 功能模組
- 儀表板（使命、商品線、自動化作業流、市場數據、每日動態 feed）
- AI 助理（媒合 / 查法規 / 追動態 / 引用學習到的情報）
- 智能媒合引擎（買家↔供應商評分）
- 出口工具箱（法規檢核 / 到岸成本試算 / 文件產生）
- 商談管線 CRM、Agent 學習中心
- 供應商目錄（30 家，可篩選）、各亞洲市場出口法規流程、市場觀察記錄、成功案例

資料儲存於瀏覽器 localStorage（觀察記錄、商談、學習知識庫）。

---

## 部署到 GitHub + Render

### 步驟 1：建立 GitHub repo
1. 到 https://github.com/new 建立新 repo（例如 `japan-seafood-hub`，設 Public）。
2. 上傳本資料夾的三個檔案：`index.html`、`render.yaml`、`README.md`
   （網頁版：repo 頁面 → **Add file → Upload files** → 拖入 → Commit）。

### 步驟 2：在 Render 建立 Static Site
1. 登入 https://render.com → **New +** → **Static Site**。
2. 連結你的 GitHub 並選擇剛建立的 repo。
3. 設定：
   - **Build Command**：留空（或 `echo no build`）
   - **Publish Directory**：`.`
4. 按 **Create Static Site**，等待數十秒即會給你一個 `https://<名稱>.onrender.com` 網址。

> repo 內已含 `render.yaml`，Render 也可用 **Blueprint** 一鍵套用設定。

### 不想用 GitHub？
Render 可直接連 public Git repo；或改用拖拉式靜態託管（Netlify Drop / Cloudflare Pages / GitHub Pages）——把 `index.html` 丟上去即可。

## 本機預覽
直接用瀏覽器開啟 `index.html` 即可，或：
```bash
python3 -m http.server 8080   # 然後開 http://localhost:8080
```
