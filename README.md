# DockerでWordPress作成

## URL
- [WordPress](http://localhost:8080/)
- [phpMyAdmin](http://localhost:8888/)

## コンテナにログイン
```bash
# WordPress
docker exec -it wordpress-foo bash

# MySQL
docker exec -it mysql-foo bash
# bassh-4.2#
mysql -u root -p
```

## インストール
```bash
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
chmod +x wp-cli.phar
php wp-cli.phar core install --url=localhost:8080 --title=Example --admin_user=user --admin_password=passwd --admin_email=info@example.co.jp
php wp-cli.phar core install --url='localhost:8080' --title='たいとる' --admin_user=user --admin_password=passwd --admin_email=info@example.co.jp
```

## 参考サイト
### WordPress
- [初心者｜Docker-ComposeでWordPressとMySQLとphpMyAdminのローカル環境の構築 - Qiita](https://qiita.com/tomokei5634/items/75d2501cfb968d0cfab5)
- [リリース | WordPress.org 日本語](https://ja.wordpress.org/download/releases/)

### .env
- [Compose 内の環境変数 — Docker-docs-ja 20.10 ドキュメント](https://docs.docker.jp/compose/environment-variables.html)

### WP-CLI
- [Docker勉強](https://zenn.dev/hisho/scraps/69c78a6a81b51f)

### MySQL Workbench
### エクスポート、インポート、dump、ダンプ
- [MySQL Workbenchのエクスポート・インポート手順 | マコブログ](https://macoblog.com/mysql-workbench-export/)
- [データベースのImport・Export方法について(MySQL WorkBenchの場合) – ヘルプ - ロリポップ！マネージドクラウド](https://support.mc.lolipop.jp/hc/ja/articles/360033934213-%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9%E3%81%AEImport-Export%E6%96%B9%E6%B3%95%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6-MySQL-WorkBench%E3%81%AE%E5%A0%B4%E5%90%88-)

### mysqldump Version Mismatch
- [MySQL database backup using MySQL Workbench and how to resolve a version mismatch error | Winhost blog](https://blog.winhost.com/mysql-database-backup-using-mysql-workbench-and-how-to-resolve-a-version-mismatch-error/)
- [MySQLのWorkBentchからエクスポートしようとするとエラーになる](http://devlabo.blogspot.com/2013/06/mysqlworkbentch.html)
- [MySQL :: Download MySQL Community Server](https://dev.mysql.com/downloads/mysql/)

#### Windowsの場合
1. MySQLをダウンロード&解凍
1. MySQL WorkbenchのEdit > Preferencesを開く
1. Workbench Preferences > AdministrationのPath to mysqldump Tool:に上記のmysqldump.exeを指定する
