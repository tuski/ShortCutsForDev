install redis
brew install redis

create directory 
Create directory anywhere<any>/7000, <any>/7001, <any>/7002 Create redis.conf inside each directory.~/dev/redis/7000 ❯ cat redis.conf

create conf file 
touch redis.conf

and put below config
port 7001
cluster-enabled yes
cluster-config-file 7001/nodes.conf
daemonize yes


Change access to 755
chmod 755 */redis.conf

Run each one redis-server
redis-server /Users/mohaimanul.islam/Downloads/redisconf/7001/redis.conf
redis-server /Users/mohaimanul.islam/Downloads/redisconf/7002/redis.conf
redis-server /Users/mohaimanul.islam/Downloads/redisconf/7003/redis.conf

Run cluster
redis-cli --cluster create 127.0.0.1:7001 127.0.0.1:7002 127.0.0.1:7003


Cluster reset
redis-cli -h 127.0.0.1 -c CLUSTER RESET


check redis bin file
redis-server/usr/local/Cellar/redis/6.2.6/bin

check process
Check if redis is running 
ps -ef | grep 'redis-server *'
ps aux | grep redis


check cli
redis-cli

shutdown server
redis-cli -p 7001 shutdown
redis-cli -p 7002 shutdown
redis-cli -p 7003 shutdown


to flush db
redis-cli -p 7001
127.0.0.1:7000> flushdb
127.0.0.1:7000> flushall
127.0.0.1:7000> exit


127.0.0.1:7001,127.0.0.1:7002,127.0.0.1:7003
