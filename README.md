<a id="top"></a>

<div align="center">

<img src="assets/readme/readme-banner.svg" alt="揚琴演奏者個人網站 Eddie" width="100%">

<br>

[![GitHub 專案](https://img.shields.io/badge/GitHub-Eddie-1a2146?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jiachang1112/Eddie)
[![作者](https://img.shields.io/badge/%E4%BD%9C%E8%80%85-Jiachang1112-0b7a5c?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jiachang1112)
[![線上預覽](https://img.shields.io/badge/%E7%B7%9A%E4%B8%8A%E9%A0%90%E8%A6%BD-GitHub_Pages-222222?style=for-the-badge&logo=github&logoColor=white)](https://jiachang1112.github.io/Eddie/)

[![HTML5](https://img.shields.io/badge/HTML5-e34f26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572b6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-f7df1e?style=for-the-badge&logo=javascript&logoColor=1a2146)](https://developer.mozilla.org/docs/Web/JavaScript)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-7952b3?style=for-the-badge&logo=bootstrap&logoColor=white)](https://getbootstrap.com/)
[![Formspree](https://img.shields.io/badge/Formspree-e0234e?style=for-the-badge)](https://formspree.io/)
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-222222?style=for-the-badge&logo=github&logoColor=white)](https://pages.github.com/)

**揚琴演奏者的個人網站 ‧ 關於 ‧ 比賽經歷 ‧ 作品 ‧ 聯絡表單 ‧ 金色慶祝特效**

<br>

[![內容](https://img.shields.io/badge/%F0%9F%8E%B6_%E5%85%A7%E5%AE%B9-b45309?style=flat-square)](#-網站內容)
[![快速開始](https://img.shields.io/badge/%E2%9A%A1_%E5%BF%AB%E9%80%9F%E9%96%8B%E5%A7%8B-7c3aed?style=flat-square)](#-快速開始)
[![聯絡表單](https://img.shields.io/badge/%F0%9F%93%AC_%E8%81%AF%E7%B5%A1%E8%A1%A8%E5%96%AE-e0234e?style=flat-square)](#-設定聯絡表單)
[![發佈](https://img.shields.io/badge/%F0%9F%9A%80_%E7%99%BC%E4%BD%88-222222?style=flat-square)](#-發佈到-github-pages)
[![常見問題](https://img.shields.io/badge/%E2%9D%93_%E5%B8%B8%E8%A6%8B%E5%95%8F%E9%A1%8C-e34f26?style=flat-square)](#-常見問題)

</div>

---

## 🎶 網站內容

<div align="center">

<img src="assets/主圖.png" alt="網站主視覺" width="720">

</div>

<table>
<tr>
<td width="33%" valign="top">

### 🏠 首頁
深色背景搭配金色重點色，主視覺與一句話介紹，並提供「查看比賽經歷」與「聯絡我」兩個按鈕。

</td>
<td width="33%" valign="top">

### 👤 關於
介紹專長與興趣，以及指導老師、伴奏老師等合作夥伴。

</td>
<td width="33%" valign="top">

### 🏆 比賽經歷
依時間排列的比賽紀錄卡片，標示名次、組別與日期。

</td>
</tr>
<tr>
<td width="33%" valign="top">

### 🖼️ 作品
作品與演出相片的展示區。

</td>
<td width="33%" valign="top">

### 📬 聯絡
用 Formspree 收信的聯絡表單，送出後會出現金色慶祝動畫。

</td>
<td width="33%" valign="top">

### 🔎 SEO
加入 Schema.org 的 Person 結構化資料，讓搜尋引擎更容易了解這個人與專長。

</td>
</tr>
</table>

---

## 🧩 運作方式

```mermaid
flowchart LR
    V([👤 訪客]):::blue --> S[index.html<br/>單檔靜態網頁]:::green
    S --> A[關於 / 比賽經歷 / 作品]:::green
    S -->|送出聯絡表單| F[Formspree]:::pink
    F -->|轉寄| M([📧 站長信箱]):::blue
    S -->|成功| C[金色慶祝動畫<br/>Canvas confetti]:::orange

    classDef blue fill:#b45309,stroke:#451a03,color:#fff
    classDef green fill:#0b7a5c,stroke:#13332c,color:#fff
    classDef pink fill:#e0234e,stroke:#7a0f26,color:#fff
    classDef orange fill:#f9c65c,stroke:#8a5a00,color:#1a2146
```

- 整個網站是**一個 `index.html`**，樣式與腳本都在裡面，Bootstrap 從 CDN 載入。
- 主要顏色定義在檔案開頭的 CSS 變數（背景、文字、金色重點色），想換配色改這裡即可。

### 📁 檔案說明

```text
Eddie/
├── index.html      整個網站（HTML + CSS + JS）
└── assets/
    └── 主圖.png     首頁主視覺
```

---

## ⚡ 快速開始

```bash
git clone https://github.com/Jiachang1112/Eddie.git
cd Eddie
python3 -m http.server 8000      # 打開 http://localhost:8000/
```

**改成你自己的內容：** 直接編輯 `index.html` 裡「關於」「比賽經歷」「作品」區塊的文字，並更新檔案開頭 `<script type="application/ld+json">` 裡的結構化資料。

---

## 📬 設定聯絡表單

聯絡表單使用 [Formspree](https://formspree.io/)：

1. 註冊 Formspree 並建立一個表單，取得 `https://formspree.io/f/xxxxxxxx` 網址。
2. 把 `index.html` 裡 `<form id="contactForm" action="…">` 的 `action` 換成你自己的網址。
3. 第一次送出時，Formspree 會寄確認信到你的信箱，確認後才會開始轉寄。

---

## 🚀 發佈到 GitHub Pages

Settings → Pages → Source 選 `main` 分支的 `/ (root)`，約 1～2 分鐘後上線：[jiachang1112.github.io/Eddie](https://jiachang1112.github.io/Eddie/)。

---

## ❓ 常見問題

<details>
<summary><b>表單送出後沒收到信</b></summary>

先檢查 Formspree 後台是否已確認信箱，並看垃圾郵件匣。

</details>

<details>
<summary><b>相簿圖片是隨機圖片</b></summary>

目前作品區使用示意圖片，請換成你自己的照片並放進 `assets/`。

</details>

<details>
<summary><b>想換掉主視覺</b></summary>

替換 `assets/主圖.png`，或修改 `index.html` 裡對應的圖片路徑。

</details>

---

<div align="center">

[GitHub @Jiachang1112](https://github.com/Jiachang1112)　‧　[Eddie](https://github.com/Jiachang1112/Eddie)

[![回到最上面](https://img.shields.io/badge/%E2%AC%86%EF%B8%8F_%E5%9B%9E%E5%88%B0%E6%9C%80%E4%B8%8A%E9%9D%A2-7c3aed?style=for-the-badge)](#top)

</div>
