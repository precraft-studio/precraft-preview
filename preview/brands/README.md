# preview/brands/ — 虛構品牌 Preview 頁面

本資料夾存放 Precraft 的虛構品牌展示頁面。每個品牌代表一種 CSS 風格，用於向潛在客戶展示 Precraft 的設計能力。

**重要：所有品牌均為虛構，每個頁面的 Footer 都有明確標註。**

## 7 個品牌 + 1 個保留品牌

| 品牌 | 產業 | 風格 | 狀態 | AI 圖片 |
|------|------|------|------|---------|
| Lumiere | 美妝保養 | elegant | 展示中 | 5 張 |
| Studio Noir | 設計工作室 | minimal | 展示中 | 6 張 |
| PawCare | 寵物保健 | warm | 展示中 | 5 張 |
| IronCore | 健身運動 | bold | 展示中 | 5 張 |
| Aroma | 精品咖啡 | editorial | 展示中 | 6 張 |
| KidsLab | 親子科學教育 | playful | 展示中 | 5 張 |
| 溫柔時光 Grace Care | 居家長照 | gentle | 展示中 | 5 張 |
| Craftland | 手工藝 | — | **保留不展示** | 5 張 |

## Craftland 的狀態說明

Craftland 的品牌頁面（`craftland.html`）和圖片（`assets/craftland/`）仍保留在此資料夾中，但不在 style-samples.html 中展示。

原因：
- warm 風格改由 PawCare 代表，Craftland 的木棕色調與 warm 重疊度高
- 7 個展示位置需要 7 個不同風格的代表，不允許同色系重複
- Craftland 保留作為備用素材，未來如需展示「自然工藝」子方向時可重新啟用

## 檔案結構

```
preview/brands/
├── lumiere.html
├── studio-noir.html
├── pawcare.html
├── ironcore.html
├── aroma.html
├── kidslab.html
├── grace-care.html
├── craftland.html          ← 保留不展示
└── assets/
    ├── lumiere/             ← AI 生成圖片
    ├── studio-noir/
    ├── pawcare/
    ├── ironcore/
    ├── aroma/
    ├── kidslab/
    ├── grace-care/
    └── craftland/           ← 圖片保留
```

## 圖片生成工具

所有 AI 圖片由 Gemini（gemini-3-pro-image-preview）生成。每張圖片的 prompt 記錄在對應的 commit 訊息中。

## 使用方式

這些品牌頁面有兩個用途：
1. **Precraft 官網 Styles 頁面**（`precraft-styles.html`）：精選 4 個品牌對外展示
2. **內部風格樣本集**（`internal/style-samples.html`）：7 個品牌完整展示，供面對面客戶對話使用
