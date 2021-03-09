修正をmaster(main)にマージするまでの流れを知りたい。


（ブラウザ）リポジトリをフォークする

![スクリーンショット 2021-03-09 13 29 23](https://user-images.githubusercontent.com/869103/110418883-96bb9100-80db-11eb-8b64-5597f8ca3d56.png)

フォークしたリポジトリをローカルにクーロンして、その中に入る

```bash
git clone <your repository url> case01
cd case01
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
