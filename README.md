# 日期假期查詢器（POC）

一個單檔 HTML 小工具：輸入「國家/地區」與「日期」，即可查詢該日是否為公眾假期，並列出後續假期。資料來源為 [Nager.Date](https://date.nager.at) 公開 REST API。

## 這個 POC 做什麼

- 從 Nager.Date API 載入 200+ 個國家/地區清單。
- 依使用者選擇的國家與日期，查詢該日是否為公眾假期。
- 顯示假期名稱（含當地名稱）、類型（Public / Bank / School / …）、是否全國性、適用的州/省代碼。
- 顯示星期、是否週末、假期筆數。
- 列出接下來 5 個公眾假期。
- 支援深色 / 淺色主題切換，選擇會保存於 `localStorage`。

## 給誰用

- 需要快速確認某國某日是否為假期的一般使用者。
- 想評估 Nager.Date API 的開發者 / 團隊（POC）。
- 需要在不同主題（深色/淺色）下使用的使用者。

## 怎麼用

1. 直接用瀏覽器開啟 `index.html`（需網路連線）。
2. 在「國家 / 地區」下拉選單選擇國家。
3. 選擇日期，點擊「查詢」。
4. 右上角可切換深色 / 淺色模式。

或以本機伺服器啟動（避免部分瀏覽器的 CORS 限制）：

```bash
python3 -m http.server 8000
# 然後開啟 http://127.0.0.1:8000/index.html
```

## 技術

- 單一 HTML 檔（HTML / CSS / Vanilla JS），無建置步驟。
- 資料來源：`https://date.nager.at/api/v3`（AvailableCountries、PublicHolidays）。
- 主題偏好保存於 `localStorage`（key: `theme`）。

## 組員

- 謝宜庭
- （其他組員待補）
