# Dashboard 文件

Dashboard 是單一檔案 `index.html`（約 8,400 行），給管理者在電腦上使用。它和 LIFF 頁面共用同一個 Supabase 資料庫。

**主文件在 `event-registration` repo 的 `docs/`**，這裡只放 Dashboard 自己的內容，避免兩邊內容不一致：

| 檔案 | 內容 |
|---|---|
| [FEATURES.md](FEATURES.md) | Dashboard 的功能面板與每項功能在 LIFF 的對照 |
| [CHANGELOG.md](CHANGELOG.md) | Dashboard 的變更紀錄 |
| event-registration/docs/DECISIONS.md | 討論過的決議（兩邊共用） |
| event-registration/docs/DEPLOY.md | 部署流程、SQL 清單 |

## 維護規則
1. 改 `index.html` 就同步更新本資料夾的 FEATURES／CHANGELOG；有決議寫進 event-registration 的 DECISIONS.md。
2. 每個功能手機（LIFF）與 Dashboard 兩邊都要有；只在 Dashboard 的要在 FEATURES.md 註明原因。
3. 需要新資料庫欄位時，先在 event-registration 的 `SQL/` 加新編號檔，**先跑 SQL 再推 Dashboard**。
4. 推送前先跑 `git diff`，確認只有預期的檔案有變動。

## 技術備忘
- 登入：Supabase Auth；權限靠資料庫 RLS（`is_super_admin()` 等）。管理者角色與 LIFF 建立透過 Edge Function `admin-roles-api`、`create-liff-app`。
- 設定常數在檔案前段：`SUPABASE_URL`、`SUPABASE_ANON_KEY`、`ADMIN_ROLES_FUNCTION_URL`、`CREATE_LIFF_FUNCTION_URL`。
- 外部程式庫（CDN，按需載入）：supabase-js、ExcelJS 4.4.0（Excel 匯出與範本匯入）、SheetJS xlsx 0.18.5（6W 簡流表匯入）、JSZip（Word 匯入）、html2canvas 1.4.1＋jsPDF 2.5.1（PDF 匯出）、lunar-javascript（農曆）。
- 單檔結構以 `/* ---------- 區段名稱 ---------- */` 註解分區，搜尋該註解可快速定位。
