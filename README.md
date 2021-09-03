# Keyboard_H
This is My First Keyboard Project.

#### 自作キーボードの設計
このリポジトリは自作キーボードのためのリポジトリ。
ただしハードウェア設計に関するファイルのみ。うｐ主のインフラの事情的に、ハードは Windows ソフトは Ubuntu で開発することになってしまったので、ハードとソフトでリポジトリを分けた。
統合してぇなぁ...

##### メモ
- USB バスパワー:5V 500mA
- Raspberry Pi Pico の GPIO のパワー
- キーボード全体で 300mA になるようにしたい。
- USB 5V だが、実際 500 mA くらい使用すると 4.8V くらいに下がってしまうので、USB デバイスはそうならないように余裕を持たせて設計する。
- GPIO で FET のゲートを制御し、Vbus からの電力を供給する。
- LED と制限抵抗は必ず一つにまとめる。
- .
- output current 出力の最大値 MAX 100 mA
- current limit 制限電流 MIN 150 mA TYP 350 mA MAX 450 mA
- .
- LED の設定
- 一つの LED に電流制限可変抵抗と LED を直列に繋いだ回路において、デューティー比 100% という条件で以下の状態を記録。
- 電源電圧 5 V
- 抵抗降下電圧 1.692 V
- LED 電圧 3.17 V
- 電流 19.30 mA
- 抵抗値 84.5 Ω
- ※小数点以下一桁目より下は当てにならないかも... 0.1 レベルなら当てになるかも。
- 上記が丁度よい輝度になっている。
- .
- 参考までに、電源電圧 3.3 V の時の値も記録しておく。
- 抵抗降下電圧 0.267 V
- LED 電圧 3.03 V
- 電流 10.58 mA
- 抵抗値 21.2 Ω
- ※小数点以下一桁目より下は当てにならないかも... 0.1 レベルなら当てになるかも。
- .
- ついでのついでに参考として、データシートの値を記録しておく。
- デューティー比 100% 電流値  30 mA
- デューティー比 10 % 電流値 100 mA
- 20 mA の時の LED 電圧降下 3.1 V

