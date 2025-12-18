## Gitの準備
### 1. wslに接続する
ターミナルから、Linux環境に入る
### 2. Gitのバージョン確認
    git --version 
    
    sudo apt install git -y (入っていない場合)
### 3. Gitの設定
- 設定値の一覧を確認
> ~$ git config --list
- ユーザー名を設定する
> ~$ git config --global user.name ユーザー名<br><br>
コミット履歴に表示される名前
- メールアドレス設定する
> ~$ git config --global user.email メールアドレス<br><br>
コミット履歴に表示されるメールアドレス
- VScodeを設定する
> ~$ git config --global core.editor "core --wait"<br><br>
コメント入力のエディタをVScodeで開くため
- デフォルトブランチ名を設定する
> ~$ git config --global init.defaultBranch main

### 4. GitHubに公開鍵を設定
- ssh-keygen -t ed25519 -C "メールアドレス"
- Enter
- パスワード入力
- ls ~/.ssh
- cat ~/.ssh/id_ed25519.pub
- GithubにSSH keys登録

### 1. Collabrator
### 2. Fork→clone

## GitHubでリポジトリを作成する
省略

## ローカル環境にリポジトリを用意する方法
### 1. 新規プロジェクトを作成
- 適当なディレクトリに移動
- mkdir プロジェクトフォルダ名
- cd プロジェクトフォルダ名
- git init<br>
↑ これで、新規リポジトリが作成できる

### 2. GitHubのリポジトリをクローン
- git clone ~<br>
「~」は、GithubのリポジトリのHTTPS or SSHをコピー


## これで準備完了<br>
## ファイルを編集して、コミットする流れ
```
1 状態を見る                    git status
2 ファイルを編集する
3 編集を追加する                git add .
4 記録（commit）する            git commit -m "何をしたか"
```
- 2回目以降の作業の時は
> ~$ git pull origin main

1. リポジトリの状態確認
> ~$ git status

2. ファイルの編集
> 今まで通り、ファイルを作って編集

3. 変更をGitに伝える（add）
```
~$ git add 追加したいファイルやフォルダ<br>
~$ git add .    ←すべて追加する場合
```

4. 変更を記録する（commit）
```
~$ git commit -m "メッセージを記述"
~$ git commit 
```


## 次は、GitHubに反映する
ここまでは、ファイルを編集、commit(ローカル保存)を行った。

- ローカルの変更をGitHubに送る
```
> ~$ git push origin main

origin：Githubのリポジトリ
main：送るブランチ名
```

## ブランチについて
```
ブランチとは、
```

- ブランチの作成
> ~$ git branch ブランチ名
- 使用中のブランチを確認
> ~$ git branch
- ブランチの変更
> ~$ git switch ブランチ名


練習

