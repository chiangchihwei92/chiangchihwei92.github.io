# Giscus 留言系統設定指南 / Giscus Comments Setup Guide

本網站現在使用 **Giscus** 作為留言系統。Giscus 是一個基於 GitHub Discussions 的開源留言系統，讓訪客可以留下評論和回饋。

This website now uses **Giscus** as the commenting system. Giscus is an open-source commenting system powered by GitHub Discussions, allowing visitors to leave comments and feedback.

## 設定步驟 / Setup Steps

### 1. 啟用 GitHub Discussions / Enable GitHub Discussions

1. 前往你的 GitHub 儲存庫 / Go to your GitHub repository:
   `https://github.com/chiangchihwei92/chiangchihwei92.github.io`

2. 點擊 **Settings** (設定)

3. 向下捲動到 **Features** 區塊

4. 勾選 **Discussions** 選項來啟用它

### 2. 安裝 Giscus App / Install Giscus App

1. 前往 / Visit: https://github.com/apps/giscus

2. 點擊 **Install** (安裝)

3. 選擇 **Only select repositories** (僅選取特定儲存庫)

4. 選擇 `chiangchihwei92/chiangchihwei92.github.io`

5. 點擊 **Install** 完成安裝

### 3. 設定 Giscus / Configure Giscus

1. 前往 / Visit: https://giscus.app/zh-TW

2. 在 **儲存庫** 欄位輸入 / In the **Repository** field, enter:
   ```
   chiangchihwei92/chiangchihwei92.github.io
   ```

3. 在 **Discussion 分類** 選擇 / For **Discussion Category**, choose:
   - 推薦選擇 **General** 或 **Announcements**
   - Recommended: **General** or **Announcements**

4. 複製生成的設定值 / Copy the generated configuration values:
   - `data-category-id` (例如 / e.g., `DIC_kwDOPL1KJs4Clq6g`)

5. 更新 `index.html` 中的 `initializeGiscusComments` 函數:
   Update the `initializeGiscusComments` function in `index.html`:
   ```javascript
   script.setAttribute('data-category-id', 'YOUR_CATEGORY_ID_HERE');
   ```

## 功能說明 / Features

✅ **自動載入** - 留言系統會在切換到產品頁面時自動載入
   **Auto-loading** - Comments load automatically when switching to product pages

✅ **中文介面** - 已設定為繁體中文 (zh-TW)
   **Chinese Interface** - Configured for Traditional Chinese

✅ **輕量級** - 不需要資料庫，使用 GitHub 作為後端
   **Lightweight** - No database required, uses GitHub as backend

✅ **反應表情** - 訪客可以對留言按讚或加上表情符號
   **Reactions** - Visitors can like comments and add emoji reactions

✅ **GitHub 帳號登入** - 訪客需要 GitHub 帳號才能留言 (有效防止垃圾留言)
   **GitHub Login** - Visitors need a GitHub account to comment (prevents spam)

## 疑難排解 / Troubleshooting

### 留言區沒有顯示 / Comments not showing

1. 確認已啟用 GitHub Discussions
   Confirm GitHub Discussions is enabled

2. 確認已安裝 Giscus App
   Confirm Giscus App is installed

3. 檢查瀏覽器控制台是否有錯誤訊息
   Check browser console for error messages

4. 確認 `data-category-id` 設定正確
   Verify `data-category-id` is configured correctly

### 如何管理留言 / Managing Comments

所有留言都會出現在 GitHub Discussions 中，你可以在那裡:
All comments appear in GitHub Discussions, where you can:

- 編輯或刪除留言 / Edit or delete comments
- 標記為已解決 / Mark as resolved
- 釘選重要留言 / Pin important comments
- 封鎖濫用者 / Block abusive users

前往 / Go to: `https://github.com/chiangchihwei92/chiangchihwei92.github.io/discussions`

## 其他資源 / Additional Resources

- Giscus 官方網站 / Official Website: https://giscus.app
- Giscus GitHub: https://github.com/giscus/giscus
- 文件 / Documentation: https://github.com/giscus/giscus/blob/main/ADVANCED-USAGE.md

---

如有問題，請查看 [Giscus 文件](https://github.com/giscus/giscus/blob/main/README.zh-TW.md) 或在 GitHub Issues 提問。

For questions, please check the [Giscus documentation](https://github.com/giscus/giscus) or ask in GitHub Issues.
