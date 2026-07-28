# 小規模地域芸術祭データベース(公開用)

経営芸術総合研究所のリサーチプロジェクトとして公開する、単一HTMLの静的データベースです。
日本・台湾・韓国・東南アジアの小規模地域芸術祭61件を収録(2026年7月調査)。

- `index.html` … これ1ファイルで完結(外部依存はGoogle Fontsのみ)。データはファイル内に埋め込み。

## GitHub Pagesでの公開手順(projectFと同方式)

1. GitHubで新しいリポジトリを作成(例: `art-festival-db`、Public)
2. `index.html` をリポジトリ直下にアップロード(Web画面の「Add file → Upload files」でOK)
3. リポジトリの Settings → Pages → Branch を `main` / `(root)` にして Save
4. 数分後に `https://epitajim.github.io/art-festival-db/` で公開されます

## keieiart.com への掲載文(案)

「リサーチ・開発」セクションのprojectFの並びに:

> **小規模地域芸術祭データベース**
> 日本・台湾・韓国・東南アジアの小規模・地域密着型芸術祭61件を横断調査したデータベース。
> 場所・予算・アーティスト数・開催間隔・連絡先・特徴を収録し、検索・絞り込みが可能(2026年7月調査)。
> https://epitajim.github.io/art-festival-db/

## データ更新について

データは `index.html` 内の `const DATA = [...]` に1件=1オブジェクトで格納されています。
項目: name / alt / cat(国内・台湾・韓国・東南アジア) / country / pref / loc / interval /
last / next / artists / budget / org / web / email / tel / form / sns / tags / features / status / sources など。
件数・国別の集計は自動計算されるため、レコードを追加・削除するだけで表示に反映されます。
