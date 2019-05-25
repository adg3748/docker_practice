# 使用するGolangのイメージを指定する
FROM golang:1.8

# 必要なパッケージなどなどをインストールする
RUN sed -i '/jessie-updates/d' /etc/apt/sources.list && apt-get update && apt-get install -y mysql-client vim

# ワーキングディレクトリを指定する
WORKDIR /go/src/sample_docker_compose

# sample_docker_compose直下のディレクトリをコンテナ上に載せる
ADD . .

# プロジェクトをビルド
RUN go build
