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

但是， **apt-get** 找不到，暫時沒空處理。

然後需要做一個鏈接：

    sudo ln -s /usr/bin/nodejs /usr/bin/node

不然可能會遇到如下 **ERROR**：

    /usr/bin/env: node: No such file or directory
    
安裝markdown2bootstrap到當前目錄下

    npm install markdown2bootstrap
    
將markdown轉換為html命令

    ~/node_modules/.bin/markdown2bootstrap filename.md
    
如果不想產生數字列表用 **-n** 參數

    ~/node_modules/.bin/markdown2bootstrap -n filename.md
    
最後一步將包拷到你的網站根目錄下，例如 **~/www**

    cp -r node_modules/markdown2bootstrap/bootstrap ~/www
    
暫時就是這樣，，，    It worked for me.