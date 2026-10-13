# CLAUDE.md

這是一個不用登入的匿名聊天室：網頁放在 GitHub Pages，即時傳訊用 Supabase。

## 開始任何工作前

先讀 [`docs/architecture.md`](docs/architecture.md)。所有技術決定、通訊約定、畫面清單和驗證清單都在裡面。需求原文在 [`docs/requirements.md`](docs/requirements.md)。

## 目前進度

**目前在「階段一」**：只做前端，使用假資料版（`MockChatService`），還沒有接上 Supabase。不要開始實作 Supabase 版，除非使用者明確說要進入階段二。

## 金鑰規則

- **不可以把金鑰檔案 commit 進 git。** `.env`、`.env.local` 以及其他 `.env.*` 都不能 commit，只有 `.env.example`（只有名稱、沒有值）可以。
- Supabase 的 Secret key（`sb_secret_...` / `service_role`）這個專案用不到，不可以出現在任何檔案裡。
- 開頭是 `VITE_` 的設定會被打包進網頁，只能放可以公開的值。
