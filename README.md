[README.md](https://github.com/user-attachments/files/34405252/README.md)
# Alicia Li｜UI/UX Designer Portfolio

李思萱（Alicia Li）的個人作品集網站，收錄 B2B 雲端後台、行動 App 與品牌官網的設計案例，以及工作經歷、專業能力與聯絡方式。

## 精選專案

| 專案 | 類型 |
| --- | --- |
| Ushow 雲端後台 | B2B 後台系統 |
| MEELO 興趣社交 App | 行動 App・興趣社交 |
| BUS+ 交通規劃應用程式改版 | 行動 App・交通規劃 |
| Ushow 官方網站重構 | 品牌官網 |

## 網站功能

- 響應式單頁版面，手機版提供可收合的導覽選單。
- 支援淺色與深色模式。首次載入依系統偏好顯示，手動切換後使用 `localStorage` 記住設定。
- 背景音樂由訪客手動播放或暫停。
- 聯絡表單將姓名、電子郵件與訊息送至 Google Apps Script Web App。

## 技術架構

| 項目 | 實作 |
| --- | --- |
| 頁面與互動 | HTML5、CSS、原生 JavaScript |
| 版面與主題 | Tailwind CSS（CDN） |
| 字型與圖示 | Google Fonts（Inter）、Font Awesome 6.4.0 |
| 圖片與音訊 | 外部網址載入 |
| 表單串接 | Google Apps Script Web App |

## 本機預覽

1. 將網站 HTML 存為 `index.html`，與本文件放在 repo 根目錄。
2. 在瀏覽器開啟 `index.html`。如需透過本機 HTTP 預覽，可在該目錄執行下方指令，再開啟 [http://localhost:8000](http://localhost:8000)。

```bash
python3 -m http.server 8000
```

這是單一 HTML 靜態頁面，無需安裝 npm 套件或執行建置。完整的樣式、字型、圖示、圖片與音訊需連線載入。

## 聯絡表單設定

若要在自己的部署啟用表單，請將 `index.html` 中的 `scriptURL` 換成自己的 Google Apps Script Web App 網址。前端會以 `POST` 傳送包含 `name`、`email`、`message` 的 JSON 字串。

目前請求使用 `mode: 'no-cors'`，瀏覽器無法讀取伺服器的回應狀態。驗證表單時，請在 Apps Script 端確認測試訊息是否實際收到。

## 作者

Alicia Li（李思萱）｜UI/UX Designer
