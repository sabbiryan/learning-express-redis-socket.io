### learning-express-redis-socket.io

### Docker commands

<strong>Start redis server:</strong> docker run --name packt-redis -p 16379:6379 -d redis:3.2.4 <br/>
<strong>Connect redis-cli:</strong> docker run -it --link packt-redis:redis --rm redis redis-cli -h redis -p 6379 <br/>
<strong>Stop redis server:</strong> docker stop packt-redis <br/>
<strong>Restart redis server:</strong> docker start packt-redis
<strong>Redis-cli help:</strong> docker run -it --rm redis redis-cli --help

### Redis cli commands
help set <br/>
help get <br/>
set TEST_KEY "test value" <br/>
get TEST_KEY <br/>
set user:1:username sabbir <br/>
get user:1:username <br/>
<br/>

### Redis data types
hmset user:1 first_name Sabbir last_name Ahamed <br/>
get hgetall user:1 <br/>
<br/>
lpush user:1:profile_views 5 <br/>
lpush user:1:profile_views 10 <br/>
lpush user:1:profile_views 15 <br/>
lpush user:1:profile_views 18 <br/>
lrange user:1:profile_views 0 -1 <br/>
<br/>
sadd post:1:users 1 2 <br/>
sadd post:1:users 1 <br/>
smembers post:1:users <br/>
sadd post:1:users 3 <br/>
smembers post:1:users <br/>
<br/>
zadd logins 500 1 <br/>
zadd logins 600 15 <br/>
zadd logins 650 18 <br/>
zrange logins 0-1 <br/>
zadd logins 550 20  <br/>
zrange logins 0-1 <br/>
zrange logins 0 -1 WITHSCORES <br/>
zremrange logins 0 -1 <br/>
 <br/>

