# GItPractice

Git、およびGitHub-flowのチュートリアル、練習用リポジトリです。

各種必要なインストール手順、Gitの基礎、GitHub-flowによる開発フローについて、
簡単に説明します。

# インストール

## Gitをインストール

下記URLからWindows版をDL、インストーラーで適当にする。

https://gitforwindows.org/

## SourceTreeをインストール

下記URL（略

https://www.sourcetreeapp.com/

- Atlassionのアカウントいるので適当に作成する。
- JIRAのアカウントで行けるはず（JIRAがAtlassion製なので）
- GitHUbと連携させる際に不都合なのでGitHubと同じメールアドレスにすること

## GitHub-flowのおまかな流れ

1. GitHubからソースをとってくる（クローン）
2. 作業用ブランチ（feature-branch）を切る
3. 空コミットする（作業開始のプルリクを投げるため）
 - SourceTreeは標準で空コミットできないので下記で設定入れる
 https://github.com/ikkou/SourceTree-Custom-Action
4. feature-branchをリモートリポジトリにプッシュ
 - プルリク名を[WIP]～～に変更すること
 _（WIP…WorkInProgress、作業中の意）_
5. できたブランチに対してプルリク作成
6. 開発開発！
 1. 開発→コミット→リモートリポジトリにプッシュ、の繰り返し
 2. 他の開発者の変更をとってくるために定期的にdevelopからプルしてくる
7. feature-branchで作るべき機能が完成
8. ローカルでテスト通す
9. feature-branchに変更をプッシュ
10. プッシュし終わったらGitHub上のプルリクを使ってレビューする。
11. 誰かがレビューすればOKになり、developにマージされる。

_細かい手順・作業はチュートリアルします。_

## ルール

- コミットは細かくやること。１つの作業単位でまとめる。３０分毎ぐらいが目安
- コミット時のメッセージは下記を規約にしましょう
https://qiita.com/Kenya/items/f72fba8fecc79d1b090c
 - JIRAでIssue管理するようになると、どのIssueに紐づいた開発・修正なのかわかるようにするので運用決まったら変更します
- フィーチャーブランチの命名は「feature-（実現機能名）」
