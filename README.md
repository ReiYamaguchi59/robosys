# robosys

ロボットシステム学の課題1のリポジトリ

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

# 開発環境:
* Rasberry Pi3
  * ubuntu20.04

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
 ```
 
  # ライセンス
 Copyright (c) 2021 Ryuich Ueda
 
 This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or any later version.
 
 This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.
