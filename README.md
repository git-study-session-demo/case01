修正をmaster(main)にマージするまでの流れを知りたい。


（ブラウザ）リポジトリを準備する
（コマンド）リポジトリをローカルにクーロンする

```bash
git clone <your repository url> .
```

（コマンド）開発ブランチを作成する

```
git switch -c feature/case0101
```

（コマンド）サンプルファイルを追加して、そのファイルをコミットしてリモートの開発ブランチにプッシュする

```
touch sample.txt
echo "hello, world" > sample.txt
git add sample.txt
git commit -m 'add sample.txt'
git push origin feature/case0101
```

（ブラウザ）PRを作成しマージする

githubのリポジトリ画面でマージを行う

ブランチを削除・ローカルブランチを削除

（コマンド）ローカルmainブランチに戻って更新する

```
git switch main
git pull origin main
```

先ほど追加したファイルはmainブランチに反映していることを確認