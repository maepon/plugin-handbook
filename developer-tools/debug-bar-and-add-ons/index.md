# デバッグバーとアドオン

## Debug Bar

Debug Bar は、有効化されているときにクエリ、キャッシュ、その他の有用なデバッグ情報を表示するデバッグメニューを管理バーに追加します。  
WP_DEBUG が有効化されていると、PHPの警告と注意を追跡して見つけやすくなります。  
SAVEQUERIES を有効化すると、mysql クエリが追跡されて表示されます。

[Debug Bar を見る](https://wordpress.org/plugins/debug-bar/)

## Debug Bar Console

このプラグインは、任意のPHPを実行できる大きなテキストエリアを提供します。  
変数などの内容をテストするのに優れています。

[Debug Bar Console を見る](https://wordpress.org/plugins/debug-bar-console/)

## Debug Bar Shortcodes

Debug Bar Shortcodes は、現在のリクエストに登録されたショートコードを表示する新しいパネルをデバッグバーに追加します。

さらに、これらが表示されます：

* ショートコードによって呼ばれた関数やメソッド
* ショートコードが現在の投稿/ページ/投稿タイプに使われているかどうか（シングルページのみ）
* ショートコードに関する概要、パラメータ、自己完結型かどうかの追加情報
* ショートコードが使われているすべてのページ/投稿などを探す

[Debug Bar Shortcodes を見る](https://wordpress.org/plugins/debug-bar-shortcodes/)

## Debug Bar Constants

リクエストの管理者として利用可能な定義済みの定数を表示する新しい3つのパネルを追加します：

* WP 定数
* WP クラス定数
* PHP 定数

[Debug Bar Constants を見る](https://wordpress.org/plugins/debug-bar-constants/)

## Debug Bar Post Types

Debug Bar Post Types はサイトに登録されている投稿タイプの詳細情報を表示する新しいパネルをデバッグバーに追加します。

[Debug Bar Post Types を見る](https://wordpress.org/plugins/debug-bar-post-types/)

## Debug Bar Cron

Debug Bar Cron はWPスケジュールイベントに関する情報をDebug Bar の新しいパネルに追加します。このプラグインはDebug Bar の拡張機能で、Debug Bar が正しく動作するようにインストールされているかどうかに依存します。

インストールすると、次の情報にアクセスできるようになります：

* スケジュールされたイベントの数
* cronが現在実行中の場合
* 次のイベントの時間
* 今の時間
* カスタムスケジュールイベントのリスト
* コアのスケジュールイベントのリスト
* スケジュールのリスト

[Debug Bar Cron を見る](https://wordpress.org/plugins/debug-bar-cron/)

## Debug Bar Actions and Filters Addon

このプラグインは、デバッグバーに2つのタブを追加して、現在のリクエストに関連付けられたフック（アクションとフィルタ）を表示します。 アクションタブには、現在の要求にフックされたアクションが表示され、フィルタタブには、それぞれの優先度でフィルタタグが関連付けられた機能と一緒に表示されます。

[Debug Bar Actions and Filters Addon を見る](https://wordpress.org/plugins/debug-bar-actions-and-filters-addon/)

## Debug Bar Transients

Debug Bar Transients はWordPress の一時的な情報をデバッグバーの新しいパネルに追加します。このプラグインはDebug Bar の拡張機能で、Debug Bar が正しく動作するようにインストールされているかどうかに依存します。

インストールすると、次の情報にアクセスできるようになります：

* 既存のトランジェントの数
* カスタムされたトランジェントのリスト
* コアのトランジェントのリスト
* カスタムサイトの遷移のリスト
* コアサイトの遷移のリスト
* 一時的なものを削除するオプション

[Debug Bar Transients を見る](https://wordpress.org/plugins/debug-bar-transients/)

## Debug Bar List Script & Style Dependencies

ロードされるスクリプトとスタイル、ロードされた順序、依存関係のリストを表示します。

[Debug Bar List Script & Style Dependencies を見る](https://wordpress.org/plugins/debug-bar-list-dependencies/)

## Debug Bar Remote Requests

HTTP APIを介して行われたリモート要求のログとプロファイルが行われます。

このプラグインは、デバッグバーに「Remote Requests」パネルを追加し、次の情報を表示します：

* リクエストメソッド (GET、POSTなど)
* URL
* リクエストの時間
* すべてのリクエストの合計時間
* リクエストの合計数

必要に応じてURLに `?dbrr_full=1` というパラメーターを追加すれば、すべてのリクエストパラメータとヘッダー付きの完全な応答を含む追加情報を取得できます。

[Debug Bar Remote Requests を見る](https://wordpress.org/plugins/debug-bar-remote-requests/)
