# Redis
是一个开源的使用ANSI C语言编写、遵守BSD协议、支持网络、可基于内存亦可持久化的日志型、Key-Value数据库，并提供多种语言的API
它通常被称为数据结构服务器，因为值（value）可以是 字符串(String), 哈希(Map), 列表(list), 集合(sets) 和 有序集合(sorted sets)等类型。
a）Redis支持数据的持久化，可以将内存中的数据保存在磁盘中，重启的时候可以再次加载进行使用。
b)Redis不仅仅支持简单的key-value类型的数据，同时还提供list，set，zset，hash等数据结构的存储。
c)Redis支持数据的备份，即master-slave模式的数据备份。
（1）安装
    下载地址：https://github.com/MSOpenTech/redis/releases
    打开cmd,将路径切换到下载的redis文件夹，运行 redis-server.exe redis.windows.conf
    这时候另启一个cmd窗口，原来的不要关闭，不然就无法访问服务端了。
    切换到redis目录下运行 redis-cli.exe -h 127.0.0.1 -p 6379 。
    设置键值对 set myKey abc
    取出键值对 get myKey
 (2)注意点：
    我再使用RedisUtil时，总是会碰到一个错误ERR Client sent AUTH, but no password is set和could not get a resource from the pool
    解决方法：
    a）切换到redis目录下运行 redis-cli.exe -h 127.0.0.1 -p 6379
    b）设置redis密码 CONFIG SET requirepass "123456"
    c）验证 AUTH 123456
    
 应用场景：
 热数据，尤其是写入比较频繁的热数据，如果量比较小，最适合放于redis中
 例如：网站注册用户，网站访问量，邮箱激活码
 数据量太大情况不适合用redis，消耗内存
 
 
    

