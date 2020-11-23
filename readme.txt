1.进入相关模块，build DOCKER 镜像
docker build -t mall/mall-admin:1.0-SNAPSHOT .
cd ../mall-gateway
docker build -t mall/mall-gateway:1.0-SNAPSHOT .
cd ../mall-auth
docker build -t mall/mall-auth:1.0-SNAPSHOT .
cd ../mall-mbg
docker build -t mall/mall-mbg:1.0-SNAPSHOT .
cd ../mall-monitor
docker build -t mall/mall-monitor:1.0-SNAPSHOT .
cd ../mall-portal
docker build -t mall/mall-portal:1.0-SNAPSHOT .
cd ../mall-search
docker build -t mall/mall-search:1.0-SNAPSHOT .


2. Go to dir docker RUN docker-compose -f standalone-derby.yml up -d #运行NACOS DOCKER
docker-compose -f docker-compose-env-win.yml up -d #数据库ELK等其他docker

3. IN eclipse 中运行mall-gateway
( docker-compose -f docker-compose-app-win.yml up)


#docker exec -it  elasticsearch /bin/sh