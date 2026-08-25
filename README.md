# php-apache
Dockerを使用してPHP+Apacheの実行環境を構築する

# Dockerコンテナを起動する手順

1. ローカルフォルダに`src`フォルダを作成する
2. `src`フォルダ配下に`index.php`ファイルを作成する
3. DockerHubからPHP公式イメージを取得しDockerコンテナを起動するコマンドを実行する

```shell
docker run -d -p 80:80 --name php-apache -v ./src:/var/www/html php:8.4-apache
```
※ `php:8.4-apache`のバージョン部分（`8.4`）を変更することで他のバージョンのPHP実行環境を構築することができます

# Dockerコンテナを停止・削除する手順

1. Dockerコンテナを停止する

```shell
docker stop php-apache
```

2. Dockerコンテナを削除する

```shell
docker rm php-apache
```

3. Dockerイメージを削除する

```shell
docker rmi [イメージID]
```
