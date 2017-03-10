# このソフトウェアについて

GitHubリポジトリ作成スクリプトに削除機能を追加した。

[前回]()の改良版。CUI対話によって削除できる。

# 開発環境

* Linux Mint 17.3 MATE 32bit
* [Python 3.4.4](https://www.python.org/downloads/release/python-344/)
    * [requests](http://requests-docs-ja.readthedocs.io/en/latest/)
    * [dataset](https://github.com/pudo/dataset)

## WebService

* [GitHub](https://github.com/)
    * [アカウント](https://github.com/join?source=header-home)
    * [AccessToken](https://github.com/settings/tokens)
    * [Two-Factor認証](https://github.com/settings/two_factor_authentication/intro)
    * [API v3](https://developer.github.com/v3/)

# 準備

[前回]()の手順に従い、リポジトリ作成しておくこと

# 実行

## 1. 起動する

1. ターミナルを起動する
1. 以下のコマンドを実行する（今回のスクリプトを実行する）

```sh
bash call.sh
```

### 2. 削除する

```sh
リポジトリ名： ytyaru/{call.shを実行したディレクトリ名}
説明: 説明文。
URL: http://abc
----------------------------------------
add 'LICENSE.txt'
add 'ReadMe.md'
add 'main.py'
commit,pushするならメッセージを入力してください。Enterかnで終了します。
サブコマンド    n:終了 a:集計 e:編集 d:削除 i:Issue作成
```

```
d
```

`d`を入力してEnterキー押下する。

### 3. 集計を表示する

```sh
.gitディレクトリ、対象リモートリポジトリ、対象DBレコードを削除します。
リポジトリ名： ytyaru0/GitHub.Upload.ByPython.DeleteRepo.201703091329
OrderedDict([('Id', 6), ('IdOnGitHub', 84407449), ('Name', 'GitHub.Upload.ByPython.DeleteRepo.201703091329'), ('Description', 'なんか適当な説明文。'), ('Homepage', 'http://abcdefg'), ('CreatedAt', '2017-03-09T06:39:51Z'), ('PushedAt', '2017-03-09T06:39:52Z'), ('UpdatedAt', '2017-03-09T06:39:51Z'), ('CheckedAt', '2017-03-09T06:39:55Z'), ('RepositoryId', None)])
OrderedDict([('Id', 6), ('RepositoryId', 6), ('Forks', 0), ('Stargazers', 0), ('Watchers', 0), ('Issues', 0)])
OrderedDict([('Id', 7), ('RepositoryId', 6), ('Language', 'Shell'), ('Size', 228)])
OrderedDict([('Id', 8), ('RepositoryId', 6), ('Language', 'Python'), ('Size', 14769)])
削除すると復元できません。本当に削除してよろしいですか？[y/n]
```

```sh
y
```

`y`を入力してEnterキー押下する。

```sh
削除しました。
```

* `.git`ディレクトリが削除される
* 対象リモートリポジトリが削除される
* 対象DBレコードが削除される

これで削除が完了する。

# ライセンス #

このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)

