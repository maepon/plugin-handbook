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

Debug Bar Cron adds information about WP scheduled events to a new panel in the Debug Bar. This plugin is an extension for Debug Bar and thus is dependent upon Debug Bar being installed for it to work properly.

Once installed, you will have access to the following information:

* Number of scheduled events
* If cron is currently running
* Time of next event
* Current time
* List of custom scheduled events
* List of core scheduled events
* List of schedules

[Visit Debug Bar Cron](https://wordpress.org/plugins/debug-bar-cron/)

## Debug Bar Actions and Filters Addon

This plugin adds two more tabs in the Debug Bar to display hooks(Actions and Filters) attached to the current request. Actions tab displays the actions hooked to current request. Filters tab displays the filter tags along with the functions attached to it with respective priority.

[Visit Debug Bar Actions and Filters Addon](https://wordpress.org/plugins/debug-bar-actions-and-filters-addon/)

## Debug Bar Transients

Debug Bar Transients adds information about WordPress Transients to a new panel in the Debug Bar. This plugin is an extension for Debug Bar and thus is dependent upon Debug Bar being installed for it to work properly.

Once installed, you will have access to the following information:

* Number of existing transients
* List of custom transients
* List of core transients
* List of custom site transients
* List of core site transients
* An option to delete a transient

[Visit Debug Bar Transients](https://wordpress.org/plugins/debug-bar-transients/)

## Debug Bar List Script & Style Dependencies

Lists scripts and styles that are loaded, in which order they’re loaded, and what dependencies exist.

[Visit Debug Bar List Script & Style Dependencies](https://wordpress.org/plugins/debug-bar-list-dependencies/)

## Debug Bar Remote Requests

This will log and profile remote requests made through the HTTP API.

This plugin will add a “Remote Requests” panel to Debug Bar that will display the:

* Request method (GET, POST, etc)
* URL
* Time per request
* Total time for all requests
* Total number of requests

Optionally, you can add ?dbrr_full=1 to your URL to get additional information, including all request parameters and a full dump of the response with headers.

[Visit Debug Bar Remote Requests](https://wordpress.org/plugins/debug-bar-remote-requests/)

## Handbook navigation
[← Developer Tools](../developer-tools/index.md)  
[Helper Plugins →](../developer-tools/helper-plugins/index.md)
