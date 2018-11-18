//启动postgresql
docker run --name postgres1 -e POSTGRES_PASSWORD=tubaoge -p 5432:5432 -d postgres:9.6  

//打开客户端
cd /Users/zhouguodong/Documents/Tools/sql/bdash
yarn start