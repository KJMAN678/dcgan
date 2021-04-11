# DCGAN

## [Colab上のコード](https://colab.research.google.com/drive/1C0tk_2UmRu4PGwBPePxfSmyPmYfSd8Fg?usp=sharing)

## コードの引用元
- [５ステップでできるPyTorch - DCGAN](https://qiita.com/hkthirano/items/7381095aaee668513487)
- [使われているアニメキャラの画像の加工済みデータセット](https://github.com/hkthirano/5Steps-PyTorch-DCGAN)

## 変更点
- GoogleColab上で実行が完結するように修正
- GPU環境だけでなく非GPU環境でも実行可能なよう修正
- パラメーターを1セルに集約
- TensorBoardの設定
- 最終的に生成した画像を表示するコードを追加

## 検証した各設定の違い

|バージョン|学習率|画像サイズ最適化関数|gen活性化関数|
|----|----|----|----|
|001|0.0002|adam|relu->tann|
|002|0.0005|adam|relu->tann|
|003|0.0002|AdaBelief|relu->tann||
|004|0.0002|Adam|frelu->tann|

### バージョン001の画像
![バージョン001](https://storage.googleapis.com/zenn-user-upload/e6gq761219s8pev6oq8qscdgy84p)

### バージョン002の画像
![バージョン002](https://storage.googleapis.com/zenn-user-upload/jc3232hn99cf4n972cz9cwoircb1)

### バージョン003の画像
![バージョン003](https://storage.googleapis.com/zenn-user-upload/stb39ibk32j4n25eybu2h5bglcdg)

### バージョン004の画像
![バージョン004](https://storage.googleapis.com/zenn-user-upload/4lsbnworil6gmpgtm23iis0pbyw7)



## AdaBelief
[出きたてホヤホヤ！最新オプティマイザー「AdaBelief」を解説！](https://qiita.com/omiita/items/5012afa3cba4d73a7aed)
[GitHub](https://github.com/juntang-zhuang/Adabelief-Optimizer)

## FReLU
[【実装】あたらしい活性化関数「FReLU」をPytorch CIFER10 Turorialに組み込んでみる](https://qiita.com/Radley/items/5cfa226d9d108e769861)
