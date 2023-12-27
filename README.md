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
* talk_listen.launch.py
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
## talk_listen.launch.pyを使った方法
```
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/kaito/.ros/log/2023-12-27-15-25-41-438554-yawarakanuma-1976
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [1977]
[INFO] [listener-2]: process started with pid [1979]
[listener-2] [INFO] [1703658342.381523022] [listener]: Listen: 0
[listener-2] [INFO] [1703658342.862671223] [listener]: Listen: 1
[listener-2] [INFO] [1703658343.362729020] [listener]: Listen: 2
[listener-2] [INFO] [1703658343.862536593] [listener]: Listen: 3
[listener-2] [INFO] [1703658344.363090467] [listener]: Listen: 4
[listener-2] [INFO] [1703658344.863053356] [listener]: Listen: 5
[listener-2] [INFO] [1703658345.363082941] [listener]: Listen: 6
```
## 必要なソフトウェア
* Python

## テスト環境
* Ubuntu 22.04.2 LTS
* ros2 Hunmble

## 著作権・ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードの一部は，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作とし、コードの一部を改変したものです．
	*  [ryuichiueda/robosys_2023](https://github.com/ryuichiueda/robosys2023)
* © 2023 Kaito Suzuki
