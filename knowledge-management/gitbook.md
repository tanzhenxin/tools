# GitBook 使用简单介绍

## 安装

GitBook 是基于Nodejs环境的，安装是通过**NPM**工具：

```
$ npm install gitbook-cli -g
```

`gitbook-cli`是GitBook的命令行工具集，包含一些简单的命令用来制作GitBook。

## 制作GitBook

创建一本新的Gitbook：

```
$ gitbook init
```

运行这个命令会在当前文件夹下面创建两个文件，`README.md` 和 `SUMMARY.md`。
其中 `README.md` 是这本GitBook的介绍页，`SUMMARY.md`是目录页面。

通过目录和文章生成静态网站：

```
$ gitbook build
```

生成静态网站并可以在本地预览：

```
$ gitbook serve
```

## 目录组织

一个基本的Gitbook组织形式看起来是这样的：

```
.
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

其中 `SUMMARY.md` 是目录文件，负责组织其它文章的位置，一个基本的**SUMMARY**大概是这样的：

```
# Summary

* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

上面的例子中有两个章节，对应独立的目录结构，每个章节下面有所对应的文章列表。

## 连接Github

先在Github上创建仓库，并将本地的GitBook推送到Github上，过程就不详述了。

然后到 [GitBook] 上建立账号并连接到Github账号，点击创建Book，在弹出的对话框里选择GITHUB和刚才的Github仓库地址。
GitBook就创建好了并和Github绑定成功，每次推送update到Github仓库，GitBook都会自动更新。

[GitBook]: https://www.gitbook.com
