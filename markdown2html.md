<link href="http://kevinburke.bitbucket.org/markdowncss/markdown.css" rel="stylesheet">


# 使用現有的html格式
可以直接在文本文檔前插入：

    <link href="http://kevinburke.bitbucket.org/markdowncss/markdown.css" rel="stylesheet">

或者

    <link href="/path/to/markdown.css" rel="stylesheet"></link>
    
# bootstrap
是近年來一個比較好的web前端框架，使用模塊 **markdown2bootstrap** 可以將 **markdown** 文件轉換為 **bootstrap** 風格的 **html** 文件。

## 安裝nodejs及npm
在 **MAC OS X** 下：

    brew install npm
    brew install nodejs
    
不過似乎安裝 **npm** 的時候就會順便把 **nodejs** 也裝了。

在 **DEBIAN** 下：

    sudo apt-get install npm
    sudo apt-get install nodejs

但是， **apt-get** 找不到。

然後需要做一个链接：

    sudo ln -s /usr/bin/nodejs /usr/bin/node

不然可能会遇到如下 **ERROR**：

    /usr/bin/env: node: No such file or directory
    
安装markdown2bootstrap到当前目录下

    npm install markdown2bootstrap
    
将markdown转换为html命令

    ~/node_modules/.bin/markdown2bootstrap filename.md
    
如果不想产生数字列表用-n参数

    ~/node_modules/.bin/markdown2bootstrap -n filename.md
    
最后一步将包拷到你的网站根目录下，例如 **~/www**

    cp -r node_modules/markdown2bootstrap/bootstrap ~/www
    
暫時就是這樣，，，    