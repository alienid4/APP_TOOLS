# APP_TOOLS

公開的小工具包，給網路受限的公司電腦直接下載 zip 使用。**這裡不放任何公司真實 IP、帳號、密碼或資料。**

| # | 工具 | 檔案 | 版本 | 用途 |
|---|---|---|---|---|
| 1 | FtpCollect | FtpCollect_py.zip | v1.0.2（2026-10-30） | 雙擊 run.bat 開視窗，帳號、密碼、目錄都在視窗設定；FTP 主機一對多唯讀收集 Serv-U／FileZilla 設定檔與 log（MFT 盤點用）；需 Windows＋Python 3.10+ |
| 2 | BinMailPacker（Python 版） | BinMailPacker_py.zip | v1.2.0（2026-10-30） | 檔案壓縮＋加密＋切成 .bin，讓 Gmail 寄得出去；有 Python 用這包（雙擊 run.bat） |
| 3 | BinMailPacker（exe 版） | BinMailPacker_exe.zip | v1.2.0（2026-10-30） | 同上，沒有 Python 的電腦用；兩版加密格式相同、可互解 |
| 4 | FtpCollect（PowerShell 版） | FtpCollectData_v1.2.1.zip | v1.2.1（2026-11-12） | **主機沒有 Python 用這包**（v1.2.1：跑完可自動用 FTP 上傳結果（填 ftpid.txt，遠端自動建「日期／結果資料夾」、逐檔核對大小、預設限速每秒 2 MB；不在主機上壓縮）；結束時印出總時間與各段時間；v1.2.0：快速模式，FileZilla log 精簡與 log 統計快約 10 倍、結果完全相同，預設讀滿 90 天；主機不允許時自動改一般模式並維持 1 GB 上限；log 日期認得「上午／下午」；讀大 log 時每 5 秒顯示進度與約剩幾分鐘；讀取上限以整天為單位；v1.1.10 起認得中文地區設定的 FileZilla 0.9 log 時間「上午／下午」；支援 Serv-U；FileZilla log 預設精簡複製，大幅縮小且報表次數不變；-MaxLogGB 可設讀取上限，超過就標「log 抽樣」；須搭配 FtpReport v0.9.16 以上）：在 FTP 主機本機以系統管理員身分雙擊 run.bat，唯讀收集 Serv-U／FileZilla 設定檔（遮密碼）、近 90 天 log（遮密碼）、帳號目錄與第一層子目錄摘要（只算 90 天內，不含完整檔名）、證據品質、版本／監聽埠／憑證／防火牆／排程；結果分 OK／PARTIAL／FAIL；不刪除、不修改主機任何東西 |
| 5 | FtpReport | FtpReport_v0.9.16.zip | v0.9.16（2026-11-12） | 認得 FileZilla 0.9 中文「上午／下午」時間； 認得「log 抽樣」主機，沒看到活動判證據不足、不判沒在用； 支援精簡 log 與分段檔（須 FtpCollect v1.1.7 以上收的結果最準）； 多來源一行一個； 列ID 移到最右（AP 版隱藏）； 每目錄列出動到它的伺服器； 主機系統對照可填網段、跳板機排除； 只呈現證據、以 AP 回填為準；同名帳號橘色、多台伺服器登入（待 AP 確認是否同一系統）紅色；部門統計、共用／同名清單、每帳號目錄數； v0.9 起可另放「帳號對照*.csv」補部門／保管人，並標出測試帳號； 支援 Serv-U log（上傳／下載／失敗、來源 IP、協定）；有員編／部門／姓名欄與「部門統計」（各部門帳號數，有在用／沒在用帳號直接列出是誰）； 把 FtpCollect 各主機的結果資料夾整理成盤點報表（可另放主機對照 CSV 填機房／環境並比對人工盤點）：SP 版／AP 版 Excel（主表、使用明細、移轉對照表、主機、說明）＋一頁總覽網頁（可排序、可點進明細）；只讀結果資料夾、不改任何東西；需 Python 3.8+，不用另外安裝套件 |
| 6 | ScreenAnytime 收集＋報告 | ScreenAnytime_SA_v1.3.1.zip | v1.3.1（2026-11-12） | v1.3.1：一律以名單欄位為準，人員分配到哪台，那台就算新主機。v1.3.0：總覽加磁碟水位與集中儲存水位圖（回推＋預估、85% 線）；圖表標百分比；sysinfra／Administrator 不列入計算。v1.2.0：移轉頁新主機表（主機／部門／使用率／已使用／未使用＋合計，點數字看名單）；容量頁加「到 85% 預估幾天（日期）」。v1.1.0：報告直接讀規劃 Excel（放在 SA_Report 同一層，改 Excel 重跑即生效）；同步落差改看 7 天合計；不再用服務狀態判紅燈。v1.0.2：工號被 Excel 吃掉開頭 0 會自動補回 8 碼；v1.0.1：側錄服務只在全部停止時才警示；run_ 資料夾放 SA_Report 底下任何位置都讀得到。兩支 PowerShell 5.1（免裝 Python）：SA_Collect 在每台跳板機與集中錄影主機以系統管理員雙擊 run_collect.bat，唯讀收集磁碟使用率、錄影資料夾大小、每主機×帳號×日錄影量、側錄服務狀態（OK／PARTIAL／FAIL，不開錄影、不改不刪）；SA_Report 讀各台結果產生一頁分頁網頁：移轉率（依部門／新主機／每日趨勢）、未移轉名單、容量與幾天會滿、本機與集中端同步落差、例外待核實、收集狀況。人員／主機對照表含公司資料，不在包內 |

下載：點檔名 → 右上「Download raw file」，或
`https://github.com/alienid4/APP_TOOLS/raw/main/<檔名>`

使用說明在各 zip 裡（FtpCollect：使用說明.txt；BinMailPacker：README.txt）。
