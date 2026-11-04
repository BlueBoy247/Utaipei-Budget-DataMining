# Utaipei-Budget-DataMining
此為臺北市立大學公共事務學系「資料探勘」課程之期中專案。<br>
This is the midterm project of the course Data Mining.

## 簡介
本專案聚焦於**臺北市立大學校務發展基金**自**邱英浩校長於 2022 年 8 月（民國 111 年 8 月）上任以來**的財務盤體變革、預算編列趨勢及審定決算執行落差。

透過資料探勘技術，系統性擷取並交叉勾稽官方 **112～115 年度法定預算書**、**116 年度預算案書**，以及 **112～114 年度審計決算報告**（共 8 冊會計文獻），建構為**一頁式全互動財務治理研究白皮書**。

研究揭示本校五年間「**預算規模突破 20 億元**（+49.9%）」、「**審定短絀腰斬減半**（-52.8%）」、「**產學自籌款躍升為第二支柱**（佔比升至 25.3%）」與「**職能學院宿舍重大基建落實**（已執行 4.56 億元）」等關鍵轉型成果。

完整分析[請點此瀏覽](https://blueboy247.github.io/Utaipei-Budget-DataMining/)。

## 動機
臺北市議會於 10 月 27 日下午 5 時 11 分，完成 116 年度總預算案及附屬單位預算等預算審議（[ref](https://firstnews.tw/taipei/news/a_mvuwsazb_7ul084vy)）。任何的政策推動執行都需要足夠的經費支撐，身為臺北市立大學學生，希望能透過自邱英浩校長上任後至今，本校各年度的預算與決算資料，了解目前的校務發展狀況，並從提出的 116 年度預算案，觀察本校的未來規劃。

## 成果要求
與生成式 AI 協作，完成一項以網頁形式展示的作品。

## 使用工具
本專題使用 Antigravity IDE 進行開發，使用模型為 Gemini 3.8 Flash。

由於預決算書為 PDF 檔案，Gemini 使用 Python 撰寫資料處理程式，透過 venv 建立 Python 虛擬環境，並搭配 cffi、charset-normalizer、cryptography、pdfminer.six、pdfplumber、pillow、pycparser、pypdf、pypdfium2 套件進行資料處理。

成果部分，Gemini 使用 HTML 及 CSS 製作網頁，並使用 Chart.js 呈現視覺化圖表。

## 專案結構
```text
.
├── Budget/                 # 112~115 法定預算書與 116 預算案書
├── FinancialStatement/     # 112~114 決算書
├── index.html              # 一頁式互動財務治理研究白皮書（主要展示成果）
├── budget_data.json        # 官方預決算抽取結構化數據集（以千元 NTD 為單位）
├── chart.umd.min.js        # Chart.js 本地核心庫（確保 100% 離線可用）
├── school_seal.png         # 臺北市立大學透明背景校徽（Retina 高畫質）
├── school_seal.jpg         # 校徽備用相容檔
├── school_seal_rgb.png     # 校徽備用相容檔
├── requirements.txt        # Python 資料處理依賴套件清單
├── .gitignore              # Git 版本控制忽略設定檔
└── README.md               # 專案研究說明文件
```

## 本地預覽指南
複製本專案後，直接以任一現代瀏覽器（Chrome、Edge、Safari、Firefox）雙擊開啟 [`index.html`](index.html) 即可完整體驗。

## 著作權與致謝
* **Copyright © 2026 BlueBoy247. All rights reserved.**
* 專題研究、資料探勘與視覺化系統工程：**Antigravity** (Google DeepMind)
* 資料來源：[臺北市立大學會計室](https://account.utaipei.edu.tw/)（存取時間 2026.11.03）
    * [112 年度法定預算書](./Budget/教育局主管臺北市立大學校務發展基金112年度法定預算書.pdf)
    * [113 年度法定預算書](./Budget/教育局主管臺北市立大學校務發展基金113年度法定預算書.pdf)
    * [114 年度法定預算書](./Budget/臺北市立大學校務發展基金114年度法定預算書.pdf)
    * [115 年度法定預算書](./Budget/臺北市立大學校務發展基金115年度法定預算書.pdf)
    * [116 年度校務基金預算案書](./Budget/教育局主管臺北市立大學校務發展基金116年度預算案書.pdf)
    * [112 年度決算書](./FinancialStatement/112年度決算.pdf)
    * [113 年度決算書](./FinancialStatement/113年決算書.pdf)
    * [114 年度決算書](./FinancialStatement/114年決算書-查核版.pdf)
