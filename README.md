# Trash Game

一些沒什麼營養的小網頁遊戲，用 GitHub Pages 發佈。每款遊戲各自放在一個資料夾，彼此獨立，沒有建置步驟。

| 遊戲 | 資料夾 | 網址 |
| --- | --- | --- |
| 被被撐住 | [`beibei/`](beibei/) | https://stevenchiang88.github.io/trash_game/beibei/ |
| 絕命電師 | [`dianshi/`](dianshi/) | https://stevenchiang88.github.io/trash_game/dianshi/ |
| 絕命礦師 | [`kuangshi/`](kuangshi/) | https://stevenchiang88.github.io/trash_game/kuangshi/ |
| 我的豆花30塊 | [`douhua/`](douhua/) | https://stevenchiang88.github.io/trash_game/douhua/ |
| 我這一生如履薄冰 | [`bobing/`](bobing/) | https://stevenchiang88.github.io/trash_game/bobing/ |
| 純手打 Code | [`shouda/`](shouda/) | https://stevenchiang88.github.io/trash_game/shouda/ |

首頁（遊戲列表）是根目錄的 `index.html`：https://stevenchiang88.github.io/trash_game/

## 結構

```
trash_game/
├─ index.html     首頁，列出所有遊戲
├─ .nojekyll      讓 Pages 原樣提供檔案，不經過 Jekyll
├─ beibei/        被被撐住（遊戲、預覽圖、圖示、說明）
├─ dianshi/       絕命電師（遊戲、預覽圖、圖示、說明）
├─ kuangshi/      絕命礦師（遊戲、預覽圖、圖示、說明）
├─ douhua/        我的豆花30塊（遊戲、預覽圖、圖示、說明）
├─ bobing/        我這一生如履薄冰（遊戲、預覽圖、圖示、說明）
└─ shouda/        純手打 Code（遊戲、預覽圖、圖示、說明）
```

資料夾名稱就是網址，不需要任何路由程式。

## 新增一款遊戲

1. 開一個新資料夾，裡面放 `index.html`（遊戲本體）和 `og.png`（1200×630 的分享預覽圖）。
2. 在遊戲的 `index.html` 開頭寫好自己的 `<title>`、`og:title`、`og:description`、`og:url`、`og:image`、`canonical`，網址用 `https://stevenchiang88.github.io/trash_game/資料夾名稱/`。貼到 Threads、LINE 時的預覽卡片只讀這些標籤，所以每款遊戲都要有自己的一份。
3. 在根目錄 `index.html` 的 `<ul class="games">` 裡複製一個 `<li>`，換掉連結、圖片、標題和說明。
4. 存在瀏覽器裡的資料（例如最佳紀錄）所有遊戲共用同一個空間，key 記得加上自己的前綴，像被被撐住用的是 `bb.`、絕命電師用的是 `ds.`、絕命礦師用的是 `ks.`、我的豆花30塊用的是 `dh.`、我這一生如履薄冰用的是 `bi.`、純手打 Code 用的是 `sd.`。

## 部署到 GitHub Pages

1. 把檔案合併到 `main`。
2. repo 要是 public（免費帳號的 Pages 只支援 public repo）。
3. Settings → Pages → Source 選「Deploy from a branch」，分支選 `main`、資料夾選 `/ (root)`，按 Save。

之後每次合併到 `main` 都會自動重新部署，大約一分鐘後生效。
