#Atlas后端连接的MySQL主库的IP和端口，可设置多项，用逗号分隔
proxy-backend-addresses = ${MYSQL_MASTER_HOST}:3306,${MYSQL_SLAVE_HOST}:3306

#Atlas后端连接的MySQL从库的IP和端口，@后面的数字代表权重，用来作负载均衡，若省略则默认为1，可设置多项，用逗号分隔
#proxy-read-only-backend-addresses = ${MYSQL_SLAVE_HOST}:3306@1

#用户名与其对应的加密过的MySQL密码，密码使用PREFIX/bin目录下的加密程序encrypt加密，下行的user1和user2为示例，将其替换为你的MySQL的用户名和加密密码！
pwds = ${MYSQL_USERNAME}:$(/usr/local/mysql-proxy/bin/encrypt ${MYSQL_PASSWORD})
