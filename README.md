Filebeat => Redis => ELK

1. 取得文件

$ git clone "https://github.com/come706/Learn_docker-elk.git"
$ CD Learn_docker-elk

2. 修改 filebeat 設定
docker-compose.yml
找到 filebeat 的 volumes
修改測試路徑

3. 啟動
$ docker-compose up -d

4. 啟動kibana
http://localhost:5601/
account: elastic
pwd: 123456

Management->Logstash->Pipelines->add
Pipeline ID: core.app
加上規則，儲存。

Discover->add->Index Patterns

credit_auth_redis_*


From:
https://github.com/wilfordw/docker-elk-example
