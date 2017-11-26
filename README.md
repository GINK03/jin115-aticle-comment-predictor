# 勾配ブースティングを利用した、KPIに聞く特徴量のレコメンド

## 意思決定をサポートする機械学習の必要性

## ワトソンの料理の新しいレシピのレコメンドと基本は一緒

## 【実験】　jin115.comのコメント数をどんな単語で記述したら数が増えるか予想する
[jin115.comのデータセットをzip圧縮で17GByteもダウンロード](https://storage.googleapis.com/nardtree/jin115-20171125)してしまったので、何か有効活用できないかと考えていたのですが、難しく、なんともKPIという軸で定量化できないので、
ある記事に対してつく、コメント数を増やすには、どんな単語選択が適切かという軸に切り替えて、分析してみました。  

jin115.comでは、2chまとめが流行った時に大量のアクセスを受けていたという背景があり、近年では常には同じぐらいのユーザ数がいるわけではありません。  
(あとでここはフィルする)

## 前処理

**データセットダウンロード**  

[Google Cloud Strageに大容量のスクレイピング済みのデータセットをzip圧縮したもの](https://storage.googleapis.com/nardtree/jin115-20171125/jin115-20171125.zip)がありので、追試等が必要な方は参照してください。
```console
$ wget https://storage.googleapis.com/nardtree/jin115-20171125/jin115-20171125.zip
```

**htmlコンテンツから必要なarticle, commentの数, 日時, タイトルのパース**  

ダウンロード済みのhtmlコンテンツから予想の元となる説明変数（article, title, date）と、目的変数であるcomment数をパースします　　

この捜査自体が極めて重いので、[Google Data Strageからもダウンロード]()できます　　

```console
$ python3 parser.py --map1
```


