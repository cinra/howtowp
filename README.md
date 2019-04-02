# How to build the wordpress site

## 1. Git

- [ ] Gitをインストール
- [ ] 当リポジトリをfork
- [ ] リポジトリをローカルにclone

## 2. Docker

- [ ] Docker for Macをインストール
- [ ] Docker Composeを用いて、Docker Imageをbuild
- [ ] hostsを使ってドメインを登録
- [ ] Docker Composeを用いて、コンテナを立ち上げる

## 3. Wordpress

- [ ] `http://wp.test`にアクセスして、Wordpressをインストールする
- [ ] Wordpressの管理画面にログインする

## 4. MySQL

- [ ] Dockerコンテナ`wp_mysql`をexec
- [ ] MySQLの内容を`develop.sql`という名前でエクスポート

## 5. Node

- [ ] NVMをインストール
- [ ] yarnをインストール

## 6. Nuxt

- [ ] Nuxtを立ち上げる
- [ ] `http://localhost:3000`にアクセス



---

### hostsの書き換え

```
$ vi /etc/hosts
```

### Docker Composeを用いた、Docker Imageのbuild

```
$ docker-compose build
```

### Docker Composeを用いた、Dockerコンテナの立ち上げ

```
$ docker-compose up -d
```

### Dockerコンテナを実行

```
$ docker exec {{ コンテナ名 }}
```

例：MySQLのコンテナにログインする

```
$ docker exec -it wp_mysql bash
```

### Nuxtの立ち上げ

```
$ cd src
$ yarn run dev
```