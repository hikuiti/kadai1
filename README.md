# myled
ロボットシステム学にて使ったデバイスドライバ

# 内容
ロボットシステム学にて作成したプログラムです。

右から順番に点灯するようにプログラムされています。

# 必要な物
Raspberry Pi 400

ブレッドボード×1

ジャンパー線×7

抵抗(φ5)×3

LED(白)×1

LED(赤)×1

LED(黄)×1

40pin I/O Protector ×1

# 回路
Raspberry Pi 400 GPIOピン配置

![20220114_11205](https://user-images.githubusercontent.com/95558214/149440665-88b4cd31-d495-4513-b57b-fff6bb37fbdf.jpg)


今回のLEDの配置は、

GPIO25 > 22ピン > 赤色LED

GPIO21 > 40ピン > 白色LED

GPIO20 > 38ピン > 黄色LED

の後、すべてをGND(39ピン)につなげています。



# 前準備
$ make 

$ sudo insmod myled.ko 

$ sudo chmod 666 /dev/myled0 

$ chmod +x blink.py 

$ python blink.py


# 実行
$ python blink.py　を実行した際に点滅を始めます。

ctrl + c を押すと停止します。



# 動画
https://youtu.be/lsic9aX-Dgg

youtubeに動画を上げてあります。

# 参考リンク
GPIOピン配置

https://www.bioerrorlog.work/entry/raspberry-pi-pinout

https://github.com/yurinishio1139/myled

# ライセンス
[GNU General Public License v3.0](https://github.com/hikuiti/kadai1/blob/main/LICENSE)

