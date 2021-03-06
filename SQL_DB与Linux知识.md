#	数据库Database

 种类：MYSQL（web关系型数据库），mongoDB（非关系型数据库（爬虫）），redis（缓存），ACCESS，SQL server（微软项目），Oracle（大型项目，收费），sqlite（轻量级数据库）

区分：关系型数据库RDBMS程序/非关系型数据库

 

关系型数据库：行-名称；列-数据域，表格形式，行列组成表单，表单组成database

SQL structured query language 结构化查询语言，操作和MySQL基本一致,不区分大小写

结构化查询语言：

1. **数据查询语言**（DQL:Data Query Language）：SELECT

2. **数据操作语言**（DML：Data Manipulation Language）：INSERT，UPDATE和DELETE

3. 事务处理语言（TPL）：BEGIN TRANSACTION，COMMIT和ROLLBACK

4. 数据控制语言（DCL）：GRANT（授权）或REVOKE（回收权限）

5. 数据定义语言（DDL）：CREATE、ALTER和DROP

6. 指针控制语言（CCL）：DECLARE CURSOR，FETCH INTO和UPDATE WHERE CURRENT用于对一个或多个表单独行的操作



数据库、数据表、列、行、冗余、主键、外键、复合键、索引、参照完整性



#### 操作数据库/表

```SQL
create database [if not exists] `数据库名` charset=字符编码(utf8mb4);//创建数据库
show database/tables; //查看数据库/表
use'数据库的名字'; //选择数据库
create database/table'数据库/表名'; //创建数据库
alter database/table '数据库/表名' charset=字符集; //修改数据库
alter table '表名' drop '字段名' ; //删除字段
drop database/table [if exists] '数据库/表的名字' ;
insert into '表名' ; //数据
select * from '表名' where ...; //查数据
desc '表名'; //查字段

```



表的操作:

C: 创建（Create）	U: 更新（Update）	R: 读取（Retrieve）	

D: 删除（Delete）	I:  插入  (Insert)	 U: 更新  (Update)





#### SQL

关系型数据库Structured Query Language



语法表

| **数字where**       | **文本where** | **排序rows** | **Join连表（table）** | **算式（select/where）** | **统计（select）**      | **子表（table）**  |
| ------------------- | ------------- | ------------ | --------------------- | ------------------------ | ----------------------- | ------------------ |
| =, !=, < ,<=, >, >= | =             | ORDER BY     | JOIN ...ON...         | + - * / %                | COUNT(*), COUNT(column) | （select -）as tmp |
| BETWEEN … AND …     | ！= or <>     | ASC          | INNER JOIN            | substr                   | MIN()                   | in（select -）     |
| NOT BETWEEN … AND … | like          | DESC         | LEFT JOIN             | AS                       | MAX()                   | avg（select -）    |
| IN (…)              | NOT LIKE      | LIMIT OFFSET | RIGHT JOIN            |                          | AVG()                   |                    |
| NOT IN (…)          | %             | ORDER BY     | IS/IS NOT NULL        |                          | GROUP BY                |                    |
|                     | -             |              |                       |                          | HAVING                  |                    |
|                     | IN()          |              |                       |                          |                         |                    |
|                     | NOT IN()      |              |                       |                          |                         |                    |

 

 

语法手册：

Col（数字=n；/文本like ’%  ’）

Rows排序

Join 连接表table

Select 找什么 from 从哪找 where 按什么条件找

 

 语法词条：

 

Select title from table			--从表table查询title

Select * from table

Select title1，title2 from table where id < 5			--从表table中查找id小于5时列title1和title2的值

Select 1+2*3/4-(5%6) 			--select直接做算术运算

Select Distinct 				--选取出唯一结果的语法

Order By column ASC/DESC			--***\*结果排序\****（ASC升序/DESC降序）

Limit--返回多少行/Offset--从哪一行开始返回

SELECT * FROM table Order by Title ASC limit 5 OFFSET 5		--升序排列后列出前五个的后五个

Select Title From Movies Where Director='John Lasseter' order by Length_minutes DESC limit 1 Offset 2

--按title排列，从movies中找Director是John Lasseter的 ，条件是第三长的

***\*连表操作\****

数据库范式normalization：数据表设计的规范

多表连接技术（多表联合查询）JOINs

主键primary key（唯一属性）

INNER JOIN another_table 		--内连接

 ON mytable.id = another_table.id （两个表合并）

 

Outer Joins			--外连接（会保留不能匹配的行）

左连接LEFT JOIN（保留A）

右连接RIGHT JOIN（保留B）

全连接FULL JOIN（全保留）

Is Null/Is Not Null			--用NULL填充不存在的数据

As 			--取别名

 

***\*在查询中用到\*******\*包含表达式的例子\****

SELECT  particle_speed / 2.0 AS half_particle_speed (对结果做了一个除2）

FROM physics_data

WHERE ABS(particle_position) * 10.0 >500

​      （条件要求这个属性绝对值乘以10大于500）;

 

| Function                                  | Description                                                  |
| ----------------------------------------- | ------------------------------------------------------------ |
| **COUNT(*****)**, **COUNT(***column***)** | 计数！COUNT(*) 统计数据行数，COUNT(column) 统计column非NULL的行数. |
| **MIN(***column***)**                     | 找column最小的一行.                                          |
| **MAX(***column***)**                     | 找column最大的一行.                                          |
| **AVG(***column*)                         | 对column所有行取平均值.                                      |
| **SUM(***column***)**                     | 对column所有行求和.                                          |

 

分组统计 ：Group By 数据分组统计

 

 

**用HAVING对分组后的数据进行筛选**

SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, …

FROM mytable

WHERE condition

GROUP BY column

HAVING group_condition;

 

**此条包含SQL所有语法**

```sql
SELECT DISTINCT column, AGG_FUNC(column_or_expression), …

FROM mytable//从上到下执行顺序

  JOIN another_table

   ON mytable.column = another_table.column

  WHERE constraint_expression

  GROUP BY column

  HAVING constraint_expression

  ORDER BY column ASC/DESC

LIMIT count OFFSET COUNT;

```

 

 

资源:

了解篇——[廖雪峰网站SQL入门篇（概述）](https://www.liaoxuefeng.com/wiki/1177760294764384)

基础篇——1.[语法手册（过一遍）](http://www.xuesql.cn/static/金老师手册.html)		 [自学SQL网lesson1-12](http://www.xuesql.cn/)		 [50题基础刷题](https://zhuanlan.zhihu.com/p/53302593)

理论篇——[廖雪峰网站SQL关系模型](https://www.liaoxuefeng.com/wiki/1177760294764384/1218728991649984)、查询数据、修改数据	 [MYSQL基础学习](https://zhuanlan.zhihu.com/p/53302593)

实战篇——[1.SQL、MYSQL环境搭建](https://zhuanlan.zhihu.com/p/37152572)	，[Navicat可视化工具](https://zhuanlan.zhihu.com/p/37155150)		 [图解SQL面试50题实战刷题（MYSQL和Navicat基础操作）](https://zhuanlan.zhihu.com/p/38354000)

 

 

操作类型：

DDL：定义数据（创建删除修改表）

DML：日常操作（添加删除更新数据）

DQL：查询数据

 

表table行rows 列columns

数据类型：整型、字符型、字符串、日期等、（NULL表示数据不存在）

 

 

每行数据为一条记录，一条记录有多个字段

 

***\*主键和外键：\******一对一、一对多、多对一、多对多的关系**

 

主键：关系表记录的唯一标识

联合主键：两个或更多的字段都设置为主键（允许有一列重复）

外键：通过class_id把数据与另一张表关联起来

***\**ALTER TABLE\**\***  **students**

***\**ADD CONSTRAINT\**\***  **fk_class_id**

***\**FOREIGN KEY\**\***  **(class_id)**

***\**REFERENCES\**\*** **classes (id);**

***\**ALTER TABLE\**\*** **students**

***\**DROP FOREIGN KEY\**\*** **fk_class_id;**

 

**注意：Windows不区分大小写，Linux/Unix区分大小写**

**任意两条记录不能重复**；不使用任何业务相关的字段作为主键；外键约束会降低数据库的性能

 

 

**创建索引**

***\**ALTER TABLE\**\*** **students**

***\**ADD INDEX\**\*** **idx_score (score)**



**查询**queries（字段选择）：

 

SELECT语法：

SELECT column（列名）, another_column, …

FROM mytable（表名）;

条件查询constraints

from

where对原始表筛选

having对分层汇总后的结果做筛选

连接语句：and和 or或

条件子句where

比较运算符：

=等于 >=大于等于 <=小于等于 !=不等于 >大于 <小于

确定（连续）范围：between ...and...

字符匹配（模糊查询）：

like %任意个字符 _一个字符

判断是否为空 is null

多个查询条件 and or

分组查询 group by / having

结果呈现 order by（排序）/ limit（限制条数）

 

连接语句 left/right/inner join

执行优先级

 

Hive单表查询完整结构：

SELECT<目标列名序列,函数>

FROM<表名>

WHERE<分区条件与检索条件>

[GROUP BY<分组依据列>]

[ORDER BY<排序依据列>]

[LIMIT N<只看结果的前N条>]

 

聚合函数：

count（id）统计表中id个数

count（distinct id）统计表中id个数（去重）

max（id）最大值min（id）最小值

sum（id）求和avg（id）平均值

 

count+distinct+if实现统计

sum+if实现分组统计（这里sum可以替换为其他聚合函数）

case when大量变形操作

 





#### MySQL

**1、安装MYSQL**

**2、连接MYSQL数据库**

**3、用户管理相关的命令**

**4、** **创建结构**：

​	A.**数据库**

show databases;  # 用来查看所有的数据库

create database <dbname> charset=utf8;  # 创建一个新的数据库，并指定编码格式为 utf8

use <dbname>  # 切换数据库

drop database <dbname>

alter database <dbname> charset=utf8;  # 修改数据库的编码方式

​	B.***\*表格\****

create table <tablename>(

id int primary key auto_increment,  # int类型的字段id，主键自增

name varchar(128),   # 至少要写字段的名字以及类型，

tel varchar(32) unique,  # 字段tel,有唯一约束

)

 

desc <tablename>;

describe <tablename>; #查看表结构

 

alter table <tablename> drop <字段名>;

show create table <talbename>; # 查看建表语句

drop table <tablename>  # 删除表格

***\*修改表格属性\*******\*:\****

alter table <tablename> rename <namename>  # 修改表格的名字

alter table <tablename> rename to <newdbname.newtablename># 将一个表移动到一个新的数据库里

alter table <tablename> add <字段名> <类型> [属性]  # 新增一个字段

alter table <tablename> add <字段名> <类型> [属性] first

alter table <tablename> add <字段名> <类型> [属性]  after <字段名>

alter table <tablename> change <字段名> <新名字> <属性> # 用来修改字段的名字和属性

alter table <tablename> modify <字段名> <属性>  # 用来修改字段的属性

 

 

简介：

MYSQL关系型数据库（本质上是软件）：多表关联
使用C/C++编写，平台可移植（支持Linux、Windows、MacOS、Solaris等）；支持多种编程语言：C/C++/Python/JAVA/Perl/PHP/Ruby；支持多线程；优化了SQL查询算法；

 

基于Linux系统下：

Sudo apt-get install mysql-server 安装数据库

 

MySQL查询：

条件/排序/聚合函数/分组/分页/连接查询/自关联/子查询

MySQL编码和数据类型：
字符集（数据存储和传输）：ASCII / LATIN1 / GB2312 / GBK / UTF-8 / UTF8MB4

查看mysql系统支持的字符集： mysql> show variables like 'character_%'; 

校对集（字符比较）：

 

数据类型：

整型：TINYINT / SMALLINT / MEDIUMINT / INT/INTEGER / BIGINT

浮点型：FLOAT / DOUBLE  定点数：DEC(M,D) / DECIMAL(M,D) 位类型：BIT(M)

字符串类型：

枚举类型enum：多选一（前端的单选框）**限制了可选值以节省空间提高了运行效率**

集合set：最多64个成员，类似于复选框

时间类型：DATE / DATATIME / TIMESTAMP / TIME / TEAR / TIMESTAMP
布尔型：bool型1 / 0
列的属性：null / not null 插入的值是否为空
SQL注释：单行 --  多行 /* */  MYSQL独有单行注释  #

 

**算术运算符**：+  -  *  /  %

**比较运算符**：= 等于（常规比较）、 <>或!= 不等于 、 <=> NULL安全的等于 、 <小于 、 <=小于等于 、 

\> 大于、 >=大于等于 、 BETWEEN存在于指定范围（范围比较） 、 IN存在于指定集合 、

 IS NULL 为NULL 、 IS NOT NULL 不为NULL 、 LIKE 通配符匹配（模糊比较） 、 REGEXP或RLIKE 正则表达式匹配

**逻辑运算符**：非：NOT或！  与：AND或&&  或： OR或||  异或： XOR

 

 

 

 

 

## Python插件：PyMySQL连接数据库

 

列——字段、行——记录、唯一标识——主键
 


### 常用操作

- show dbs

- show collections

- use dushu  打开或创建dushu数据库

- db.createCollection('集合名')

- db.集合名.drop()

- db.dropDatabase()

- db.集合名.insert()|save()

- db.集合名.update(条件{}, 更新的数据{ $set: { }}, upsert, multi)

  - upsert 为真时，当条件没有匹配数据时，将更新的数据插入到集合中, 反之为假时，则什么也不做。
  - multi, 为真时， 当条件匹配多条数据时，将会更新所有的数据，反之，只更新每一条数据。

- db.集合名.remove(条件 { })

  删除user集合中文档的name属性包含`成`所有的记录

  ```js
  db.user.remove({name: {$regex: '成'}})
  ```

- db.集合名.find(条件{ }， 保留属性{name: 1}).pretty()

  - 逻辑关系
    - $or
    - $ne
    - $lt 
    - $gt
    - $lte
    - $gte
  - 正则表示
    - $regex


##### mql_toolkits.mplot3d

```python
from mql_tookits.mplot3d import Axes3d
```
 
 ### Linux

#### 系统安装

A：虚拟机安装Linux Ubuntu开发系统（未采纳）

B：电脑双系统https://www.cnblogs.com/masbay/p/11627727.html

基于Windows10安装Linux Ubuntu 双系统

基本信息：DELL Ispiron 5488 单硬盘（C盘 D盘）WIndows 系统UEFI格式

工具：

UItralSo 软牒通 软件(用软牒通向U盘写入镜像文件)

U盘 （>2G)

Ubuntu镜像文件 ：Ubuntu-20.04.2.0-desktop-cmd64.iso

Windows(NIFS)分区：压缩卷 D	80G用来装新系统

*分区是因为两个系统文件存储格式不同，防止混乱* 

```
BIOS boot manager(F12快捷键)
	--Security boot Secure		[Disabled]
	--Intel RST					[Disabled]
System Configuration	--SATA Operation
```

——双系统切换：

Windows10 	RAID ON	boot manager

Ubuntu20.4	ACHI		   ubuntu



Set Individual OS(Ubuntu):
Language(语言)/regon（地区）/keyboard(键盘)/Account(账户)/Password(密码)

Ubuntu 分区（手动分区）：

​	efi		200MB	逻辑分区/起始位置	安装启动项

​	swap	8G		   逻辑分区/起始位置	交换空间

​	/			40G		主分区/起始位置		ext4日志文件系统（根目录）

​	/home  剩余空间 逻辑分区/起始位置   ext4日志文件系统（存储）


#### Shell指令

1.程序安装：

基于Debian(Ubuntu)的deb或源文件（rpm基于Red hat)

deb包安装 dpkg -i xxx		卸载 dpkg -r xxx 

2.常用程序

Ubuntu Software

PyCharm Professional Edition/Visual Studio Code/Vim

Typora /FireFox/Google Chrom



3.Shell 常用指令

  ...


