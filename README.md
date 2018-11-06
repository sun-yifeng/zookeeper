# 第2章节
1、官网tar安装（brew安装后集群有问题）
/Users/sunyifeng/program/zookeeper-3.4.10

2、启动服务器
bin/zkServer.sh start

3、启动客户端
bin/zkCli.sh

5、停止服务器
bin/zkServer.sh stop

6、使用命令
ls /
create workers ""
ls /
delete workers ""
ls /
quit

7、仲裁模式
#创建三份配置文件
cp conf/zoo_sample.cfg conf/zoo-1.cfg
cp conf/zoo_sample.cfg conf/zoo-2.cfg
cp conf/zoo_sample.cfg conf/zoo-3.cfg
#启动服务端
bin/zkServer.sh start-foreground z3/zoo-3.cfg
bin/zkServer.sh start-foreground z3/zoo-3.cfg
bin/zkServer.sh start-foreground z3/zoo-3.cfg
#客户端访问
$ZK_HOME/bin/zkCli.sh -server 127.0.0.1:2181,127.0.0.1:2183,127.0.0.1:2183

