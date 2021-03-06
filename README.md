# 伺服器守護神

使用虛擬伺服器（VPS/虛擬主機）所以不能放乖乖？想放乖乖卻身處異地買不到？又或者想要乖乖以外的守護神？

不用擔心，因為伺服器守護神Server-Protecter能幫你解決這些問題－－放置乖乖，一鍵完成，不需再擔心各種問題（最少不會過期）。

#注意：本程式並非防毒軟件。

##安裝需求
在安裝之前，請先確認你的伺服器已經安裝了以下三個套件：

1. php5
2. php5-gd
3. sqlite3

##下載及安裝
你可以透過以下指令取得伺服器守護神的原始碼：

```bash
$ git clone https://github.com/dollars0427/Server-Protecter.git
```

若你的電腦沒有安裝Git，也可以從以下連結取得原始碼：
https://github.com/dollars0427/Server-Protecter/releases/tag/v1.0

下載完成後，請至/config目錄下將config.sample.ini其改名為config.ini:

```bash
$ cd ./config
$ mv config.sample.ini config.ini
```

再修改裡面的內容。這是伺服器守護神的設定檔，你可以在這裡設定你的資料庫檔案位置及管理者帳號密碼：

```ini
[sqlite]
sql_file = "../database/protecter.rdb"

[admin]
admin_username = "your_admin_username"
admin_password = "your_admin_password"
```

修改完畢後，再到/database目錄下將base.protecter.rdb改名為protecter.rdb（假設你的資料庫檔案為這個名字）

```bash
$ mv base.protecter.rdb protecter.rdb
```

完成後將所有程式碼檔案上傳至伺服器即可。

**注意！若資料夾權限不設定成網頁伺服器可讀取的狀態（例如擁有者及擁有者群組為www-data），程式將無法正常運作！**

##使用
在首頁，你可以自由選擇將喜歡的守護神（數量不限）放置在伺服器上。預設只有「好乖好乖」這位守護神能使用，若想要更多的守護神，可以到管理後台自行上傳。

管理後台位置：{伺服器地址}/login.php

輸入在conig.ini裡設定的帳號及密碼後即可進入。

##示範
如想觀看示範，可前往以下網址：http://protecter.sardo.work

##回報問題
如遇任何問題，歡迎在Issues進行回報。
