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
