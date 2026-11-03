# SBOM 軟體物料清單｜人工智慧應用實務研習班第1期 網頁

- 產出日期：2026-11-03（115年11月3日）
- 範圍：`index.html`（主網頁）、`ai-course-draw/index.html`（報告順序抽籤）、`ai-course-feedback/index.html`（課程回饋）
- 主網頁只用原生 HTML／CSS／JavaScript 寫成（含 Canvas 動畫），沒有使用任何第三方元件或外部資源。
- 機器可讀版本：`sbom.cdx.json`（CycloneDX 1.5）

## 一、第三方程式元件

| # | 元件 | 版本 | 授權 | 作者／維護者（所在地） | 用途 | 使用頁面 | 載入來源 |
|---|------|------|------|------|------|------|------|
| 1 | jsPDF | 2.5.1 | MIT | James Hall／yWorks GmbH（英國／德國） | 產生 PDF | 抽籤 | cdnjs（Cloudflare，美國） |
| 1a | └ fflate（內含於 jsPDF） | 0.4.x | MIT | Arjun Barrett（美國） | PDF 壓縮 | 抽籤 | 同上 |
| 2 | html2canvas | 1.4.1 | MIT | Niklas von Hertzen（芬蘭） | 將結果表轉為圖片放進 PDF | 抽籤 | cdnjs（Cloudflare，美國） |
| 2a | └ css-line-break、text-segmentation、utrie、base64-arraybuffer（內含） | 2.1.0／1.0.3／1.0.2／1.0.2 | MIT | Niklas von Hertzen（芬蘭） | 斷行、文字處理 | 抽籤 | 同上 |

說明：jsPDF 的選用相依套件 canvg、dompurify 只在使用 `.html()` 或 SVG 功能時才會載入，本頁未使用，所以不會載入。

## 二、字型
- 使用作業系統內建字型：Microsoft JhengHei 微軟正黑體（Windows）／PingFang TC（macOS、iOS），不另外下載字型。
- **已移除** Google Fonts「Noto Sans TC」。這套字型源自思源黑體（Source Han Sans），由 Adobe 與 Google 主導開發，但字形設計合作廠商之一為中國大陸常州華文（Changzhou SinoType）。

## 三、外部服務與資源
| 項目 | 提供者 | 說明 |
|------|------|------|
| GitHub Pages | GitHub, Inc.（美國，Microsoft 旗下） | 網頁託管 |
| cdnjs | Cloudflare, Inc.（美國） | 提供上述 2 個 JS 函式庫 |
| reurl.cc 短網址 | reurl.cc（經營者待確認） | 只是回饋頁上的超連結和 QR Code 內容，網頁不會載入它的任何程式 |
| QR Code 圖片 | 使用者提供 | 以 base64 內嵌在 html 中 |

## 四、瀏覽器內建功能（不屬於第三方元件）
Web Audio API（背景音樂、音效）、Web Crypto `crypto.getRandomValues`（亂數抽籤）、Clipboard API（複製網址）。

## 五、確認結果
- 兩個網頁的程式元件、字型及託管、CDN 服務，都沒有來自中國大陸的廠商或元件。
- 程式不蒐集、也不送出任何個人資料；抽籤結果只存在當下的瀏覽器畫面中。
- 待確認：reurl.cc 的經營者及所在地沒有公開資料可查證。如有疑慮，建議改用回饋表單的原始網址，或機關自己的短網址服務。

## 六、完整性雜湊（SHA-256，npm 官方套件檔）
- jspdf.umd.min.js：`98ccf17aa10c20bb1301762618fcc9b6ab3a4e7f26b6071d64d0b41154df3875`
- html2canvas.min.js：`e87e550794322e574a1fda0c1549a3c70dae5a93d9113417a429016838eab8cb`
