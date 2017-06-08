# git-cheatsheet
## Git　コマンドの設定

    $ git config --global user.name "<name>"
    コミットに付加される名前を設定する
    
    $ git config --global user.email "<email>"
    コミットに付加されるメールアドレスを設定する
    
    $ git config --global color.ui auto
    コマンドラインの出力を見やすくするための色を設定する
  
## リポジトリの設定

    $ git init <project>
    指定した名前でローカルリポジトリを作成する
    
    $ git remote add <name> <url>
    リモートリポジトリの設定を指定した名前で追加する
    
    $ git remote rename <old> <new>
    リモートリポジトリの設定を<old>から<new>に変更する
    
    $ git clone <url>
    <url>のリポジトリをローカルリポジトリとして複製する
  
## 変更履歴の登録

    $ git status
    リポジトリとステージングエリアの状態を確認する
    
    $ git add <file>
    ワーキングディレクトリの変更をステージングエリアに追加する
    
    $ git add --all
    ワーキングディレクトリの全ての変更をステージングエリアに追加する
    
    $ git diff
    ワーキングディレクトリとステージングディレクトリの差分を表示
    
    $ git commit -m "<message>"
    ステージングした内容をコミットする
    
    $ git reset <file>
    ファイルをステージングエリアから外すが、内容の変更は保持する
    
    $ git commit --amend
    直前のコミットを新しいコミットで置き換える
    
## 履歴確認
    
    $ git log
    現在のブランチのバージョン履歴を表示
    
    $ git log --oneline
    現在のブランチのバージョン履歴を一覧ではなく、各履歴一行で表示
    
    $ git log --follow <file>
    名前の変更を含む指定したファイルのバージョン履歴の一覧を表示
    
    $ git show <commit>
    指定したコミットの辺呼応内容とメタ情報を出力
    
    $ git blame <file>
    指定ファイルの各行毎に最終変更の情報を表示する
    
    $ git diff <first> <second>
    2つのブランチ間の差分を表示
    
    $ git checkout <commit>
    指定コミットのリビジョンの内容をワーキングディレクトリに反映
    
## 履歴修正

    $ git reset <commit>
    現在のブランチのHEADを指定コミットまで移動し、ステージングされた内容をクリアし、ワーキングディレクトリの変更状態を保つ
    
    $ git reset --hard <commit>
    現在のブランチのHEADを指定コミットまで移動し、ステージングされた内容とワーキングディレクトリの変更をクリアする
    
    $ git revert <commit>
    指定コミットによって加えられた変更をもとに戻す新しいコミットを生成し、摘要
    
    $ git rebase <branch>
    指定ブランチの内容を自動的にチェックアウトし、現在のブランチで加えられた変更履歴を退避させ、１つずつコミットし直して履歴を作成する
    
## ブランチ操作

    $ git branch
    ローカルリポジトリのブランチを一覧表示
    
    $ git branch -a
    ローカルブランチとリモート追跡ブランチの一連を表示する
    
    $ git branch <name>
    新規ブランチを作成する
    
    $ git checkout <name>
    指定したブランチに切り替え、ワーキングディレクトリを更新する
    
    $ git checkout -b <name>
    指定したブランチの作成とそのブランチに移行する
    
    $ git merge <name>
    指定したブランチの履歴を現在のブランチに統合する
    
    $ git branch -d <name>
    指定したローカルブランチを削除する
    
    $ git branch -m <name>
    現在のブランチの名前を<name>に変更
    
    $ git tag <name>
    指定した名前でタグを生成
    
## 一時的な変更の記録

    $ git stash
    変更を監視されているファイルの変更の状態とステージングの状態を保存し、HEADの状態までクリーンに戻す
    
    $ git stash list
    一時的に保存された記録の一覧を表示
    
    $ git stash pop
    一時的に保存された記録から、記録内容をワーキングディレクトリに反映する
    
    $ git stash drop
    一時的に保存された記録を破棄する
