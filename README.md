# robosys

ロボットシステム学の課題1のリポジトリ

# 開発環境:
* Rasberry Pi3
  * ubuntu20.04

# 使用機器
* PC(ubuntu18.04を使用)
* Rasberry Pi 3
* HDMIケーブル
* LANケーブル
* ブレッドボード
* LED×1
* 抵抗100Ω
* 圧電ブザー
* ジャンパー線

# 配線
gpio25ピンから抵抗、LEDと圧電ブザー、GNDピンの順に配列する。

![](https://lh3.googleusercontent.com/djGr50s7JCHUsFOD3r2aYdzRQE1s4wWumOpIDoSAnVMYrCLV8fnCsTNJWdTdL7-yGFwPuKwYIdZKYy6JGzHsmGCJtgCNClYYOMoFlz17)
![](https://lh3.googleusercontent.com/G9CgZZSwJNgv6Y6Hd8fIjQkd5uOVv7E9u5gnbNJCJao32J0oTpG5-ZiQ9J9cQWBVUKUvyjYQ1n4xrEsWjjsy-zHeX3fw6VfscR-YQb-olQ)

# 動作方法
 ```
 sudo insmod myled.ko
 ```
 ```
 sudo chmod 666 /dev/myled0
 ```
点灯
 ```
 echo 1 > /dev/myled0
 ```
 消灯
 ```
 echo 0 > /dev/myled0
