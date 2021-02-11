# GIt学习



## 学习Git的原因

多人开发需要使用版本控制

1. 本地版本控制：RCS

2. 集中版本控制：SVN,CVS,VSS (所有版本数据保存在服务器上，协同开发者从服务器上同步更新或上传自己的修改，必须联网)

3. 分布式版本控制：Git （每个人拥有全部的代码，不会因为服务器损坏或者网络问题造成不能工作的情况，每个人都有备份，数据不易丢失，且可以互相看到对方的修改）

    ***Git是目前世界上最先进的分布式版本控制系统***

   

## 启动Git

**Git Bash** ：Unix与Linux风格的命令行，推荐！

**Git CMD**：Windows风格命令行

**Git GUI** ：图形界面Git，不推荐初学者



## Git基本原理

GIt 有三个工作区域：工作目录,   暂存区，资源库

Git工作流程：1.工作目录中添加文件 2.将文件放入暂存区 3.将暂存区域的文件提交到本地 4.提交到git仓库

​									思路：工作目录——暂存区——本地——git仓库



## Git文件操作

Git重要的三个上交命令： git add files  、 git commit 、 git push  

​				 三个反向上交：git checkout 、 git reset、 git pull

在空的文件中操作：

1. Git初始化，设置为Git目录： git init 
2. Git克隆： git clone URL    克隆网上的项目



git add . ：上传当前文件夹全部到暂存区

git commit  上传到本地  +-m “提交暂存区的信息”



***上传需要忽略某些文件的命令:***

在主目录下建立‘“.gitignore”文件写入忽略的代码：

*.文件后缀  忽略此类文件后缀的文件

.........



## IDEA的Git操作

先留空，暂时不学习





## Git分支

- master项目是主分支

- dev是用于开发的分支

- 其他是不同版本的分支

  

**master主分支需要非常稳定，一般开发不允许到master分支上，一般需要在新建的dev开发分支上工作，等到能够稳定发布后再合并到master。**



Git分支相关命令：

git branch：列出所有分支

git branch  -r ：列出远程分支

git branch  XX:创建一个XX分支

git checkout -b XX :创建一个XX分支，并切换过去

git merge XX：合并指定分支到当前分支

git branch -d XX:删除XX分支

#删除远程分支：

git push origin --delete XX：删除XX分支

git branch -dr XX/路径：删除XX分支



## Git后续

Gittee上资源：

[Git大全](https://gitee.com/all-about-git)

[Git命令学习](https://oschina.gitee.io/learn-git-branching/)

