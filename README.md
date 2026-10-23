# 履歷組合器 Resume Composer

單一 HTML 檔的中文履歷組合工具：素材庫（卡片）＋ 投遞版本組合器，可列印成 A4 PDF、複製 104 純文字。

**本 repo 只有程式碼，不含任何個人資料。** 資料存放在使用者自己的 GitHub 私有 repo（預設 `CasioESH311/resume-data` 的 `resume.json`），透過 GitHub Contents API 讀寫：

- 開啟時自動載入雲端最新版；修改後約 4 秒自動 commit，也可「立即同步」。
- 每 60 秒及切回視窗時檢查雲端更新；同時修改時提供「保留雲端版本 / 用我的版本覆蓋 / 先匯出備份」。
- 金鑰（fine-grained PAT，只需目標 repo 的 Contents: Read and write）只存在瀏覽器 localStorage，可隨時「清除金鑰」。
- 未設定金鑰時為本機模式：空白範本＋匯入／匯出 JSON 備份。

使用：<https://casioesh311.github.io/resume-builder/> → 右上角「☁」→ 輸入 owner / repo / branch / 路徑與金鑰（建立：<https://github.com/settings/personal-access-tokens/new>）。

## 🎤 語音模擬面試（interview.html）

<https://casioesh311.github.io/resume-builder/interview.html>

這個頁面用 Google Gemini 免費 API 扮演三位科技業 EHS 面試官（HR 主管、職安主管、資深職安經理），以繁體中文語音進行模擬面試。面試結束後會產生評估報告，可下載成 .md 檔；也可以按按鈕，選擇存到私有 repo 的 `interviews/` 資料夾。Gemini 金鑰（到 <https://aistudio.google.com/apikey> 免費取得）只會存在瀏覽器的 localStorage。語音辨識建議使用電腦版 Chrome 或 Edge。

---

Single-file résumé composer (Traditional Chinese UI). It contains no personal data. Data lives in a private GitHub repo and syncs through the Contents API, authenticated with a fine-grained PAT that is stored only in the browser's localStorage.
