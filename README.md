
# skills-introduction-to-git

本專案為一個教學用範例，展示 Git 與網頁前端基礎練習範例。內容以靜態網頁為主，方便學習者在本機打開或透過簡單伺服器查看與練習。

## 專案目的

- 提供一組可直接在本機操作的練習檔案，讓學習者練習 Git 操作（clone、branch、commit、pull request）以及簡單的前端檔案結構。

## 主要功能

- 靜態示範頁面：`src/index.html` 與相關資源。
- 範例 JavaScript：`src/index.js` 與 `src/patterns.js` 展示基本互動與程式範例。
- 本機測試與練習：可直接以瀏覽器開啟或啟動簡單 HTTP 伺服器檢視。

## 遊戲說明 — Stack Overflown

這個專案包含一個開發者主題的方塊拼圖遊戲（標題：Stack Overflown）。玩家要在 10×20 的棋盤上放置方塊（類似方塊下落遊戲），並嘗試在棋盤上形成緊接的 5×5 模式以配對目標錯誤圖案。

遊戲重點：

- 目標：配對畫面右側顯示的「Target Pattern」。
- 棋盤大小：10 列 × 20 行。每個方塊顯示為不同的顏色，代表不同的「程式語意」（例如 bug、function、string 等）。
- 方塊來源：隨機出現的方形、直條、單顆或特殊「void（黑色）」方塊。部分方塊（value 8）視為 void，對配對不算作實心方塊。

操作說明：

- 左右鍵（←/→）：移動方塊。
- 上鍵（↑）：旋轉方塊。
- 下鍵（↓）：軟下落（加速下降）。
- 空白鍵（Space）：硬下落（立刻落到底並固定）。
- P：暫停/恢復遊戲。

配對與計分：

- 每當新的方塊固定到棋盤並造成某處出現與目標 5×5 模式完全匹配的位置時，判定為配對成功。
- 配對成功會觸發：
	- 清空棋盤（現行實作會將整個棋盤重置為空）。
	- 得分 +100 分，並隨機選擇新的目標模式。
- 目前可出現的目標模式（示例）：`Null Pointer`, `Memory Leak`, `Off By One`, `Race Condition`, `Infinite Loop`, `Syntax Error`, `Type Mismatch`。

遊戲結束：

- 若剛生成的新方塊在頂部產生碰撞（表示堆疊到頂），遊戲結束並顯示最終分數，畫面提供重新開始按鈕。

實作備註（對想閱讀程式碼的貢獻者）：

- 主要邏輯位於 `src/index.js`，模式（patterns）定義在 `src/patterns.js`。
- 配對偵測：程式會掃描整個棋盤尋找能匹配 5×5 模式的位置；匹配條件會忽略值為 `8`（void）的方塊。

如果想要我調整遊戲機制（例如：改為只清除匹配區塊而非整個棋盤、增加分數計算方式或加入關卡／速度提升），我可以幫你修改程式碼並更新說明。

## 快速開始

1. 下載或 clone 專案：

```
git clone <repo-url>
cd skills-introduction-to-git
```

2. 直接在瀏覽器打開靜態頁面：

開啟 `src/index.html`（雙擊或瀏覽器開啟）。

3. 使用簡單 HTTP 伺服器（備選）：

Python 3:

```
python -m http.server 8000
# 然後在瀏覽器開啟 http://localhost:8000/src/index.html
```

或使用 Node.js 的簡易伺服器如 `npx serve`。

## 檔案結構

- `src/`：靜態資源目錄
	- `index.html`：示範主頁面
	- `index.js`：主程式邏輯與互動
	- `patterns.js`：範例程式片段或練習題
	- `style.css`：樣式表
	- `onlocal`：教材或本機練習相關檔案（說明見課程檔案）

## 貢獻

歡迎提出 Issue 或 Pull Request：

- 建議修改內容時請先建立分支，並在 PR 中描述變更目的。

## 授權

本專案依照專案根目錄的 `LICENSE` 檔案授權（請參見該檔案）。

---

如果你要我把 README 調整為英文版、加入更多範例或在 `src/index.html` 加入使用說明，我可以繼續幫你修改。

