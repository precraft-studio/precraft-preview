# 04-elegant — 優雅質感風格

## 風格總覽

以深酒紅為品牌主色、金色為點綴強調色，搭配奶油色暖底背景，營造高端而溫暖的視覺氛圍。標題使用 Playfair Display 襯線體增加質感，內文使用 Noto Sans TC 確保中文可讀性。

## 適用產業

| 產業 | 適合度 | 原因 |
|------|--------|------|
| 美妝保養品牌 | ★★★★★ | 深酒紅 + 金色 = 高端質感，奶油色背景溫和 |
| 醫美診所 | ★★★★★ | 專業感 + 信賴感，臨床數據模組加分 |
| 精品零售 | ★★★★☆ | 襯線標題 + 留白充裕 = 精品氛圍 |
| 保健食品 | ★★★★☆ | 合規聲明模組 + 臨床數據 = 專業可信 |
| 高端服務業 | ★★★☆☆ | 色調偏女性，可調整主色適應 |

## 配色方案

### 品牌色

| 色碼 | 用途 | CSS 變數 |
|------|------|---------|
| `#8B1A2E` | 深酒紅 — 品牌主色 | `--color-primary` |
| `#6B1222` | 加深 — hover、漸層 | `--color-primary-dark` |
| `#A82438` | 減淡 — 漸層搭配 | `--color-primary-light` |
| `#5C1020` | 中深 — page header 漸層 | `--color-primary-darker` |
| `#3D0A14` | 最深 — 頁尾背景 | `--color-footer-bg` |
| `#C9A84C` | 金色 — 強調、hover、引言裝飾 | `--color-accent` |

### 背景色

| 色碼 | 用途 | CSS 變數 |
|------|------|---------|
| `#FFFFFF` | 主背景 | `--color-bg` |
| `#F9F6F0` | 奶油色 — 卡片背景、品牌區 | `--color-bg-alt` |
| `#F4F4F4` | 淺灰 — 產品區段背景 | `--color-bg-light` |
| `#f8f4f0` | 暖灰 — 品牌故事漸層 | `--color-bg-warm` |
| `#f9f9f9` | 聲明區背景 | `--color-bg-disclaimer` |

### 文字色

| 色碼 | 用途 | CSS 變數 |
|------|------|---------|
| `#2C2C2C` | 主文字 | `--color-text` |
| `#555555` | 次要文字 | `--color-text-light` |
| `#666666` | 更淡文字 — caption | `--color-text-muted` |

## 字型組合

| 用途 | 字型 | 權重 |
|------|------|------|
| 標題 (h1-h6) | Playfair Display (serif) | 600-700 |
| 內文 | Noto Sans TC (sans-serif) | 300-700 |

### 字型大小尺度

```
Display:  52px  — 臨床數據大數字
H1:       56px  — Hero 主標題
H2:       42px  — Section 標題
H3:       28px  — 卡片標題
H4:       20px  — 特色標題
H5:       16px  — 小標題
Body-lg:  17px  — FAQ / 產品描述
Body:     15px  — 一般段落
Small:    14px  — 導航 / caption
XS:       10-11px — Logo 副標
```

## 設計原則

1. **優雅克制** — 最多使用 3 種顏色（主色 + 金色 + 中性灰），不使用過多裝飾
2. **留白充裕** — Section padding 80px，Grid gap 30px，元素間距寬鬆
3. **細節精緻** — 圓角 12px、陰影淡而柔、邊框 1-2px、hover 帶品牌色陰影
4. **層級清晰** — 深背景（footer）→ 白背景 → 奶油背景 → 淺灰背景，交替使用
5. **動效輕柔** — fadeInUp 0.6s、hover translateY(-5px)、transition 0.3s ease
6. **襯線對比** — 標題用襯線體營造高級感，內文用無襯線體保持中文可讀性

## 陰影系統

| 層級 | 值 | 使用場景 |
|------|-----|---------|
| xs | `0 2px 8px rgba(0,0,0,0.05)` | 基礎卡片、FAQ |
| sm | `0 4px 15px rgba(0,0,0,0.06)` | 品牌故事價值卡 |
| md | `0 4px 15px rgba(0,0,0,0.08)` | 標準卡片、產品卡 |
| lg | `0 8px 30px rgba(0,0,0,0.08)` | 引言卡片 |
| hover | `0 8px 25px rgba(139,26,46,0.15)` | hover 帶品牌色 |

## 圓角系統

| 層級 | 值 | 使用場景 |
|------|-----|---------|
| sm | 8px | FAQ item、小按鈕 |
| md | 10px | 聯絡方塊 |
| lg | 12px | 產品卡片、stat 卡片 |
| xl | 16px | 引言卡片 |
| pill | 25-30px | 膠囊按鈕 |
| circle | 50% | 圓形圖示 |

## RWD 斷點

| 斷點 | 說明 | 主要變化 |
|------|------|---------|
| 1400px+ | 大螢幕 | container 1320px、H1 64px |
| 992px | 平板分界 | Grid 改 2 欄、footer 單欄 |
| 768px | 手機分界 | 漢堡選單、Grid 改 1 欄、section padding 50px |
| 480px | 小手機 | Hero 縮小、字型縮小、padding 縮小 |

## 外部依賴

```html
<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;600;700&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet">

<!-- Font Awesome (icons) -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
```

## 檔案清單

- `variables.css` — CSS 變數定義 + 基礎重置 + 共用元件樣式
- `README.md` — 本說明文件
- `preview.html` — 風格預覽頁（9 個模組完整展示）

## 萃取來源

從 BIOXCIN 台灣官網（bioxcintw.com）的 `css/style.css` + `index.html` inline styles 萃取。涵蓋 CSS 變數定義、所有色碼、字型大小、間距、圓角、陰影等 design tokens。
