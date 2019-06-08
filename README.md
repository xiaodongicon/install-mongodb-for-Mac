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




