# myled
ロボットシステム学にて使ったデバイスドライバ

# 内容
ロボットシステム学第7~8回にて製作したデバイスドライバーです。講義で製作した物と動きは一致していますが、少しプログラムを書き換えています。具体的には、77行目の「ioremap_nocache」の部分を「ioremap」に変えています。

# 必要な物
Raspberry Pi 400
ブレッドボード×1
ジャンパー線×2
抵抗(φ5)×1
LED(白)×1
40pin I/O Protector ×1

# 回路
Raspberry Pi 400 GPIOピン配置
![20210821150645](https://user-images.githubusercontent.com/95558214/149341948-528e38e4-29be-4e05-8a4b-0754422b69d0.png)
今回はLEDもアノード側をGPIOの25番に、カソード側をGPIOの39番に差し込んでいます。

# 前準備
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0

# 実行
$ echo 1 > /dev/myled0
このコマンドによってLEDが光り続けます。
$ echo 0 > /dev/myled0
このコマンドによってLEDの光を消します。

# 動画
https://youtu.be/AeP_80_LSAQ
youtubeに動画を上げてあります。

# 参考リンク
GPIOピン配置
https://www.bioerrorlog.work/entry/raspberry-pi-pinout
