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
- current limit 
