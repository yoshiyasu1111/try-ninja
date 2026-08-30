# Try Ninja

Ninjaを試すためのサンプルプログラムです。

複数のC++ソースコードとヘッダーファイルからなる簡単なプログラムを、`build.ninja`を使ってビルドします。

## ファイル構成

```text
.
├── build.ninja
├── gcd.cc
├── gcd.hh
└── main.cc
```

* `main.cc` — メインプログラム
* `gcd.cc` — 最大公約数を計算する`gcd`関数の実装
* `gcd.hh` — `gcd`関数の宣言
* `build.ninja` — Ninjaのビルド定義

## 必要なもの

* C++コンパイラ（GCCなど）
* [Ninja](https://ninja-build.org/)

Ubuntuでは、以下のコマンドでNinjaをインストールできます。

```sh
sudo apt install ninja-build
```

## ビルド

リポジトリを取得して、`ninja`を実行します。

```sh
ninja
```

`main`という実行ファイルが生成されます。

```sh
./main
```

実行すると、以下のように表示されます。

```text
5
```

ビルド時に実行されるコマンドを確認したい場合は、`-v`オプションを付けます。

```sh
ninja -v
```

## クリーン

生成されたファイルを削除するには、以下を実行します。

```sh
ninja -t clean
```

## 関連記事

このリポジトリは、以下の記事で使用しているサンプルコードです。

[Qiita - お試しninja](https://qiita.com/yoshiyasu1111/items/fb1b0222c6d1e3837e8c)
