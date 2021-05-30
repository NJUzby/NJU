# MySQL教程

## MySQL创建数据库

CREATE DATABASE NJU;//创建了一个名为NJU的数据库

## MySQL删除数据库

drop database NJU;//删除名为NJU的数据库

## MySQL选择数据库

use NJU;//选择了名为NJU的数据库，接下来的所有操作都在数据库NJU中进行

## MySQL数据类型

### 数值类型

严格数据类型：INTEGER（INT），SMALLINT，DECIMAL（DEC），NUMERIC

近似数据类型：FLOAT，REAL，DOUBLE PRECISION

![](asset\数据类型.png)

### 日期和时间类型

DATETIME，DATE，TIMESTAMP，TIME，YEAR

![](asset\日期和时间类型.png)

### 字符串类型

CHAR、VARCHAR、BINARY、VARBINARY、BLOB、TEXT、ENUM和SET

![](asset\字符串类型.png)

## MySQL创建数据表

创建数据表需要以下信息

- 表名称
- 表字段名
- 定义每个表字段

### 语法

`CREATE TABLE table_name(column_name column_type);`

参数中的`column_name column_type`可以有多组，但必须是成组的。可选参数`primary key(column_name)`,`column_type`后可选NOT NULL，AUTO_INCREMENT(自增，一般用于逐渐，数值会在前一个的基础上自动加一)

在CREATE子句后面还可以指定存储引擎`ENGINE=`和设置编码`CHARSET=`



## MySQL删除数据表

`drop TABLE table_name;`

## MySQL插入数据

```MySQL
INSERT INTO table_name(field1,field2,...fieldN)
VALUES
(value1,value2,...,valueN);
```

## MySQL查询数据

MySQL 数据库使用SQL SELECT语句来查询数据

```MySQL
SELECT column_name1,column_name2
FROM table_name
WHERE cause
```

## MySQL WHERE子句

WHERE子句用来限制筛选的条件，可以使用AND，OR等指定一个或多个条件。WHERE子句也可用于UPDATE或者DELETE语句，类似于if。

![](asset\WHERE操作符.png)



where子句默认是不区分大小写的，可以通过加入BINARY关键字来开启区分大小写

## MySQL UPDATE更新

```MySQL
UPDATE table_name SET field1=new-value1, field2=new-value2
[WHERE Clause]
```

可以同时更新一个或者多个字段，用WHERE子句限制修改的行

## MySQL DELETE语句

```MySQL
DELETE FROM table_name [WHERE Clause]
```

这是删除行的语句

## MySQL LIKE子句

可以获取数据库中满足某个字符串匹配条件的行

用%表示任意字符（可以是多个）

用_表示任意一个字符

比如LIKE D% 表示查找以D开头的字符串

## MySQL UNION子句

MySQL UNION 操作符用于连接两个以上的 SELECT 语句的结果组合到一个结果集合中。多个 SELECT 语句会删除重复的数据。

但如果是UNION ALL，那么就不会去除重复元素

## MySQL排序

如果我们需要对读取的数据进行排序，我们就可以使用 MySQL 的 **ORDER BY** 子句来设定你想按哪个字段哪种方式来进行排序，再返回搜索结果

```MySQL
SELECT field1, field2,...fieldN FROM table_name1, table_name2...
ORDER BY field1 [ASC [DESC][默认 ASC]], [field2...] [ASC [DESC][默认 ASC]]
```

ASC 表示升序，desc表示降序。优先按前一个排，在排好的基础上对于每一项相同的按照后者排。

## MySQL GROUP BY语句

```MySQL
SELECT column_name, function(column_name)
FROM table_name
WHERE column_name operator value
GROUP BY column_name;
```

可以做到分组（当然分的组你是看不到的），并对分组后的数据进行统计。

## MySQL连接的使用

### INNER JOIN

和WHERE功能差不多

### LEFT JOIN



