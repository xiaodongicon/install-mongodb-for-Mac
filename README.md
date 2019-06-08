# MAC系统 安装 Mongodb 步骤详解

### 一、brew 安装

1. brew 官网 [https://brew.sh/](https://brew.sh/) 找到安装命令
  	
![brew安装命令](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WechatIMG283.png)

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
	
2. 复制到命令行中，回车键后会自动安装

3. 安装完成后输入 `brew -v` 显示版本号证明安装成功

![安装成功](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-122642%402x.png)

### 二、brew 基本使用

1. 更新 brew

>`brew upgrade` 更新 brew 及 使用 brew 安装的所有软件

2. brew 安装软件

>`brew install [soft_name]`  比如：安装 node `brew install node`

3. 查看brew 安装的文件路径

>`brew --cache`

4. 查看 brew 安装的软件列表

>`brew list`

5. brew 卸载软件

>`brew uninstall [soft_name]` 比如：卸载 git `brew unstall git`

### 三、安装 mongodb

1. 使用 brew 安装 mongodb

>`brew install mongodb`

![brew 安装 mongodb](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-124720%402x.png)

2. 查看 mongodb 安装目录

>`which mongod` 或者 `where mongod`

![mongodb安装目录](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-174930%402x.png)

3. 手动添加数据库数据目录

>进入系统根目录，运行 `sudo mkdir -p /data/db` 

![数据库数据目录](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-175358%402x.png)

4. 输入命令 `mongod` 启动 Mongodb 数据库

> 这时会有错误提示，是刚创建的数据目录没有读写权限导致

![未授权的数据目录](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-175935%402x.png)

5. 添加可读写权限 ``sudo chown \`id -u` /data/db`` 并运行 `mongod`

> 提示 ``waiting for connections on port 27017`` 表示数据库启动成功，等待被链接

![启动成功](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-180518%402x.png)

6. 推荐一个 MongoDB 可视化工具 [Robo 3T](https://download-test.robomongo.org/mac/robo3t-1.3.1-darwin-x86_64-7419c40.dmg) 
安装后启动Robo3t, 点击左上角:computer:图标， 按照默认设置创建一个链接 

![Robo3t 创建链接](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-183432%402x.png)

7. 新开个 shell 窗口, 输入 `mongo` 进入数据库服务

![进入数据库服务](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-184604%402x.png)

8. 查看数据库 `show dbs`
默认有这几个数据库

![数据库列表](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-184854%402x.png)

9. 使用/新建 数据库 ` use db_fanxd ` 数据库存在就是使用，不存在就是创建

![使用/新建数据](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-190127%402x.png)

10. 查看当前所在数据库 `db`

![查看当前数据库](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-190304%402x.png)

11. 添加表数据 `db.db_fanxd.insert({'name':'小东','age':'27'})`

![添加表数据](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-190455%402x.png)

12. 查看表数据 `db.db_fanxd.find()`

![查看表数据](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-190740%402x.png)

13. 查看 Robo3t 刚才创建的数据库

![查看 Robo3t 数据库](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-191348%402x.png)


14. 关闭数据库时 需要进入 `admin` 数据库才能关闭

![关闭数据库](https://github.com/xiaodongicon/install-mongodb-for-Mac/blob/master/WX20190608-190938%402x.png)


---
ps: 以上内容是整合 google 出来的内容，有哪里不对请您提个issue :smile:

