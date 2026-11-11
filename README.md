# APP_TOOLS

公開的小工具包，給網路受限的公司電腦直接下載 zip 使用。**這裡不放任何公司真實 IP、帳號、密碼或資料。**

| # | 工具 | 檔案 | 版本 | 用途 |
|---|---|---|---|---|
| 1 | FtpCollect | FtpCollect_py.zip | v1.0.2（2026-10-30） | 雙擊 run.bat 開視窗，帳號、密碼、目錄都在視窗設定；FTP 主機一對多唯讀收集 Serv-U／FileZilla 設定檔與 log（MFT 盤點用）；需 Windows＋Python 3.10+ |
| 2 | BinMailPacker（Python 版） | BinMailPacker_py.zip | v1.2.0（2026-10-30） | 檔案壓縮＋加密＋切成 .bin，讓 Gmail 寄得出去；有 Python 用這包（雙擊 run.bat） |
| 3 | BinMailPacker（exe 版） | BinMailPacker_exe.zip | v1.2.0（2026-10-30） | 同上，沒有 Python 的電腦用；兩版加密格式相同、可互解 |
| 4 | FtpCollect（PowerShell 版） | FtpCollect_ps_v1.1.4.zip | v1.1.4（2026-11-11） | **主機沒有 Python 用這包**（v1.1.4 起支援 Serv-U 帳號檔、log 位置自動判讀）：在 FTP 主機本機以系統管理員身分雙擊 run.bat，唯讀收集 Serv-U／FileZilla 設定檔（遮密碼）、近 90 天 log（遮密碼）、帳號目錄與第一層子目錄摘要（只算 90 天內，不含完整檔名）、證據品質、版本／監聽埠／憑證／防火牆／排程；結果分 OK／PARTIAL／FAIL；不刪除、不修改主機任何東西 |
| 5 | FtpReport | FtpReport_v0.3.zip | v0.3（2026-11-11） | 把 FtpCollect 各主機的結果資料夾整理成盤點報表（可另放主機對照 CSV 填機房／環境並比對人工盤點）：SP 版／AP 版 Excel（主表、使用明細、移轉對照表、主機、說明）＋一頁總覽網頁（可排序、可點進明細）；只讀結果資料夾、不改任何東西；需 Python 3.8+，不用另外安裝套件 |

下載：點檔名 → 右上「Download raw file」，或
`https://github.com/alienid4/APP_TOOLS/raw/main/<檔名>`

使用說明在各 zip 裡（FtpCollect：使用說明.txt；BinMailPacker：README.txt）。
