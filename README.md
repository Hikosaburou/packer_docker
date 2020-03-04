# packer_docker
Dockerコンテナをpackerで焼いてみる


# 目的
Amazon Linux 2 AMIを焼くときに何かと時間がかかるので、Dockerを使って時間短縮したい。

# やっていること

- Docker Image を Packer で焼く
    - AMIを焼くときに必要なコマンド群をあらかじめ導入する
    - `ec2-user` ユーザーとして各種コマンドを実行する
        - Shell Provisioner の使用飲み想定している。
        - AnsibleやChefの場合の手順はわからない

# Usage

```
packer build docker.json
```

# ToDo

- AMI作成をエミュレートするための Shell Provisioner 部分をあらかじめDocker Image化する
    - Dockerfile を作る
- AWSのAPIを叩くための認証情報周りの整理