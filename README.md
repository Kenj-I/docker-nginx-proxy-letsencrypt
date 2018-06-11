# nginx-proxy, letsencrypt

## description

dockerでnginx-proxy,letsencryptを使ってアクセスするためのcompose file

nginx_proxyで80,443ポート開放

Appコンテナで
VIRTUAL\_HOST=hogehoge.local
LETSENCRYPT\_HOST=hogehoge.local
と書いておくと自動で証明書を発行してhttps通信が可能になる

※（localで適当に設定したドメインは不可）

## usage

コンテナを起動する前にネットワークを作成して起動

```
$ docker network create [network_name]
$ docker-compose up --no-satart
$ docker-compose up -d
```

リポジトリ
https://github.com/jwilder/nginx-proxy
https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion

参考
https://suin.io/531
