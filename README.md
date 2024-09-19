<style>

    .success {
        padding:5px;
        display:inline;
        color:#1B5E20;
        background-color:#C8E6C9;
    }
    .warning {
        padding:5px;
        display:inline;
        color:#E65100;
        background-color:#FFE0B2;
        width:100%;
    }
    .danger {
        padding:5px;
        display:inline;
        color:#B71C1C;
        background-color:#FFCDD2;
    }
    .info {
        padding:5px;
        display:inline;
        color:#006064;
        background-color:#B2EBF2;
    }
    .doubt {
        padding:5px;
        display:inline;
        color:#AAA;
        background-color:#DDDDDD;
    }
    .asso {
        padding:5px;
        display:inline;
        color:#555;
        background-color:#FFCC00;        
    }
    
    .alert {
        display:inline-block;
        width:100%;
        padding:5px;
        line-height:30px;
        margin-top:10px;
    }
</style>

## MySQL安装
- 安装界面 select products and features 界面，Available Products中选择 MySQL Server8.0.20-x64
- High Available（高可用性）界面，选择默认的Standalone MySQL Server/Classic MySQL Replication
- Type and NetWork界面，Config Type配置类型的三个不同设置
    - Development Machine（开发机器）， 适用于个人开发者使用的电脑或者测试环境，配置MySQL以占用较少的系统资源，不那么侧重性能。
    - Server Machine（服务器机器），一台专门用作数据库服务器的机器，配置MySQL以利用更多的系统资源，优化性能，比如分配更多的内存给数据库缓存。
    - Dedicated MySQL Server Machine（专用MySQL服务器机器），最激进的配置选项，专为那些仅运行MySQL且对数据库性能有极致要求的环境设计。最大化MySQL对系统资源的使用，包括内存、CPU和I/O，以达到最佳的数据库性能。
- 添加环境变量，系统变量，path中将MySQL安装目录中bin目录的路径添加。添加后在cmd命令行中输入`mysql -u root -p`命令并执行，验证是否添加成功

- ubuntu 安装mysql https://blog.csdn.net/weixin_45626288/article/details/133220238
    - 初始化MySQL服务，获取新的随机生成的root密码 `mysqld --initialize --console` 需要相关文件及目录权限，命令执行后在/var/log/mysql目录下的log日志中查找新生成的root密码
    - 编辑配置文件 `sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf` 修改 bind-address      = 0.0.0.0       启用port  = 3306 保存退出

    `sudo systemctl start mysql`
    `sudo systemctl status mysql`
    `sudo systemctl restart mysql`
    `sudo systemctl stop mysql`
    `sudo systemctl enable mysql` 随系统启动
    `sudo systemctl disable mysql` 取消随系统启动
## Navicat可视化工具安装


## CRUD

### create

### read

```sql
desc select * from tableName --查询语句执行详细过程
```

### update
```sql
insert into tableName(colum1,colum2,colum3) values ('001','002','005'); --指定列插入
insert into tableName values('1','12','15','26'); --插入所有列
```

### delete

## 查询语句

## 索引

```sql
alter table tableName add index indexName(columName) --增加默认索引
alter table tableName add index unique indexName(columName) --增加唯一索引，主键就是唯一索引
alter table tableName drop index indexName
show index from tableName \G
```


## 事务transaction

```sql
begin 开启事务
rollback 回滚事务
commit  提交事务
```


## 锁lock
锁分为表级别锁，行级别锁。指在执行某个读写操作时，将表锁定，防止其他进程修改表，或读取表。
- 读锁状态，可以并发读取，但不能写入，直到释放锁。
- 写锁状态，只有锁表的用户可以读写操作，其他用户都不行。（抢购唯一商品场景）
```sql
lock table tableName read -- 读取锁，只能读，解锁之前无法对标进行写操作
unlock tables -- 解除锁

lock table tableName write --写锁，只锁表用户读写，解锁之前其他用户无法读写操作。
unlock tables -- 解除锁
```














---
<span class="success">
    test asdfds adasf dfas 
</span>

<span class="alert danger">
    test asdfds adasf dfas 
</span>

<span class="alert info">
    test asdfds adasf dfas 
</span>


<span class="alert success">
    test asdfds adasf dfas 
</span>

<div class="alert warning">python不区分单精度和双精度浮点
数，默认双精度，int也不细分short,long整型)
</div>

<div class="alert asso">python不区分单精度和双精度浮点
数，默认双精度，int也不细分short,long整型)
</div>

<div class="alert doubt">python不区分单精度和双精度浮点
数，默认双精度，int也不细分short,long整型)
</div>