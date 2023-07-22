。# WordPressテストサイトの作り方（Local使用編）
本番運用しているWordPressサイトをコピーして、自分のPCに検証用のテストサイトを作ります。
## 1. 準備
### 1-1. All in one WP Migration（WordPressプラグイン）
WordPress管理画面からプラグイン名で検索＆インストールして有効化、またはWordPressプラグインサイトからダウンロード＆アップロードして有効化します。

[All-in-One WP Migration &#8211; WordPress プラグイン &#124; WordPress.org 日本語](https://ja.wordpress.org/plugins/all-in-one-wp-migration/)
### 1-2. Local（開発環境）
ダウンロードしてインストールします。なお、新規ダウンロード時は、メールアドレスの登録が必要です。

[Local &#x2d; Local WordPress development made simple](https://localwp.com/)
## 2. テストサイト作成手順
### 2-1. サイトデータのエクスポート
WordPress管理画面のサイドメニュー「All-in-One WP Migration」にアクセスして、エクスポートを実行します。

通常は、そのままファイルにエクスポートすれば問題無いですが、画像が多い場合はオプションで「メディアライブラリをエクスポートしない」をチェックしても良いでしょう。動作確認するだけなら、画像は必須ではありません。（ただし、画像を表示するプラグインを使用している場合などを除く）
### 2-2. LocalのインストールとWordPressのインストール
インストール手順については割愛させて頂きますが、基本的にインストールウィザードに従って進めるだけです。

インストール完了後はLocalを起動し、左下の＋（プラス）マークをクリックしてサイトを追加します。ドメイン名は分かりやすいものを任意で、動作環境設定では「Custom」を選択して、実際に運用している環境に近いPHPバージョンとMySQLバージョンを選択します。なお、サーバーの種類はNginxでもApacheでもどちらでも問題無いと思います。

サイトの追加が完了したら、右上の「START SITE」からサイト起動し、「ADMIN」ボタンをクリックして指定したIDとPASSWORDで管理画面にログインします。

なお、WindowsでLocalの動作が異様に遅い（WordPressが重い）場合は、下記のフォーラムのスレッドを参考に設定を行ってみて下さい。（それでも、体感的にMacの方が早い気がします）

[Local is too slow with wordpress and windows 10](https://community.localwp.com/t/local-is-too-slow-with-wordpress-and-windows-10/26348/10)
### 2-3. サイトデータのインポート
## 3. 検証手順
## 4. こんな時どうする？問題別対処法
