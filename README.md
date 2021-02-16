# みんなで架空サイトを作ってみよう

# 開発の流れ

Githubで管理するリポジトリでは、以下の流れでコードを更新します。

* まずはmainブランチからはじめる
    * ローカルリポジトリで`main`ブランチに入る
    * リモートリポジトリで`main`ブランチの更新があるか確認する
* featureブランチで開発
    * featureブランチを切る
    * 開発する
    * 変更点をローカルリポジトリで`commit`する
* レビュー
    * リモートリポジトリへ`push`する
    * Pull Requestを出す
    * PRでレビューをしてもらう
* 最後にmainブランチへmerge
    * PRのレビューが終了したら、`main`ブランチへ`merge`する

---------
## まずは、コードをローカルにコピーするのに次のコマンドを実行します。

```
git clone https://github.com/over-40-web-club/playground01.git
```

# 開発
---------
## ローカルリポジトリでmainブランチに入る
次のコマンドで、自分がいるブランチを確認しましょう。
```
git branch
```

mainブランチにいなかったら、mainに戻ります。
```
git checkout main
```

## リモートリポジトリでmainブランチの更新があるか確認する
誰か更新をしていないか確認するために以下のコマンドを実行します。
```
git pull
```

# featureブランチで開発

mainブランチでは、追加や変更をしないようにしましょう。
**チーム開発の練習なので、一行でもなにかコードを書こうと思ったら、featureブランチという開発用ブランチで作業します。**

## featureブランチを切る

```
git checkout -b feature/new-branch
```
＊「feature/new-branch」の「new-branch」には変更内容がわかるような名前をつけます。

## 変更した内容をコミットする

```
git add .
git commit -m "(例)[add]画像を追加"
```
- git add 「.」には変更したファイル名を入力します。「.」は変更全部という意味です。
- ""は全角を使用しないように注意しましょう。
おかしくなってしまったら、「control+C」で内容を廃棄できます。慌てないでやり直してみましょう。
- 識別子にまずは、[add], [update], [fix], [remove]（追加・更新・修正・削除）を使ってみましょう。


----
# レビュー

## リモートリポジトリへpushする
```
git push --set-upstream origin feature/new-branch
```


Githubのリモートリポジトリへ、ローカルリポジトリの変更を反映させます。
これでPRを出したり、他の人があなたの更新したコードを見えるようになります。

## Pull Requestを出す
Github上のリポジトリページに移動します。
pushしたブランチのPull Request (PR)を出せるようになっています。
画面右の[Compare & pull request]を押します。



参考にしたサイト：[Githubでチーム開発するためのマニュアル](https://qiita.com/siida36/items/880d92559af9bd245c34)
