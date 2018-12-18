# word2vec
##copy code from 我爱自然语言处理

###原文链接 http://www.52nlp.cn/中英文维基百科语料上的word2vec实验
###下载数据
nohup wget -o enwiki-latest-pages-articles.xml.bz2 https://dumps.wikimedia.org/enwiki/latest/enwiki-latest-pages-articles.xml.bz2 &


## 其他
###中文语料
https://dumps.wikimedia.org/zhwiki/latest/zhwiki-latest-pages-articles.xml.bz2
###繁体转简体
https://github.com/BYVoid/OpenCC
opencc -i wiki.zh.text -o wiki.zh.text.jian -c zht2zhs.ini
###一种分词方式
mecab -d ../data/ -O wakati wiki.zh.text.jian -o wiki.zh.text.jian.seg -b 10000000
###一种解决编码问题的方式
iconv -c -t UTF-8 < wiki.zh.text.jian.seg > wiki.zh.text.jian.seg.utf-8


#等于号表示上一行为大标题(一级标题)， 参考资料 https://www.cnblogs.com/shiy/p/6526868.html
=======
#中划线为中标题(二级标题)
-------------
#一级标题
##二级标题
###三级标题
####四级标题
#####五级标题
######六级标题

插入圆点符号：编辑的时候使用的是星号 *，星号后面要有一个空格，否则为普通星号

* 列表一
* 列表二
* 列表三


二级圆点、三级圆点：多加一个Tab，即第二行一个Tab，第三行两个Tab

* 列表一
    * 列表二
        *列表三
        

缩进：

>缩进一
>>缩进二
>>>缩进三
>>>>缩进四
>>>>>缩进五


插入链接

[百度](http://baidu.com)


插入网络图片：![](网络图片链接地址)，即叹号!+方括号[]+括号()，如果不加叹号!就会变成普通文本，方括号里可以加入一些 标识性的信息

![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")



插入GITHub仓库里的图片：![](图片链接地址)，即叹号!+方括号[]+括号()，URL写法：http://github.com/自己的用户名/项目名/raw/分支名/存放图片的文件夹/文件夹里的图片名字

给图片加上超链接：即点击一个图片进入指定网页，方括号里写自己起的标识名称，上下两行标识要一致。

[![baidu]](http://baidu.com)  
[baidu]:http://www.baidu.com/img/bdlogo.gif "百度Logo" 


插入代码片段：在代码上下行用```标记，注意`符号是tab键上面那个，要实现语法高亮，则在```后面加上编程语言的名称

```Java
public static void main(String[] args){}
```

```javascript
document.getElementById("ts").innerHTML="Hello"
```




换行：使用标签<br>

单行文本：前面使用两个Tab

多行文本:每行行首加两个Tab

部分文字高亮：使用``包围，这个符号不是单引号，而是Tab上方，数字1左边那个按键的符号

文字超链接格式：[要显示的文字](链接的地址"鼠标悬停显示")，在URL之后用双引号括起来一个字符串，即鼠标悬停显示的文本，可不写

