# Dashboard 變更紀錄

版本號用 `YYYY.MM.DD-n`。每次 push 前在最上方新增一段，註明影響範圍與**要先跑的 SQL**（SQL 檔放在 event-registration repo 的 `SQL/`）。
跨 repo 的總變更紀錄見 event-registration 的 `docs/CHANGELOG.md`。

## [未發佈]
（新的變更先寫這裡）

## 2026.10.10-1
- 「溝通共識系統」擴充：會議類型、場次（出席／紀錄／狀態／待辦）、待辦事項總覽、統計與匯出 Excel／出席明細 CSV。直接寫資料庫（超級管理者 RLS）。見 event-registration `docs/DECISIONS.md` D-20261010-01。無新 SQL。

## 2026.10.09（含未推送的修改）
- 開班參加名單 Excel：天職欄位視為格式欄位；自動排序改為「依性別及天職（預設）」「依報名時間」兩種；匯入範本帶入所有有值儲存格與公式；移除「加入天職欄位」勾選框。
- 新增 docs/。無新 SQL。

## 以下為 GitHub 提交歷史（自動整理）

### 2026-10-09
- Update roster export in dashboard
- Update roster export in dashboard
- Update roster export in dashboard
- Add roster export and saint save fix to dashboard

### 2026-10-08
- Add altar team dashboard features
- Update altar calendar dashboard

### 2026-10-07
- Add checklist templates for subtasks
- Add lunar 1/15 handling to dashboard calendar
- Add PDF export to dashboard
- Apply saint-import-fix and altar-leader-events updates to dashboard

### 2026-10-06
- Add saint day lunar calendar management
- Add train schedule management
- Preserve field IDs and export archived answers
- Remove obsolete standalone LIFF links
- Update dashboard for saint-days calendar feature

### 2026-10-05
- Remove phone fields from Dashboard workflows
- Improve Word import detection and train fields
- Add work rules import and registration bulk actions
- Add calendar filters and duplicate registration controls
- Add calendar management and CSV export tools

### 2026-10-02
- Display multi-assignee subtasks
- Add admin role management controls
- Improve subtask section styling
- Add altar and member profile administration
- Add featured program controls

### 2026-09-30
- Update Home branding and default event fields
- Use shared Home LIFF entry point

### 2026-09-29
- Add LIFF link regeneration controls
- Include entity parameters in LIFF links
- Add task assignment dashboard views

### 2026-09-23
- Add resident team and system management
- Make index.html the single Dashboard entry point

### 2026-09-22
- Add per-altar LIFF links and team task sync
- Add per-altar LIFF links and team task sync
- Sync index.html with admin-dashboard.html (missed in last 2 updates)
- Update admin dashboard system hierarchy and kitchen management
- Add Meetings panel and System/Group hierarchy to admin dashboard

### 2026-09-21
- support message api

### 2026-09-20
- Add event service toggles + Lodging management panel
- Carpool v5: show waiting location + time range in matching modal
- Carpool v3: dashboard matching modal for new fields/status
- Add Carpool panel: LIFF link, Car Managers list, per-event matching

### 2026-09-19
- Add group checkboxes to New Event form
- Add Event Admins management to Manage Events panel
- Add Home Link management modal

### 2026-09-18
- Support templete while creating the activity
- minor change for the naming
- minor fix for creating item on activity
- Support activity flow
- Add Job Admins management and job-admin LIFF link
- Add job presets: save/apply job content excluding recurrence, day settings, and slots
- Task stats/cards reflect subtask status instead of job-level assignments

### 2026-09-17
- Add Groups management and template group assignment
- Add task status stats tiles and confirm action
- support a single task
- Support multi-attendee registration
- Support multi-attendee registration
- Support multi-attendee registration
- Admin dashboard: dynamic per-event fields, no email column
