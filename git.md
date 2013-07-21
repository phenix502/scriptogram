Title: Git 学习
Category: 编程学习
Tags: git
date: 2013-07-18

这是阅读 [pro git中文版](http://git-scm.com/book/zh/Git-%E5%9F%BA%E7%A1%80-%E8%AE%B0%E5%BD%95%E6%AF%8F%E6%AC%A1%E6%9B%B4%E6%96%B0%E5%88%B0%E4%BB%93%E5%BA%93)的阅读笔记.

首先看git文件管理的状态图
![状态图](/image/file_status_lifecycle.png)

##  取得项目
对需要用__git__进行管理的项目, 进入项目所在的目录, 执行:

     
    git init
在项目的目录中,会多出一个.git文件.

对__github__仓库上开源项目, copy下来进行学习, 选择需要保存项目的文件夹,然后在终端输入:

     
    git clone https://github.com/phenix502/phenix502.github.com.git
会发现多出了一个phenix502.github.com的文件夹,如果想自己定义项目名称可以这样:

     
    https://github.com/phenix502/phenix502.github.com.git blog
这样就得到了blog为名称的项目

##  跟踪管理文件

     
    git add filename

对文件进行跟踪管理.

##  得知当前项目状态

     
    git status

信息有以下情况:

* Changes to be commited 文件修改且已暂存(snapshot)
* Changes not staged for commit 文件修改了但没提交管理

## 忽略某些文件
在__.gitignore__文件中输入要忽略的文件.举例如下

    # 此为注释 – 将被 Git 忽略
    # 忽略所有 .a 结尾的文件
    *.a
    # 但 lib.a 除外
    !lib.a
    # 仅仅忽略项目根目录下的 TODO 文件，不包括 subdir/TODO
    /TODO
    # 忽略 build/ 目录下的所有文件
    build/
    # 会忽略 doc/notes.txt 但不包括 doc/server/arch.txt
    doc/*.txt

## 查看已暂存和未暂存的更新 

这是高级用法.以前不是很懂.如果你修改了一个文件且尚未__暂存__,你想看它和已暂存的版本有什么不同.

     
    git diff

如果想看已暂存的文件和上次提交的文件有什么不同

     
    git diff --staged
 
## 提交更新

     
    git commit -m "something about this change"

## 删除文件

把文件从已经跟踪管理的文件中去掉.

     
    git rm filename
特别地,要删除当前目录下所有文件

     
    git rm *

## 重命名

对跟踪管理的文件重新命名

     
    git mv old_file new_file

## 查看log文件

     
    git log




