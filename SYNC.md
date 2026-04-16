# 同步工作流

本 repo 的內容來自 `website-modules/preview/` 與 `website-modules/styles/`。

## 未來如何同步新內容

當 website-modules 有新品牌 preview 或風格更新，執行以下步驟：

### Windows 手動同步

```cmd
@echo off
REM 同步 preview/brands/
xcopy /E /Y /I C:\work\website-modules\preview\brands C:\work\precraft-preview\preview\brands

REM 同步 styles/（7 個風格）
for %%s in (minimal bold editorial gentle playful warm) do (
    xcopy /E /Y /I C:\work\website-modules\styles\%%s C:\work\precraft-preview\styles\%%s
)
xcopy /E /Y /I C:\work\website-modules\styles\04-elegant C:\work\precraft-preview\styles\04-elegant

REM Commit 並 push
cd C:\work\precraft-preview
git add .
git commit -m "同步更新：從 website-modules 同步最新 preview 與 styles"
git push origin main
```

### 同步後注意事項

1. 檢查新增的 HTML 是否有引用 `../precraft-home.html`，如有需改為 `../../index.html`
2. 檢查新增的 HTML 是否有引用 `../../modules/` 或 `../../compliance/`，這些不應出現在 public repo
3. 不要同步 `preview/internal/`（內部工具）和 `preview/precraft-*`（官網 MVP）

### 建議同步時機

- 新增品牌 preview 時
- 風格 CSS 有修改時
- 元億或其他客戶打樣有更新時
