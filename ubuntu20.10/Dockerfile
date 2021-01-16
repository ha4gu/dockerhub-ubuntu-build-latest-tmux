# Ubuntu 20.10の通常サポート期限: 2021年7月
FROM ubuntu:20.10

# 必須パッケージの導入
RUN apt-get update -qq &&\
    DEBCONF_NOWARNINGS=yes apt-get install -y -q --no-install-recommends \
      curl ca-certificates &&\
    apt-get clean &&\
    rm -rf /var/lib/apt/lists/*

# ビルドスクリプトの実行
CMD curl -sSL https://raw.githubusercontent.com/ha4gu/tmux-build-check/master/tmux-build-check.sh | bash -
