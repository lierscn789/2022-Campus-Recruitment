面经

1、英文自我介绍

忘记准备了，想死

2、实习工作内容

3、算法题

https://leetcode-cn.com/problems/single-element-in-a-sorted-array/

4、vector的扩容机制？

2倍扩容和1.5倍扩容

1230
1234
12345000
5、扩容后之前的内存是否还会使用

聊了聊空间配置器。Realloc

6、虚函数和抽象类？
7、TCP和UDP的区别

可靠传输协议
面向报文
字节流->粘包
拥塞控制、
不可能三角：可靠性、实时性、公平性（拥塞控制）

场景：

HTTP3、QUIC


8、如何分包？http的分包方式，设计一个RPC框架中应该如何分包？
content-length

9、长连接和短连接使用场景？
正向代理和反向代理？？？

9、HTTP请求过程？
HTTP报文格式
get get url 版本
keep-alive

DNS
读浏览器缓存、本地host文件、本地dns服务器、根dns服务器、域dns服务器、下一级域dns服务器

TCP
IP
10、讲一讲操作系统中的虚拟内存机制？
页表项：页框号+控制位
是否有虚拟页号？？？
内存交换中涉及到哪些技术？
LRU、每次一起换入相邻页


11、如果要设计一个索引，可以用哪些数据结构？如何选择？
哈希索引、二叉搜索树
b+树和b树
哈希冲突如何解决

12、如果要对一个数据库进行分表，如何平滑地进行，不影响线上的操作？
中间件
client 和 mysql server 中 加一层
垂直分库，垂直分表，水平分库，水平分表

15、sql优化：
select * from user where create_time between '2019-01-01' and '2020-01-01'  order by create_time limit 100000,10;


select * from user
where create_time between '2019-01-01' and '2020-01-01'
order by create_time limit 100000, 10;

select *
from user
where id in(
	select id from user
	where create_time between '2019-01-01' and '2020-01-01'
	order by create_time limit 100000, 10
)



16、InnoDB的隔离级别和实现方式？
Undo log
Next-key lock
Redo log
Binlog

17、Redis有哪些数据结构？各自在哪些场景可以使用？
list、set、zset

消息队列
查找相同好友
zset，支持范围查找，score，热榜排序

18、讲一讲跳表
链表、二分思想、多级索引

19、如何给跳表加锁？

20、CAS算法聊一聊？底层实现是什么？
比较并交换，

21、从磁盘中读取一个文件并发送到网络中有几次拷贝？
磁盘->内核缓冲区->用户缓冲区->内核缓冲区->网卡
磁盘->内核缓冲区->内核缓冲区->网卡
零拷贝：mmap
22、Golang如果一个线程要等待其他线程完成，怎么做？
23、如何用C++实现defer（设计一个变量，注册一个函数，析构时调用）




