# やんばるエキスパート Laravel 課題（応用）

## 教材のご案内

- やんばるエキスパート教材
  - [【テキスト教材】Laravelの基本](https://www.yanbaru-code.com/texts/482)
  - [【テキスト教材】ローカル環境構築(Mac向け)](https://www.yanbaru-code.com/texts/483)
  - [【テキスト教材】ローカル環境構築(Windows向け)](https://www.yanbaru-code.com/texts/484)

## 課題の提出方法

Laravel課題（基礎）で作成したご自身のGitHubリポジトリ(`laravel_application`)にプッシュして下さい。

## 質問する際の注意点

Laravel課題（応用）は共同開発前の最後の課題です。

Slackの「質問」チャンネルで質問する際は以下のテンプレートに沿って質問してみましょう。

### 質問テンプレート

```
①聞きたいことの一言まとめ

②発生している問題（起きている現象の詳細/エラー文/スクショ/デバッグ結果）

③ソースコード（関連する全てのソースコード/ファイルを直接添付しない）

④問題解決するために試したこと（コマンドやコードがあれば追記し、参考にしたサイトを全て記載）

⑤問題について自分なりに考えたこと（検索結果/自分なりの原因予想）
```

エンジニアにとって質問の上手さ（＝質問力）は仕事をする上でかなり重要な要素です。

学習段階から意識して質問力を向上させていきましょう。

## 課題

### 作成するアプリの概要について

Laravel課題応用ではCRUDアプリを作成します。<br>

CRUDとは以下の4つの機能の総称です。

- C(Create)：登録
- R(Read)：読込・詳細表示
- U(Update)：更新・編集
- D(Delete)：削除

データベースには以下の2つのテーブルを作成します。

- `users`テーブル（ユーザー用）
- `posts`テーブル（投稿データ用）

なお、`users`テーブル用のマイグレーションファイルはデフォルトで用意されているので新たに作成する必要はありません。

`posts`テーブルのカラムは以下の通りで設定してください。（必ずマイグレーションファイルからテーブルを作成してください）

- `id`(Integer)
- `title`(String)
- `body`(String)
- `created_at`(Timestamp)
- `updated_at`(Timestamp)

※()内はデータの型を表しています

Laravel課題（応用）ではいくつかの画面を作成しますが、今はLaravelでのバックエンド実装の力をつけるため、画面のデザイン（UIと言います）は気にしなくて問題ありません。<br>
テキスト教材を読み進めて行けば問題なく画面作成はできます。

**課題提出の際は、必ずGitHubのURLを添付してください。**

### Laravel 課題5

`laravel ui`というパッケージを使用してユーザー登録画面とログイン画面を作成し、提出してください。

- [【テキスト教材】ユーザー登録・ログイン](https://www.yanbaru-code.com/texts/488)
- Laravel課題（基礎）で作成したLaravelアプリに機能を追加してください。（別のアプリを作成する必要はありません）
- Slackでレビュー依頼する際に「**ユーザー登録画面のスクショ**」、「**ログイン画面のスクショ**」を添付してください。

### Laravel 課題6

ユーザー登録、ログインができるLaravelアプリを作成し、提出してください。

- [【テキスト教材】ユーザー登録・ログイン](https://www.yanbaru-code.com/texts/488)
- Laravel課題5で作成したアプリに機能を追加してください。（別のアプリを作成する必要はありません）
- ユーザー登録後、データベースに登録情報が1件以上保存されていることを確認した上で提出してください。

### Laravel 課題7

以下の機能を実装したLaravelアプリを作成し、提出してください。

1.  ログインユーザーのみがトップページから登録画面に遷移できる
2.  ログインユーザーのみがデータの登録ができる
3.  登録画面から投稿データを登録できる
4.  トップページにデータベースに保存された投稿データが表示される

- [【テキスト教材】CRUD（C：登録）](https://www.yanbaru-code.com/texts/489)
- Laravel課題6で作成したアプリに機能を追加してください。（別のアプリを作成する必要はありません）
- データ登録処理後、データベースに登録情報が1件以上保存されていることを確認した上で提出してください。
- トップページに表示する投稿データは投稿したユーザーの名前、投稿データのタイトル(`posts`テーブルの`title`カラムの値)、投稿データの本文(`posts`テーブルの`body`カラムの値)としてください。

### Laravel 課題8

トップページから選択した投稿データの詳細画面に遷移できるLaravelアプリを作成し、提出してください。

- [【テキスト教材】CRUD（R：詳細表示）](https://www.yanbaru-code.com/texts/493)
- Laravel課題7で作成したアプリに機能を追加してください。（別のアプリを作成する必要はありません）
- 詳細画面に遷移するための「詳細ボタン」を追加して、ボタンをクリックすると詳細画面に遷移するようにしてください。
- 詳細画面に表示する投稿データはトップページと同じく、投稿したユーザーの名前、投稿データのタイトル(`posts`テーブルの`title`カラムの値)、投稿データの本文(`posts`テーブルの`body`カラムの値)としてください。

### Laravel 課題9

以下の機能を実装したLaravelアプリを作成し、提出してください。

1.  ログインユーザーのみが記事詳細画面に設置した「編集」ボタンから編集画面に遷移できる
2.  ログインユーザーのみが編集画面からデータの更新ができる
3.  トップページには編集後の投稿データが表示される

- [【テキスト教材】CRUD（U：更新・編集）](https://www.yanbaru-code.com/texts/491)
- Laravel課題7で作成したアプリに機能を追加してください。（別のアプリを作成する必要はありません）
- 記事詳細画面から編集画面に遷移するための「編集ボタン」を追加してください。
- データ編集処理後、編集が反映されていることをトップページとデータベース両方で確認し、提出してください。

### Laravel 課題10

選択した投稿データを削除することができるLaravelアプリを作成し、提出してください。

- [【テキスト教材】CRUD（D：削除）](https://www.yanbaru-code.com/texts/492)
- Laravel課題9で作成したアプリに機能を追加してください。（別のアプリを作成する必要はありません）
- 記事詳細画面に追加した「削除ボタン」をクリックしたらその投稿データを削除できるようにしてください。
- データ削除処理後、削除されていることをトップページとデータベース両方で確認し、提出してください。

### Laravel 課題11

以下の条件を満たすデバッグコマンドを埋め込んだLaravelアプリを作成し、提出してください。

1. 投稿画面に遷移しようとすると画面に「投稿画面だよ！！」と表示されて、投稿画面に遷移しない。
2. 編集画面に遷移しようとすると画面に「編集しようとした投稿データの情報」が表示され、編集画面に遷移しない。

- [【テキスト教材】デバッグ](https://www.yanbaru-code.com/texts/494)
- Laravel課題10で作成したアプリに機能を追加してください。（別のアプリを作成する必要はありません）

<hr>

これで課題は全て終了です！

全ての課題レビューが完了したら、担当メンターにご連絡ください！

共同開発も頑張っていきましょう！