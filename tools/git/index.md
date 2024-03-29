# 学习使用Git
## `Git`简介
Git是什么？

Git是目前世界上最先进的分布式版本控制系统（没有之一）。

Git有什么特点？简单来说就是：高端大气上档次！

那什么是版本控制系统？

如果你用Microsoft Word写过长篇大论，那你一定有这样的经历：

想删除一个段落，又怕将来想恢复找不回来怎么办？有办法，先把当前文件“另存为……”一个新的Word文件，再接着改，改到一定程度，再“另存为……”一个新文件，这样一直改下去，最后你的Word文档变成了这样：

![](https://cdn.jsdelivr.net/gh/coder-th/static/202110132349136.png)

过了一周，你想找回被删除的文字，但是已经记不清删除前保存在哪个文件里了，只好一个一个文件去找，真麻烦。

看着一堆乱七八糟的文件，想保留最新的一个，然后把其他的删掉，又怕哪天会用上，还不敢删，真郁闷。

更要命的是，有些部分需要你的财务同事帮助填写，于是你把文件Copy到U盘里给她（也可能通过Email发送一份给她），然后，你继续修改Word文件。一天后，同事再把Word文件传给你，此时，你必须想想，发给她之后到你收到她的文件期间，你作了哪些改动，得把你的改动和她的部分合并，真困难。

于是你想，如果有一个软件，不但能自动帮我记录每次文件的改动，还可以让同事协作编辑，这样就不用自己管理一堆类似的文件了，也不需要把文件传来传去。如果想查看某次改动，只需要在软件里瞄一眼就可以，岂不是很方便？

这个软件用起来就应该像这个样子，能记录每次文件的改动：

| 版本 | 文件名      | 用户 | 说明                  | 日期       |
| ---- | ----------- | ---- | --------------------- | ---------- |
| 1    | service.doc | 张三 | 删除了软件服务条款5   | 7/12 10:38 |
| 2    | New.doc     | 李四 | 增加了License人数限制 | 7/12 18:09 |


这样，你就结束了手动管理多个“版本”的史前时代，进入到版本控制的20世纪。


## 安装`Git`
安装`git`是一个非常简单的操作，我们可以到`git`官网下载好对应操作系统的软件，然后解压后一直点击`next`下一步就可以了，中间记得不要做其他的操作,全部默认就可以了。
::: tip 如何查看已经安装完成呢?
你可以打开电脑终端(`cmd`(window)/`zsh`(mac)),输入命令`git --version`
如果显示的是对应的版本，那么恭喜你，安装成功了。

:::
## 全局配置

- 用户名

  ```shell
  git config --global user.name ”coder-lean"
  ```

- 邮箱

  ```shell
  git config --global user.email ”13265317640@163.com"
  ```
## Git的仓库概念
![Git的仓库概念](https://cdn.jsdelivr.net/gh/coder-th/static/202110132334904.png)



- **`WorkSpace`**(工作区): 我们编写代码的区域
- **`Index/Storage`**(暂存区):  我们编写代码后,可以选择我们想要管理的对应文件存储到临时文件夹中。相关的命令请看下方
- **`Local Repository`**(本地仓库): 我们想要把确定好的文件提交到本地仓库中(`git`软件),**记得**注释信息一定要写喔
- **`Remote Repository`**(远程仓库): 远程代码仓库(你可以理解为上传到百度网盘).
  

### 工作区的命令

#### 新建项目

```shel
git init
```

#### 提交文件到暂存区

- **全部提交**

```shell
git add .
```

- **部分提交**

```shell
git add readme.md(某个文件夹所有的文件)   src/test.js(某个文件夹某个文件)  src/*(某个文件夹所有的文件)
```

### 暂存区的命令

> 提交到本地仓库

```shell
git commit -m "我是第一次提交"
```

### 本地仓库的命令



