# LC_MySql
## 事务隔离级别
~~
## 锁
~~
## 分区
~~
## 分表之水平拆分和垂直拆分
~~
## 分库之水平拆分和垂直拆分
~~

## MYSQL索引失效的总结：
最佳左前缀法则：组合索引(带头大哥不能死，中间兄弟不能断) 

索引列上不计算：索引列不用函数，否则会导致索引丢失。

范围之后全失效：where q=2 and x>6 and y=1 会用到q索引，但是后面的y索引会失效

覆盖索引尽量用：在写sql不要使用select *，用什么字段就查询什么字段。

不等有时会失效：!=、<>

like百分比加右边：like 'XXX%'

字符要加单引号：如果没有加引号会进行类型转换，使用到了函数，会导致索引失效。

小表驱动大表：in/exisits 

等...

## mysql下载和安装
![image](https://user-images.githubusercontent.com/26539681/121656533-29503f80-cad2-11eb-9722-192e7bb10f5a.png)
![image](https://user-images.githubusercontent.com/26539681/121657500-083c1e80-cad3-11eb-9f58-7b23a5e67122.png)

## MySQL执行计划的内容是SQL调优时的一个重要依据，我们想要优化SQL语句就必须得先掌握执行计划。
![image](https://user-images.githubusercontent.com/26539681/121989239-5badb580-cdce-11eb-8f16-c22db6e21db5.png)
