コンテナ作成後、コンテナ内のドキュメントルート直下で以下のコマンドを実行

# laravelのプロジェクト作成{poratl}はプロジェクト名のため可変になっているが
# ドキュメントルートを/var/www/html/portalを設定しているため、変更する場合は/app/apache/000-default.confを変更する
laravel new portal

#　デクレクトリ移動 
cd /var/www/html/portal

# 色々ライブラリ取得
npm install

# bootstrap
npm install bootstrap

# bootstrap icons
npm i bootstrap-icons

# webpack.mix.js
# 以下２レコードを追加、publicから資産の呼び出しをできるように変更
mix.copy('node_modules/bootstrap-icons', 'public/bootstrap-icons');
mix.copy('node_modules/bootstrap', 'public/bootstrap');

# session.php
# .envが優先

# app.php

/*
|--------------------------------------------------------------------------
| Application Timezone
|--------------------------------------------------------------------------
|
| Here you may specify the default timezone for your application, which
| will be used by the PHP date and date-time functions. We have gone
| ahead and set this to a sensible default for you out of the box.
|
*/

'timezone' => 'Asia/Tokyo',

/*
|--------------------------------------------------------------------------
| Application Locale Configuration
|--------------------------------------------------------------------------
|
| The application locale determines the default locale that will be used
| by the translation service provider. You are free to set this value
| to any of the locales which will be supported by the application.
|
*/

'locale' => 'ja',
