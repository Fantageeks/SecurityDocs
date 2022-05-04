### Unix Command Usage:

* ping確認遠方機器是否可以連到: ping xxx.xxx.xxx.xxx / ping google.com(Domain:網域名稱) 
* ls -al : 列出目前的目錄與檔案
* clear : 清除目前螢幕資料
* cd 進入目錄: cd files
* mkdir建立目錄: mkdir files
* wget --no-check-certificate 連結 : 下載網站中的檔案下來
* cat file: 將檔案內容輸出到螢幕
* file filename: 知道檔案類型

####原理與觀念：
* ping google.com: (1)找到DNS(網域名稱伺服器)，查詢google.com對應的IP位置，再送出網路封包確認遠方機器是否存活
* ifconfig: 檢查目前的網路ＩＰ
* service ssh start: 啟動sshd伺服器，可以遠端登入
* netstat -ant: 看主機有開哪些的服務，哪些網路埠口

####Kali VM遠端登入：
* sudo service ssh start
* ifconfig 找到VM的IP
* 用putty遠端登入 (kali/kali)
* su (轉成root帳號)
* cd /root/Desktop/


####JPEG檔案：
＊圖片檔：秘密資訊都會藏在metadata中。
＊圖片檔: 壓縮檔案(zip file)
* wget --no-check-certificate https://exiftool.org/Image-ExifTool-12.41.tar.gz
* tar zxvf Image-ExifTool-12.41.tar.gz (解壓縮)
* cd Image-ExifTool-12.41
* perl Makefile.PL
* make test
* sudo make install
