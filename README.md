# care-label
画像認識による洗濯表示の識別

## Description
画像から洗濯表示を識別し、意味を表示する

>洗濯表示とは？  
衣服についたタグのマークのこと。  
洗濯や乾燥の方法、アイロンのかけ方やクリーニングの方法などが示されている。  
全41種類。世界共通。

### WEBアプリケーション
- TOP  
![screencapture-localhost-5000-2019-10-08-23_21_42](https://user-images.githubusercontent.com/20394831/66403986-899bfd80-ea22-11e9-8d49-2ba7ce8e9cc7.png)
- 予測結果表示  
![screencapture-localhost-5000-predict-2019-10-08-23_23_41](https://user-images.githubusercontent.com/20394831/66404071-b0f2ca80-ea22-11e9-9fed-017e87f21105.png)


## Features
- 洗濯表示の識別
- 意味出力

## Requirement
画像の水増し python 3.6~（f文字列）

WERアプリ
[app/requirements.txt](/app/requirements.txt)

## Usage
### 画像の水増し
1枚から約1500枚に水増し。明るさ、ノイズ、回転、移動（上下左右斜め）の加工を行う。

1. [cnn/train-seeds](/cnn/train-seeds/)下の該当するフォルダに画像をおく
2. [cnn/all-ver2.ipynb](/cnn/all-ver2.ipynb)を実行する  
(windowsの場合は、[cnn/all-ver2-win.ipynb](/cnn/all-ver2-win.ipynb))
3. [cnn/train](/cnn/train/)下の該当するフォルダに水増しされた画像が出力される


上記の方法は、一括で水増しする場合。
1枚1枚指定して水増しする場合は、[cnn/all-file.ipynb](/cnn/all-file.ipynb)を実行する。

### 学習
[cnn/predict.py](/cnn/predict.py)を実行する。

モデル、重み、学習履歴、学習過程の図が保存される。

### WEBアプリケーション
[app/app.py](/app/app.py)を実行する。  
localhost:5000から確認できる。  
