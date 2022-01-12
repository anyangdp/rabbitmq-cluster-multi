# rabbitmq-cluster-multi（多机机群）
rabbitmq多机部署
- 拉取仓库
```
git clone https://github.com/anyangdp/rabbitmq-cluster-multi.git
```
- 集群配置统一cookie
```
chmod -R 400 .erlang.cookie
chmod -R 777 cluster-entrypoint.sh
```
- 安装部署
  - 分别将master、slave2、slave3发送至指定服务器
  - 修改slave2及slave3中的extra_hosts
  - 确保服务器端口开放
  - 依次分别启动master，slave2，slave3
- 启动命令
```
前台启动：docker-compose up
后台启动：docker-compose up -d
```
- 启动haproxy代理服务，修改其配置映射

- 访问web ui
http://ip:15672
- 客户端连接
ip:5672
- 默认账号密码：guest guest

https://www.jianshu.com/p/afa6b9dcbf13
