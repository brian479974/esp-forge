# ESP32 Forge｜ESP32 鍛造坊

ESP32-S3（N16R8）互動式實作指南：即時腳位圖、32 個實驗、可在瀏覽器裡操作的模擬器、3D 開發板、逐行解說韌體的程式碼閱讀器，以及整理成好讀版本的晶片資料手冊。介面支援 11 種語言（含繁體中文）。

- **網站**：https://d-boy.markforged.tw/?lang=zh-TW（舊網址 brian479974.github.io/esp-forge/ 會自動轉過來）
- **部署**：推到 `main` 由 GitHub Actions 檢查（型別、lint、671 項測試）、建置並發布到 GitHub Pages（`.github/workflows/pages.yml`）。

## 來源與授權

本站以 Abderrehmen Gharsallah 的開源專案為基礎，兩者皆為 MIT 授權：

- 網站：[agharsallah/esp-labs-web](https://github.com/agharsallah/esp-labs-web)（匯入版本 `d716cc7`）
- 韌體：[agharsallah/esp-labs](https://github.com/agharsallah/esp-labs)（建置時取固定版本 `72f1fc1`，供程式碼閱讀器使用）

原作者的版權聲明保留在 [LICENSE](LICENSE)；原專案的完整說明在 [docs/UPSTREAM-README.md](docs/UPSTREAM-README.md)。
`docs-llm/esp32-s3/` 內的 ESP32-S3 參考文件為樂鑫（Espressif）原文，沿用上游專案的收錄方式，版權屬樂鑫。

## 與上游的差異

- 站名改為 ESP32 Forge／ESP32 鍛造坊（11 種語言的標題、頁首、首頁大標）。
- 頁尾加註原作者與原專案連結（MIT）。
- 部署改為 GitHub Pages（移除 Vercel 部署設定與上游的 issue／PR 管理流程）。
- 網頁設定不給搜尋引擎收錄（noindex）。

## 本機開發

需要 Node 24.14+ 與 pnpm 11（`corepack enable`）。韌體原始碼放在旁邊的資料夾：

```sh
git clone https://github.com/agharsallah/esp-labs.git ../esp-labs
pnpm install
pnpm dev      # http://localhost:5180
pnpm check    # 型別 + lint + 測試
pnpm build    # 輸出到 dist/
```
