# 日日提醒

[開啟獨立的 GitHub Pages 網頁](https://pininca68-web.github.io/personal-weekly-reminder/)

獨立的個人每週提醒頁。週一到週日可複選，並提供每天、平日（週一到週五）、週末（週六、週日）的快捷設定。國定假日不會自動套用。

可設定每天一次，或在所選時間範圍內每 30 分鐘、1／2／3／4 小時提醒。所有時間皆為台北時間（UTC+8）。提醒由下一個未來時間開始，錯過的時段不會連續補發。

設定僅保存在目前瀏覽器的 `personal-weekly-reminder.v1`。本工具不使用定位、帳號、家庭資料、第三方 App 使用情況或雲端資料服務，也沒有資料匯出或行為歷史功能。

分頁內提醒不需通知權限；桌面通知需本人按鈕允許。請保持分頁開啟。關閉分頁後不會提醒，背景分頁、休眠與瀏覽器暫停也可能略過提醒。本工具不適合作為必須準時觸發的重要警報。

## 使用

開啟 `personal-reminder.html` 即可使用，也可將 `dist/` 裡的 `index.html` 和 `.nojekyll` 放在獨立的 GitHub Pages 儲存庫根目錄。網站不需要安裝任何套件或連接外部服務。

本機檔案與網站網址使用各自的瀏覽器儲存空間，設定不會在不同網址或裝置之間同步。

## 驗證與重新產生檔案

```text
node tests/schedule.test.cjs
node build.cjs
```

`src/schedule.js` 為獨立排程邏輯；`src/app.js` 為畫面互動；`src/template.html` 和 `src/ui.css` 為頁面與樣式。所有資源會內嵌至單一 HTML，不含外部字型、分析或第三方程式。
