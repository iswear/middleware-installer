```bash

# docker 中下载 mysql
docker pull mysql:latest

#启动
docker run --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 -d mysql:latest

#进入容器
docker exec -it mysql bash

#登录mysql
mysql -uroot -p123456
ALTER USER 'root'@'localhost' IDENTIFIED BY '123456';

#添加远程登录用户
CREATE USER 'iswear'@'%' IDENTIFIED WITH mysql_native_password BY '123456';
GRANT ALL PRIVILEGES ON *.* TO 'iswear'@'%';

```