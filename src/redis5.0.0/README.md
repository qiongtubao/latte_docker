#编译
docker build -t redis:5.0.0 .

#配置文件 
```
#bind 127.0.0.1
protected-mode no
appendonly yes
```
#启动
docker run -v $PWD/data:/data -p 6379:6379 --name redis -d redis:5.0.0 /redis/redis-server /data/redis.conf
#查看
docker ps

#停止
docker stop <id>

#删除
docker rm <id>