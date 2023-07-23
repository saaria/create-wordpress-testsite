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
WordPress管理画面のサイドメニュー"All-in-One WP Migration"にアクセスして、エクスポートを実行します。

通常は、そのままファイルにエクスポートすれば問題無いですが、画像が多い場合はオプションで「メディアライブラリをエクスポートしない」をチェックしても良いでしょう。動作確認するだけなら、画像は必須ではありません。（ただし、画像を表示するプラグインを使用している場合などを除く）
### 2-2. LocalのインストールとWordPressのインストール
インストール手順については割愛させて頂きますが、基本的にインストールウィザードに従って進めるだけです。

インストール完了後はLocalを起動し、左下の＋（プラス）マークをクリックしてサイトを追加します。

1. "Create a new site"を選択します。
2. サイト名は自分が分かりやすいものを英数字で入力します。
3. "Environmet"（環境設定）では"Custom"を選択して実際に運用している環境に近いPHPバージョンとMySQLバージョンを選択します。なお、サーバーの種類はNginxでもApacheでもどちらでも問題無いと思います。
4. ユーザー名とパスワードを入力します。一般公開するサイトでもないので、testとかでも問題ないです。

暫く待ってサイトの追加が完了したら、右上の"Start Site"をクリックしてサイトを起動し、"WP Admin"ボタンをクリックして指定したユーザー名とパスワードで管理画面にログインします。

なお、WindowsでLocalの動作が異様に遅い（WordPressが重い）場合は、下記のフォーラムのスレッドを参考に設定を行ってみて下さい。（それでも、体感的にMacの方が早い気がします）

[Local is too slow with wordpress and windows 10](https://community.localwp.com/t/local-is-too-slow-with-wordpress-and-windows-10/26348/10)
### 2-3. サイトデータのインポート
管理画面にログインすると英語環境になっているので、"Setting"から"Site Language"を「日本語」にしておきます。

"All-in-One WP Migration"プラグインをインストールし、「インポート」から、先ほどエクスポートしたサイトデータを読み込み、暫く待ちます。

インポートが完了したら、再度ログインし直します。具体的にはURLに"`http://サイト名.local/wp-login.php`"を打ち込んで直接アクセスします。

ログイン後、データがインポートされていることを確認出来ればOKです。
## 3. 検証手順
## 4. こんな時どうする？問題別対処法
