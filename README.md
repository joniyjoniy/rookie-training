## rookie-training

#### GitHubの設定

  - 大学メールアドレスでGitHubに登録する。
  - [GitHub Education](https://education.github.com)を申請すれば、Micro Planが無料になる。
  - [Generating SSH keys](https://help.github.com/articles/generating-ssh-keys/)を参考に、GitHubに公開鍵を登録する。
  - sai-labの[Owners](https://github.com/orgs/sai-lab/teams/owners)に、[Members](https://github.com/orgs/sai-lab/teams/members)に招待してもらう。

#### Gitの設定

研修用サーバ(rookie)にログインして作業する。  
Gitに、GitHubに登録したメールアドレスと名前(英語)を設定する。

    $ git config --global user.email "YOUR EMAIL ADDRESS"
    $ git config --global user.name "YOUR NAME"

「[gitのpush.defaultに関するノウハウ - Qiita](http://qiita.com/awakia/items/6aaea1ffecba725be601)」を参考に、`push`のデフォルトの挙動を設定する。

    $ git config --global push.default current

最後に、研修用のリポジトリを`clone`する。

    $ git clone git@git@github.com:sai-lab/rookie-training.git

#### ルール・ポリシー

各研修の開始時に、学籍番号と日付(例: `s00t000_150423`)でブランチを切る。

    $ git pull
    $ git checkout -b s00t000_150423

研修の終了時に、そのブランチを`push`し、プルリクエストを作成する。  
プルリクエストのタイトルは学籍番号と研修内容、日付(例: `s00t000 git 2014.04.23`)とする。  
本文には、研修の作業内容や質問、感想や反省を書く。  
研修の担当者(院生など)がプルリクエストを確認し、マージや、不足があればコメントする。
