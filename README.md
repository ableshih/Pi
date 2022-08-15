# Pi樹莓派
#image
  image to SD
# 開終端機
  預設帳號 pi 密碼 raspberry
  raspi-config 環境設定
# 指令
  date 時間
  cal 行事歷
  df 查 SD 空間
  free 查記憶體
  exit 關終端機
  shutdown -h now 立即關機
  ls (dir)
  cp (copy)
  mv (move)
  rm (del)
  nano filename.txt 文字編輯器
  mkdir 建目錄
  chmod 664 filename.txt (檔案權限 r.w.x)
  passwd 舊 新 新 (改密碼)
  sudo apt-get update
  sudo apt-get upgrade
  host name 查看 IP addr.

# 開機自動執行
  sudo nano /etc/rc.local
  在第一行加入
  /usr/bin/python /home/pi/hmtt.py
  $ sudo apt-get update$ sudo apt-get upgrade$ sudo apt-get dist-upgrade$ sudo rpi-update$ sudo reboot
  kernel version checkuname -a

# 硬體比較
  https://3q.9527.tw/123

# 樹莓派4問題USB-C無法充電
  調整 SD 大小
  樹莓 icon
  偏好設定
  GParted
  調整
  套用所有動作
  會 自動重開機 

# 忘記密碼
  將樹莓派關機，移除sd卡，插入到你的電腦。在PC上打開SD卡根目錄，啟動部分是可見的，並包含一個名為“cmdline.txt”的文件。用編輯軟體編輯，於內容最後加入 init=/bin/sh保存，將sd卡插入樹莓派mount -o remount, rw /passwd piEnter new UNIX password:Retype new UNIX password:passwd: password updated successfullysyncexec /sbin/init樹莓派會繼續啟動，然後關掉樹莓派並且斷電。sudo halt用電腦再次編輯“cmdline.txt” 刪除 init=/bin/sh 存檔插入sd卡到你的樹莓派啦，再次啟動就可以使用新的密碼啦。

# Raspberry Pi - 調整SD分割空間

# 安裝 ubnutu 要非常久，不建議
