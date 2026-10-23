# 履歷組合器 Resume Composer

單一 HTML 檔的中文履歷組合工具：素材庫（卡片）＋ 投遞版本組合器，可列印成 A4 PDF、複製 104 純文字。

**本 repo 只有程式碼，不含任何個人資料。** 資料存放在使用者自己的 GitHub 私有 repo（預設 `CasioESH311/resume-data` 的 `resume.json`），透過 GitHub Contents API 讀寫：

- 開啟時自動載入雲端最新版；修改後約 4 秒自動 commit，也可「立即同步」。
- 每 60 秒及切回視窗時檢查雲端更新；同時修改時提供「保留雲端版本 / 用我的版本覆蓋 / 先匯出備份」。
- 金鑰（fine-grained PAT，只需目標 repo 的 Contents: Read and write）只存在瀏覽器 localStorage，可隨時「清除金鑰」。
- 未設定金鑰時為本機模式：空白範本＋匯入／匯出 JSON 備份。

使用：<https://casioesh311.github.io/resume-builder/> → 右上角「☁」→ 輸入 owner / repo / branch / 路徑與金鑰（建立：<https://github.com/settings/personal-access-tokens/new>）。

---

Single-file résumé composer (Traditional Chinese UI). It contains no personal data. Data lives in a private GitHub repo and syncs through the Contents API, authenticated with a fine-grained PAT that is stored only in the browser's localStorage.
