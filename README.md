# robosys

ロボットシステム学の課題1のリポジトリ

# 使用機器
* PC(ubuntu18.04を使用)
* Rasberry Pi 3
* HDMIケーブル
* LANケーブル
* ブレッドボード
* LED×1
* 抵抗1kΩ
* 圧電ブザー

# 開発環境:
* Rasberry Pi3
  * ubuntu20.04

# 配線
gpio25ピンから抵抗、LEDと圧電ブザー、GNDピンの順に配列する。

![](https://lh3.googleusercontent.com/5XVVP76mozH5nTRnFArJEeF2bGDebCs_uXAj4k6lGFsCxTR5IYqvNhHSX1PQAkgyDRVggLZUriQjCnwzPMu0rgWsjfyjzjbVlbw5-3d5hw)
![](https://lh3.googleusercontent.com/2YnfVsCZ_gcHF1fi-zvSBoEVayzknAahSlrE5Jc_n35a2a3pv_3jcnWK3qB2E025ehu3FLVgbLGCYQzTfgcwAuLlgM_veXAucifQ-w4Y)

# 動作方法
```
sudo rmmod myled
```
 ```
 sudo insmod myled.ko
 ```
 ```
 sudo chmod 666 /dev/myled0
 ```
LED点灯
 ```
 echo 1 > /dev/myled0
 ```
 ブザーを鳴らす
 ```
 echo 2 > /dev/myled0
 ```
 LED、ブザーを消す
 
 ```
 echo 0 > /dev/myled0
 ```
 
  # ライセンス
myled.c is under GNU General Public License v3.0(https://www.gnu.org/licenses/gpl-3.0.ja.html)
