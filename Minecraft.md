
建目錄

下載 server.jar

連點兩下 server.jar (第一次解壓縮)

修改 eula.txt eula=true

連點兩下 server.jar 安裝 (第二次才是安裝)

連點兩下 server.jar 執行 

查 IP

進入遊戲

輸入 IP

確認可以玩 退出離開 


-------------------
安裝模組

下載 Forge

連點兩下 安裝 server

連點兩下 安裝 client

forge1.12.2.14


C:\Users\C940\AppData\Roaming\.minecraft\resourcepacks







https://www.curseforge.com/
https://www.curseforge.com/minecraft/modpacks 模組包
https://download.curseforge.com/
https://minecraft.fandom.com/zh/wiki/Server.properties?variant=zh-tw

木綾的JAVA模組伺服器架設教學 模組安裝地圖跟換全教你

因為原版Minecraft只給最新版的伺服器所以要自行去下載
Forge下載:https://files.minecraftforge.net/net/minecraftforge/forge/
地圖模組網址:https://www.mediafire.com/file/zs77om...
https://www.curseforge.com/minecraft/mc-mods/journeymap/files/all
https://www.curseforge.com/minecraft/mc-mods/journeymap
https://mega.nz/file/GmRXkCTC#mqD125QqJfuprttTRpoYm6Wskg7l4Esd6JviUssqTVQ

伺服器設定介紹: https://minecraft.fandom.com/zh/wiki/Server.properties?variant=zh-tw
伺服器設定:(下面是我整理出來的設定留自己原本伺服器的上面兩行文字其他刪掉複製上去就OK了)
'''
spawn-protection=16
max-tick-time=60000
query.port=25565
generator-settings=
sync-chunk-writes=true
force-gamemode=false
allow-nether=true
enforce-whitelist=false
gamemode=survival
broadcast-console-to-ops=true
enable-query=false
player-idle-timeout=0
text-filtering-config=
difficulty=normal
spawn-monsters=true
broadcast-rcon-to-ops=true
op-permission-level=4
pvp=true
entity-broadcast-range-percentage=100
snooper-enabled=true
level-type=default
hardcore=false
enable-status=true
enable-command-block=true
max-players=20
network-compression-threshold=256
resource-pack-sha1=
max-world-size=29999984
function-permission-level=2
rcon.port=25575
server-port=25565
server-ip=
spawn-npcs=true
allow-flight=true
level-name=world
view-distance=10
resource-pack=
spawn-animals=true
white-list=false
rcon.password=
generate-structures=true
max-build-height=256
online-mode=false
level-seed=
prevent-proxy-connections=false
use-native-transport=true
enable-jmx-monitoring=false
motd=A Minecraft Server
enable-rcon=false
rate-limit=0
'''
















































NAT -> DMZ

OpenJDK 
https://docs.microsoft.com/zh-tw/java/openjdk/download

JAVA EDITION SERVER
https://www.minecraft.net/en-us/download/server


https://minecraft.fandom.com/wiki/Tutorials/Setting_up_a_server


伺服器 list
https://www.mc-list.xyz/

下載完後，新增一個資料夾，把下載的檔案server.jar移到新資料夾，然後在資料夾中建立一個執行檔，方法如下：
資料夾中按滑鼠右鍵→【文字文件】→【新增文字文件】→開啟新文字文件→貼上指令
  java -Xmx1G -Xms1G -jar server.jar nogui
【檔案】→【另存為...】→【檔案名稱:123.bat】→【存檔類型:所有檔案】→【編碼:ANSI】→【存檔】。如下圖
這個指令中的1G，如果電腦的記憶體RAM有8G以上，可以試著改成2G，若記憶體RAM太低，可以試著改成512M，如
  java -Xmx2G -Xms2G -jar server.jar nogui
  或
  java -Xmx512M -Xms512M -jar server.jar nogui













============================================
windows 11
============================================
1. 在桌面建立一個 "server" 資料夾

2. 下載 免費版 JAVA
	https://docs.microsoft.com/zh-tw/java/openjdk/download

3. 下載 伺服器
	https://www.minecraft.net/en-us/download/server
	https://piston-data.mojang.com/v1/objects/f69c284232d7c7580bd89a5a4931c3581eae1378/server.jar

4. 安裝 JAVA
	Windows	x64	msi	microsoft-jdk-17.0.4-windows-x64.msi

5. Minecraft_Init.bat

6. 右鍵 在終端中開啟 or 建一個 .bat 
	java -Xmx1024M -Xms1024M -jar server.jar nogui






============================================
raspberrypi
============================================








============================================
linux
============================================


============================================
google架設免費雲端伺服器
============================================


一、基本設定
1.創google帳號

2.進入google cloud platform免費試用並填寫資料
  https://console.cloud.google.com/?hl=...

3.設定基本資訊與硬體設備
  固定的外部IP要記下來

4.建立防火牆規則
  0.0.0.0/0
  tcp:25565

二、打開小黑窗輸入指令(記得按Enter)
  1.輸入sudo su
  2.輸入apt-get update
  3.輸入apt-get install default-jre
  4.輸入screen
  5.輸入cd /home
  6.輸入mkdir minecraft
  7.輸入cd minecraft

8.輸入wget (你要下載的伺服器端JAR網址)
  全版本 Server.jar下載連結：
  https://mcversions.net/

9.輸入java -Xms2096M -Xmx6144M -jar server.jar nogui
10.輸入vi eula.txt 
11.按insert然後把false改成true
12.按兩次Esc然後輸入:wq再按Enter
13.輸入java -Xms2096M -Xmx6144M -jar server.jar nogui
14.按ctrl+a+d 讓它在背景執行即可關閉小黑窗

三、下載WinSCP、putty並再次打開小黑窗
  1.輸入sudo -s
  2.輸入screen -dr
  3.輸入sudo chmod -R 777 /home/minecraft

WinSCP：
  https://drive.google.com/file/d/1p1Gn...

Putty：
  https://drive.google.com/file/d/1i0Ps...

4.記得Putty的key/parameter.../PPK...改成"2"
5.回到VM執行個體加入金鑰設定

四、打開server.propertie依照需求修改遊戲設定

五、開玩

備註：
一、如果遇到LINUX的問題不知道怎麼辦：
  1.輸入sudo su
  2.輸入shutdown -r now
  (直接重開機)
  3.輸入 cd /home
  4.輸入 cd minecraft
  輸入cd minecraft
  5.輸入 screen 
  6.輸入 java -Xms2096M -Xmx6144M -jar server.jar nogui
  7.再按 ctrl+a+d 讓他在背景執行不關閉
  8.之後輸入 screen -dr 可回到伺服器畫面
  9.每次要離開就記得按 ctrl+a+d 讓他在背景執行不關閉

二、伺服器基本指令
  http://hikari-solving.blogspot.com/20...

三、有遇到問題會繼續補充












