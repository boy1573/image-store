[toc]

## 数据库相关概念

### 数据库的好处

* 持久化数据到本地

*  可以实现结构化查询，方便管理

### 数据库的常见概念

* DB：数据库（database），保存一组有组织的数据的容器
* DBMS：数据库管理系统（Database Management System），又称为数据库软件（产品），用于管理DB中的数据
 * SQL：结构化查询语言（Structure Query Language），用于和DBMS通信的语言
    * 不是某个特定数据库供应商专有的语言，几乎所有DBMS都支持SQL

   * 简单易学
   * 虽简单实际上是一种强有力语言，灵活使用其语言元素，可进行非常复杂和高级的数据库操作。

### 数据库存储数据的特点

* 将数据放到表中，表再放到库中
* 一个数据库中可以有多个表，每个表都有一个的名字，用来标识自己。表名具有唯一性。
* 表具有一些特性，这些特性定义了数据在表中如何存储，类似java中 “类”的设计。
* 表由列组成，我们也称为字段。所有表都是由一个或多个列组成的，每一列类似java 中的”属性”
* 表中的数据是按行存储的，每一行类似于java中的“对象”。

### 常见的数据库管理系统

* mysql、oracle、db2（IBM，适合海量数据）、sqlserver（微软，只能Windows安装）



## MySQL介绍

### MySQL的背景

* 前身属于瑞典的一家公司，MySQL AB
* 08年被sun公司收购
* 09年sun被oracle收购

### MySQL的优点

* 开源、免费、成本低

* 性能高、移植性也好
* 体积小，便于安装

### DBMS分两类

* 基础共享文件系统（例如微软的Access）
* 基于客户机-服务器（C/S架构）（例如MySQL、Oracle、SQLServer）

### MySQL的安装

* 属于c/s架构的软件，一般来讲安装服务端
  * 企业版（收费）
  * 社区版（免费）

### MySQL服务的启动和停止

* 方式一：通过命令行
  * net start 服务名
  *  net stop 服务名 
* 方式二：计算机——右击——管理——服务

### MySQL服务的登录和退出

* 登录：mysql 【-h 主机名 -P 端口号】 -u 用户名 -p密码（注意-p和密码之间不能有空格，可先不输入密码，回车再输）	

* 退出：exit或ctrl+C

### MySQL的常见命令

* 查看当前所有的数据库：show databases;

* 打开指定的库：use 库名

* 查看当前库的所有表：show tables;

* 查看其它库的所有表：show tables from 库名;

* 创建表：create table 表名(列名 列类型,列名 列类型，。。。);

* 查看表结构：desc 表名;

* 查看服务器的版本

  * 方式一：登录到mysql服务端：select version();

  * 方式二：没有登录到mysql服务端：mysql --version或mysql --V

    

### MySQL的语法规范

* 不区分大小写,但建议关键字大写，表名、列名小写

* 每条命令最好用分号结尾(或\g结尾)

* 每条命令根据需要，可以进行缩进 或换行

* 注释

  * 单行注释：#注释文字

  * 单行注释：-- 注释文字

  * 多行注释：/* 注释文字  */
  
    

### SQL的语言分类

* DQL（Data Query Language）：数据查询语言
  		select 
* DML(Data Manipulate Language)：数据操作语言
  		insert 、update、delete
* DDL（Data Define Language）：数据定义语言
  		create、drop、alter
* TCL（Transaction Control Language）：事务控制语言
  		commit、rollback

