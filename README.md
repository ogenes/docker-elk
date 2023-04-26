```shell
#下载
[root@ogenes01 data]#  git clone https://github.com/ogenes/docker-elk.git

#进入项目
[root@ogenes01 data]# cd docker-elk

#生成环境变量
[root@ogenes01 docker-elk]# cp .env.example .env

#创建网络，指定子网与.env中配置一致
[root@ogenes01 docker-elk]# docker network create backend --subnet=172.19.0.0/16
18f511530214374896700ad3f179fb9180227fe4e5b6ccf7e9f8ed9b8602059c
[root@ogenes01 docker-elk]# docker network ls | grep backend
18f511530214   backend   bridge    local

#启动
[root@ogenes01 docker-elk]# docker-compose up -d
[+] Running 4/0
 ⠿ Container es03    Running                                                                                                                                                   0.0s
 ⠿ Container es02    Running                                                                                                                                                    0.0s
 ⠿ Container es01    Running                                                                                                                                                    0.0s
 ⠿ Container kibana  Running                                                                                                                                                    0.0s
```
