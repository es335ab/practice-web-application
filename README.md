## このリポジトリの目的

- Ajaxをたくさん使ったWebアプリケーションの開発（Trelloなど）ができるようになること

## 前提知識

- <a href="https://github.com/es335ab/practice-front-end">practice-front-end</a>を修了していること
- Railsチュートリアルを一通りこなしてあること

## 要求

- Na○erまとめのようなまとめサイトを展開してください
- ユーザーが記事を見る機能、ユーザーがインタラクティブに記事を作成できる機能を作成してください

## 要件

### ルーティング（html）

- `/articles`
  - 記事を全件表示。
  - 記事にはタイトルと記事の最終更新日時を表示する。
  - コンテンツはサーバーサイドでhtml生成する。
  - 記事カセットをクリックすると、記事詳細ページに遷移する。
  - 一覧のページネートなどはなくてOK
- `/articles/:id`：記事詳細を表示するページ。コンテンツはサーバーサイドでhtmlを生成する。
- `/articles/new`：記事を新規に作成するページ
- `/articles/:id/edit`：記事を編集するページ
- `/categories`：カテゴリーの一覧ページ
- `/categories/:id`：あるカテゴリーに属する記事の一覧ページ
- `/tags`：タグの一覧ページ
- `/tags/:id`：あるタグに属する記事の一覧ページ

### ルーティング（API）

- `get /api/v1/article/:id`：記事詳細情報を取得するAPI
- `post /api/v1/article_item`：記事アイテムを新規追加するAPI
- `update /api/v1/article_item/:id`：記事アイテムを更新するAPI
- `delete /api/v1/article_item/:id`：記事アイテムを削除するAPI

### ユーザーについて

- ユーザーはseedでダミーのユーザーを1名し登録し、current_userとして扱ってください。
  - ユーザーはid,name だけ属性を持っておけばOK

## 開発方針

### サーバーサイド

- ruby v2.4.1
- rails v5.1.2
- mysqlwrokbench（ER図作成用ツール）

### フロントエンド（モジュール）

- node@8.1.2
- react@15.6.1
- babel
- gulp
- webpack@3系
- node-sass
- bootstrap（UI作成用）
- axios（ajax用）

### フロントエンド（コーディングガイドライン）

- SMACSS, OOCSSを採用すること

## マイルストーン

1. サービスの要求を正しく理解する
2. サービスの要求に合ったER図を作成する ※
3. 記事詳細情報のCRUD機能を作成 ※
4. 4以外の機能を作成 ※

※レビュー者にレビューを受ける
