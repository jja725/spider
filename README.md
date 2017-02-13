##留学论坛爬虫

******

这个爬虫，我主要是爬去一个留学论坛，这次爬取的是北美的offer结果版面，他的页面是这样的：

![pic](https://github.com/salamer/gter_bbs_spider/blob/master/6B2CE164-4B3D-49E3-91E0-3AEFA200E674.png?raw=true)

爬虫使用了`gevent`异步进行，使用mongodb做最后的数据库存储，然后将内容导出成csv文件



###usage

******
安装mongodb：

MacOS:

    brew install mongodb

Linux:

Ubuntu/debian:

    sudo apt-get install mongodb

CentOS:

    sudo yum install mongodb

安装 `python`包依赖：

    pip install -r requirements.txt

然后你去`config.py`，修改你的开始页面的url和页码，非常简单的配置，还有配置你的mongodb的collection名称

然后执行：

    python engine.py

将Mongodb内的数据导出成CSV:

    python dbToCsv.py



