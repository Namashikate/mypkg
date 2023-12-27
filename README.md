# mypkg
[![test](https://github.com/Namashikate/mypkg/actions/workflows/test.yml/badge.svg?branch=lesson11)](https://github.com/Namashikate/mypkg/actions/workflows/test.yml)

# リポジトリ概要
ロボットシステム学課題2提出用リポジトリ

# インストール方法
* ターミナルを開いた後、以下のコマンドにクローンします.

``` 
git clone -b lesson11 https://github.com/Namashikate/mypkg.git 
```
# 使用するノード説明
## mypkg
* talker.py
パブリッシャー。0.5秒ごとに数字を1カウントし、`/countup`トピックを通してメッセージを送信する。
* listener.py
サブスクライバー。`/countup`トピックからのメッセージを受け取り表示する。
## launch
*talk_listen.launch.py
`talker.py`と`listener.py`を同時に実行し表示する。

# 使用方法
## talker.pyとlistener.pyを使った方法

```
端末1$ ros2 run mypkg talker
端末2$ ros2 run mypkg listener
[INFO] [1703656832.069725697] [listener]: Listen: 82
[INFO] [1703656832.505912489] [listener]: Listen: 83
[INFO] [1703656833.005927325] [listener]: Listen: 84
[INFO] [1703656833.506021493] [listener]: Listen: 85
[INFO] [1703656834.005683186] [listener]: Listen: 86
[INFO] [1703656834.505891763] [listener]: Listen: 87
[INFO] [1703656835.006010521] [listener]: Listen: 88
```
任意の数nまでの合計値Sを計算し、偶数か奇数かの判別を行います.

* 具体的な使用例

```
seq 10 | ./plus
55 奇数
```

## 必要なソフトウェア
* Python
  * テスト済みver. 3.7～3.10

## テスト環境
* Ubuntu 22.04.2 LTS

## 著作権・ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードの一部は，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作とし、コードの一部を改変したものです．
	*  [ryuichiueda/robosys_2023](https://github.com/ryuichiueda/robosys2023)
* © 2023 Kaito Suzuki
