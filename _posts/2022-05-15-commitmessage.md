**规范**

程序员是一个千变万化但是又不离其中的职业，能够实现各种各样的功能，实现的方法也是各种各样，而最佳实践又是很多程序员比较认可和遵守的一些规则，其中会有：

-   html-css规范：https://github.com/doyoe/html...
-   JavaScript书写习惯：https://github.com/adamlu/jav...

规范可能并不会带来直接的利好，但是随着工程的扩大，这些良好的习惯可能会带来很好的优势，不然eslint也不会这么受欢迎，

本文讲的并不是JavaScript-css-html的规范，而是程序员比较常用地git操作，先安利一个命令端的工具，

1.  [https://github.com/robbyrusse...](https://github.com/robbyrussell/oh-my-zsh) 一个命令端的利器  
    这里也是讲git commit的一种方式，参考了AngularJS项目的推荐git规范]，

**git** [commit](https://so.csdn.net/so/search?q=commit&spm=1001.2101.3001.7020)**补充**

先看看[angular](https://so.csdn.net/so/search?q=angular&spm=1001.2101.3001.7020)的格式

1.  
2.  Commit Message 格式
3.  
4.  \<type\>(\<scope\>): \<subject\>
5.  \<空行\>
6.  \<body\>
7.  \<空行\>
8.  \<footer\>

可以看出分为三个部分，头部，主体，底部；

1.  首先是头部，\<type\>(\<scope\>): \<subject\>  
    包括了三个节点：
    -   type 类型，修改的类型级别
        -   feat：新功能（feature）
        -   fix：修补bug
        -   docs：文档（documentation）
        -   style： 格式（不影响代码运行的变动）
        -   refactor：重构（即不是新增功能，也不是修改bug的代码变动）
        -   test：增加测试
        -   chore：构建过程或辅助工具的变动
    -   scope 修改范围  
        主要是这次修改涉及到的部分，最好简单的概括
    -   subject 修改的副标题  
        主要是具体修改的加点
2.  body，修改的主体标注
3.  footer里的主要放置不兼容变更和Issue关闭的信息，  
    这些东西由于我们书写代码本身就会经常性的提交，所以如果每次都这样书写的确是挺烦人的，所以我目前建议自己采用相同的但是更加简单的方式来完成，

**简单的git commit规范**

简单的git commit的格式：

1.  git commit -m "fix:修改了去除定位偏移的bug"
2.  //git commit -m "fix+style:修改了去除定位偏移的bug+背景样式修改"
