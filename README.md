# ROS2を用いての、ノード間の連携を確認

## 何をするためのソフトか
* 予め決めておいた値を、ノード間で送受信できているかを確認するものです。

## 必要なソフトウェア
* python

## 動作確認済み環境
* ubuntu22.04

## 簡単な使い方
### 二つあります。
* `ros2 run mypkg talker`を端末で立ち上げて行った後に<br>
`ros2 run mypkg listener`をもう一つの端末を立ち上げて行う。
	* 実行結果<br>
	  [INFO] [1671245591.045926600] [listener]: age: 19

* 上記のコマンド順序を入れ替えて行う。
	* 実行結果<br>
	  [INFO] [1671245733.760671800] [listener]: 待機中<br>
	  [INFO] [1671245734.763645700] [listener]: 待機中<br>
	  [INFO] [1671245735.769432800] [listener]: age: 19<br>

* どちらも同じものを出力するもので、待機中が入るか入らないかの違いです。

## 型の名前とデータについて
* 型の名前はQuery
* データは
	* string name<br>
	---<br>
	uint8 age<br>

## LICENSE・使用しているコードについて
* このソフトウェアパッケージは、3条項ライセンスの下、再頒布および使用が許可されます。
* このパッケージのコードは、下記のスライド(CC-BY-SA 4.0 by Ryuichi Ueda) のものを、本人の許可を得て自身の著作としたものです。
	* [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2022 Souta Kobori
