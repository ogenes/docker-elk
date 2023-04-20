```shell
#下载
[root@ogenes01 data]#  git clone https://github.com/ogenes/docker-elk.git

#进入项目
[root@ogenes01 data]# cd docker-elk

#生成环境变量
[root@ogenes01 docker-bitwarden]# cp .env.example .env

#创建网络，指定子网与.env中配置一致
[root@ogenes01 docker-bitwarden]# docker network create backend --subnet=172.19.0.0/16
18f511530214374896700ad3f179fb9180227fe4e5b6ccf7e9f8ed9b8602059c
[root@ogenes01 docker-bitwarden]# docker network ls | grep backend
18f511530214   backend   bridge    local
```
