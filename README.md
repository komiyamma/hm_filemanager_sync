# HmFileManagerSync

![HmFileManagerSync v1.0.0](https://img.shields.io/badge/HmFileManagerSync-v1.0.0-6479ff.svg)
[![CC0](https://img.shields.io/badge/license-CC0-blue.svg?style=flat)](LICENSE)
![Hidemaru 8.01](https://img.shields.io/badge/Hidemaru-v8.01-6479ff.svg)

秀丸エディタで現在開いているファイルと、ファイルマネージャ（エクスプローラペイン）の表示フォルダを同期させるためのマクロです。

## 概要

秀丸エディタでファイルを切り替えるたびに、ファイルマネージャペインが自動的にそのファイルの場所に移動します。これにより、関連ファイルを素早く見つけたり、ファイル構造を把握したりするのが容易になります。

## ファイル

このリポジトリには、以下のマクロファイルが含まれています。

- **`HmFileManagerSync.mac`**
  - メインのマクロです。現在アクティブなファイルのディレクトリをファイルマネージャペインで開きます。
  - 秀丸エディタの `[イベント(E)]` → `[ファイルを開いた後]` や `[フォーカスが当たった後]` にこのマクロを割り当てることで、自動的に同期できます。

- **`HmFileManagerClose.mac`**
  - ファイルマネージャペインを閉じます。

- **`HmFileManagerCloseBecauseThin.mac`**
  - ファイルマネージャペインの幅が非常に狭い（150px未満）場合にのみ、ペインを閉じます。
  - ペインの幅を意図せず狭めてしまい、表示が崩れた場合などに自動で閉じることを想定しています。

## 使い方

1. このリポジトリにある `.mac` ファイルを、秀丸エディタのマクロディレクトリ（通常は `C:\Users\YourName\AppData\Roaming\Hidemaru\Macro`）に配置します。
2. 秀丸エディタの `[マクロ(M)]` → `[マクロ登録(E)]` から、各マクロを登録します。
3. 必要に応じて、`[その他(O)]` → `[キー割り当て(K)]` や `[イベント(E)]` にマクロを割り当てて使用してください。
   - 例：`HmFileManagerSync.mac` を `[ファイルを開いた後]` イベントに割り当てる。

## 動作要件

- 秀丸エディタ v8.01 以上
- [HmExplorerPane.dll](https://hide.maruo.co.jp/software/hmexplorerpane.html) が必要です。
- `HmFileManagerCloseBecauseThin.mac` を使用する場合は、`HmGetTargetWindowSize.dll` が必要です。（作者の別リポジトリなどで入手してください）

## ライセンス

[CC0 1.0 Universal](LICENSE)

このソフトウェアは、パブリックドメインとして提供されます。

## 作者

(ここに作者名を記載)
