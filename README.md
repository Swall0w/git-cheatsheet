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
