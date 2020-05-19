## Project
ELK Apache Log

---
## 概要
Apacheログ解析用のELK環境
既に存在しているApacheのログをディレクトリへコピーするだけでkibanaで見たいという思いで作ったもの

---
## 環境
* elasticsearch
* logstash
* kibana

---
## 確認手順

```bash
git clone git@github.com:s-fukumoto/elk-apache-log.git

cd elk-apache-log

# 環境設定
cp .env.sample .env
vi .env

# logstash設定（適宜変更）
cp ./logstash/pipeline/logstash.conf.sample ./logstash/pipeline/logstash.conf
vi ./logstash/pipeline/logstash.conf

docker-compose up -d
```

あとは、`./logstash/input/httpd` へ `access.log` を放り込むだけ
