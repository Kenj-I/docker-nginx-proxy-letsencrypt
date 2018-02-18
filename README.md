# description

dockerでvirtualhostでアクセスするためのコンテナ

virtualhostでアクセスしたいコンテナのdocker-compose.ymlで
80番ポートをexposeして、environmentオプションでVIRTUAL\_HOST=hogehoge.localと書くと
自動的に検知されてアクセスできる

コンテナを起動する前にネットワークを作成しておく

```
$ docker network create [network_name]
```

リポジトリ
https://github.com/jwilder/nginx-proxy

参考
https://suin.io/531
