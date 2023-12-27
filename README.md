# robosys2023

# リポジトリ概要
ロボットシステム学課題提出用リポジトリ

# インストール方法
* ターミナルを開いた後、以下のコマンドにクローンします.

``` 
git clone https://github.com/Namashikate/robosys2023.git 
```
* クローンをした後、ディレクトリ"robosys2023"に移動します.

``` 
cd robosys2023 
```

# plusコマンド
![test](https://github.com/Namashikate/robosys2023/actions/workflows/test.yml/badge.svg)

標準入力から読み込んだ数字を足した後、合計値が偶数か奇数かを判別します.

* 使用方法

```
seq n | ./plus
S (偶数or奇数)
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
