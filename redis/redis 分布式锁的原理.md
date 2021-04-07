>1，利用setNX的原子性
2，setNX会出现。 如果客户端获取了锁，某些操作阻塞的时间超过了该锁的有效时间，解锁的时候然后又删除了另一个客户端已经获得的锁 。
3、用lua，保证锁只允许加锁人解锁
4、redis分布式集群下下，setNx会失效。  官方提供了radLock
5、分析一手radLock的缺陷，推荐zk

lua是什么？

radLock是什么？

radLock缺陷？