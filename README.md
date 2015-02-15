Comic Crawler
=============

Comic Crawler 是用來扒圖的一支 Python Script。擁有簡易的下載管理員、圖書館功能、
與方便的擴充能力。

Todos
-----
* 加入連結 > 取消無效
* 下載時刪除無效
* 移除 tkinter root 前要移除 safeprint hook
* On duplicate mission: Ask for re-analyzing ep list.
* Add "Open folder" to context menu.

下載和安裝（Windows）
-------------------

### Python

你需要 Python 3.4 以上。安裝檔可以從它的[官方網站](https://www.python.org/)下載。
	
安裝時記得要選「Add python.exe to path」，否則安裝 PyExecJS 時會找不到 `pip` 命令。
	
### PyExecJS

[PyExecJS](https://pypi.python.org/pypi/PyExecJS) 是 Python 的套件，用來執行 JavaScript。裝完 Python 後在 cmd 底下直接用 pip 指令

	pip install pyexecjs
	
### Comic Crawler

直接從 Github 下載原始碼就能執行了。點右方的「Download ZIP」按鈕。

## 目前支援網址

> manhua.dmzj.com, www.dm5.com, g.e-hentai.org, konachan.com, chan.sankakucomplex.com, exhentai.org, www.99comic.com, www.8comic.com, comic.ck101.com, comic.sfacg.com, deviantart.com, comic.example.com, www.pixiv.net, tel.dm5.com, www.example.com

## 命令介面

Comic Crawler 的核心就是個可以載入 module 的扒圖工具。基本命令只有兩個。

### 列出支援的網址

	comiccrawler.py domains

### 下載網址內的漫畫至特定目錄

	comiccrawler.py download URL -d FILE_PATH

## 圖形介面

### 下載

執行comiccrawlergui.py，貼上連結後點「加入連結」，若是程式支援的網址，在復製完後切換到 Comic Crawler 的視窗就會自動貼上。貼上後按 Enter 也可以加入連結。加入連結後點「開始下載」就會自動下載到指定資料夾中了。

### 圖書館

對著任務右鍵，可以選擇把任務加入圖書館。圖書館內的任務，在每次程式啟動時，都會檢查是否有更新。也可以手動點選「檢查更新」。點「下載更新」會把顯示「有更新」的任務加到下載列表裡面，並自動開始下載。

### 設定檔（setting.ini）

第一次執行程式時會在同目錄下產生 setting.ini，可以設定...

	savepath = 下載目錄。
	runafterdownload = 下載完後欲呼叫的程式，會傳入任務資料夾位置。
	libraryautocheck = 是否要自動檢查圖書館更新

`zip.bat` 是預先寫好的 Windows 批次檔，會呼叫 7z 命令將檔案壓縮後刪除資料夾（小心！）。與 `runafterdownload` 配合使用。

## 聮絡作者

eight04@gmail.com


