<h1>Plugin Basics</h1>

# プラグインの基本

<h2 class="toc-heading" id="getting-started" tabindex="-1">Getting Started <a href="#getting-started" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">Getting Started</span></a></h2>

## Getting Started

<p>At its simplest, a WordPress plugin is a PHP file with a WordPress plugin header comment.
It’s highly recommended that you create a directory to hold your plugin so that all of your plugin’s files are neatly organized in one place.</p>

もっとも単純なプラグインは、WordPressプラグインのヘッダーコメントのPHPファイルです。
作成するプラグインのファイルが一箇所に整理されているような形で、保持するディレクトリを用意することを強く推奨します。

<p>To get started creating a new plugin, follow the steps below.</p>

あたらしいプラグインの作成をはじめるにあたって、下記の手順を踏んでください。

<ol>
<li>Navigate to your WordPress installation’s&nbsp;<strong>wp-content</strong> directory.</li>
<li>Open&nbsp;the <strong>plugins</strong> directory.</li>
<li>Create a new directory and name it after your plugin (e.g. <code>plugin-name</code>).</li>
<li>Open&nbsp;your new plugin’s directory.</li>
<li>Create a new PHP file (it’s also good to name this file after your plugin, e.g. <code>plugin-name.php</code>).</li>
</ol>

1. インストールしたWordPressの**wp-content**ディレクトリに移動します。
2. **plugins**ディレクトリを開きます。
3. 新しくディレクトリを作成し、プラグインの名前で命名します（例：**plugin-name**）。
4. 新しいプラグインのディレクトリを開きます。
5. PHPファイルを作成します（ファイル名は、プラグインの名前で命名すると良いでしょう。例：**plugin-name.php**）

<p>Here’s what the process looks like on the Unix command line:</p>

以下がUnixのコマンドラインでの手順です：

```PHP
wordpress$ cd wp-content
wp-content$ cd plugins
plugins$ mkdir plugin-name
plugins$ cd plugin-name
plugin-name$ vi plugin-name.php
```

<p>In the example above, “vi” is the name of the text editor. Use whichever editor that is comfortable for you.</p>

上記の例の「vi」はテキストエディタの名前です。普段利用しているエディターの名前を入れてください。

<p>Now that you’re editing your new plugin’s PHP file, you’ll need to add a <strong>plugin header comment</strong>. &nbsp;This is a specially formatted PHP block comment that contains metadata about your plugin, such as its name and author. &nbsp;At the very least, the plugin header comment must contain the <strong>name</strong> of your plugin. &nbsp;Only <strong>one file</strong> in your&nbsp;plugin’s folder should have the header comment—if your plugin has multiple PHP files, only one of those files should have the comment.</p>

新しいプラグインのファイルを編集する時に、**plugin header comment**を記述する必要があります。これはプラグインの名前や作成者などのメタデータを含んだ、このためにフォーマットを定められたPHPのブロックコメントです。最低限、plugin header commentにはプラグインの**name**を含める必要があります。プラグインのフォルダー内のファイルの一つだけがplugin header commentを持つべきです。プラグインが、複数のPHPファイルで構成されている場合、その中の一つのファイルがplugin header commentを持つべきです。

```PHP
<?php
/*
Plugin Name: YOUR PLUGIN NAME
*/
```

<p>After you save the file, you should be able to see your plugin listed in your WordPress site. Log in to your WordPress site, and click <strong>Plugins</strong> on the left navigation pane of your WordPress Admin. This page displays a listing of all the plugins your&nbsp;WordPress site has. Your new plugin should now be in that list!</p>

ファイルを保存すると、WordPressで作成したサイトにあなたのプラグインがリストに加えられたか確認できます。WordPressで作成したサイトにログインし、WordPressの管理画面の左ナビゲーションの**プラグイン**をクリックします。その画面ではWordPressで作成したサイトに登録されているすべてのプラグインの一覧が表示しています。あなたが作成した新しいプラグインも一覧の中に加えられているでしょう！

<h2 class="toc-heading" id="hooks-actions-and-filters" tabindex="-1">Hooks: Actions and Filters <a href="#hooks-actions-and-filters" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">Hooks: Actions and Filters</span></a></h2>

<p>WordPress hooks allow you&nbsp;to tap into WordPress at specific points to change how WordPress behaves without editing any core files.</p>

<p>There are two types of hooks within WordPress: <em>actions</em> and <em>filters</em>. Actions allow you to add or change WordPress functionality, while filters allow you to alter&nbsp;content as it is loaded and displayed to the website user.</p>

<p>Hooks are not just for plugin developers; hooks are used extensively to provide default functionality by WordPress core itself. Other&nbsp;hooks are unused place holders that are simply available for you to tap into when you need to alter how WordPress works. This is what makes WordPress so flexible.</p>

<h3 class="toc-heading" id="basic-hooks" tabindex="-1">Basic Hooks <a href="#basic-hooks" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">Basic Hooks</span></a></h3>

<p>The 3 basic hooks you’ll need when creating a plugin are the <a href="https://developer.wordpress.org/reference/functions/register_activation_hook/">register_activation_hook()</a>, <a href="https://developer.wordpress.org/reference/functions/register_deactivation_hook/">register_deactivation_hook()</a>&nbsp;and the <a href="https://developer.wordpress.org/reference/functions/register_uninstall_hook/">register_uninstall_hook()</a>.</p>

<p>The <a href="https://developer.wordpress.org/plugins/the-basics/activation-deactivation-hooks/">activation hook</a> is run when you <em>activate</em> your plugin. You would use this to provide a function to set up your plugin — for example, creating some default settings in the <code>options</code> table.</p>

<p>The <a href="https://developer.wordpress.org/plugins/the-basics/activation-deactivation-hooks/">deactivation hook</a> is run when you <em>deactivate</em> your plugin. You would use this to provide a function that clears any temporary data stores by your plugin.</p>

<p>These <a href="https://developer.wordpress.org/plugins/the-basics/uninstall-methods/">uninstall methods</a> are used to clean up after your plugin is <em>deleted</em> using the WordPress Admin. You would use this to delete all data created by your plugin, such as any options that were added to the <code>options</code> table.</p>

<h3 class="toc-heading" id="adding-hooks" tabindex="-1">Adding Hooks <a href="#adding-hooks" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">Adding Hooks</span></a></h3>

<p>You can add your own, custom hooks with <a href="https://developer.wordpress.org/reference/functions/do_action/">do_action()</a>, which will enable developers to extend your plugin by passing functions through your hooks.</p>

<h3 class="toc-heading" id="removing-hooks" tabindex="-1">Removing Hooks <a href="#removing-hooks" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">Removing Hooks</span></a></h3>

<p>You can also use invoke <a href="https://developer.wordpress.org/reference/functions/remove_action/">remove_action()</a> to remove a function that was defined earlier. For example, if your plugin is an add-on to another plugin, you can use <a href="https://developer.wordpress.org/reference/functions/remove_action/">remove_action()</a> with the same function callback that was added by the previous plugin with <a href="https://developer.wordpress.org/reference/functions/add_action/">add_action()</a>. The priority of actions is important in these situations, as <a href="https://developer.wordpress.org/reference/functions/remove_action/">remove_action()</a> would need to run after the initial <a href="https://developer.wordpress.org/reference/functions/add_action/">add_action()</a>.</p>

<p>You should be careful when removing an action from a hook, as well as when altering priorities, because it can be difficult to see how these changes will affect other interactions with the same hook. We highly recommend testing frequently.</p>

<p>You can learn more about creating hooks and interacting with them in the <a href="https://developer.wordpress.org/plugin/hooks/">Hooks</a> section of this handbook.</p>

<h2 class="toc-heading" id="wordpress-apis" tabindex="-1">WordPress APIs <a href="#wordpress-apis" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">WordPress APIs</span></a></h2>

<p>Did you know that WordPress provides a number of <a href="https://make.wordpress.org/core/handbook/core-apis/">Application Programming Interfaces (APIs)</a>? These APIs can greatly simplify the code you need to write in your plugins. You don’t want to reinvent the wheel, especially when so many people have done a lot of the work and testing for you.</p>

<p>The most common one is the <a href="https://codex.wordpress.org/Options_API">Options API</a>, which makes it easy to store data in the database for your plugin. If you’re thinking of using <a href="https://en.wikipedia.org/wiki/CURL" target="_blank">cURL</a> in your plugin, the <a href="https://codex.wordpress.org/HTTP_API">HTTP API</a> might be of interest to you.</p>

<p>Since we’re talking about plugins, you’ll want to study the <a href="https://codex.wordpress.org/Plugin_API">Plugin API</a>. It has a variety of functions that will assist you in developing plugins.</p>

<h2 class="toc-heading" id="how-wordpress-loads-plugins" tabindex="-1">How WordPress Loads Plugins <a href="#how-wordpress-loads-plugins" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">How WordPress Loads Plugins</span></a></h2>

<p>When WordPress loads the list of installed plugins&nbsp;on the Plugins page of the WordPress Admin, it searches through the <code>plugins</code> folder (and its sub-folders) to find PHP files with WordPress plugin header comments. If your entire plugin consists of just a single PHP&nbsp;file, like <a title="Hello Dolly" href="https://wordpress.org/plugins/hello-dolly/">Hello Dolly</a>, the file could be located directly inside the root of the <code>plugins</code> folder. But more commonly, plugin files will reside in their own folder, named after the plugin.</p>

<h2 class="toc-heading" id="sharing-your-plugin" tabindex="-1">Sharing your Plugin <a href="#sharing-your-plugin" class="anchor"><span aria-hidden="true">#</span><span class="screen-reader-text">Sharing your Plugin</span></a></h2>

<p>Sometimes a plugin you create is just for your site. But many people like&nbsp;to share their plugins with the rest of the WordPress community. Before sharing your plugin, one thing you need to do is&nbsp;<a href="https://opensource.org/licenses/category">choose a license</a>. This lets the user of your plugin know how they are allowed to&nbsp;use your code. To maintain compatibility with WordPress core, it is recommended that you pick a license that works with GNU General Public License (GPLv2+).</p>
