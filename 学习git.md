# 精通GIT

[TOC]

## 入门

版本控制分为：

* 本地版本控制（VCS）

~~~ plantuml
@startuml
rectangle "本地计算机"{
rectangle "版本数据库"{
[版本3]-down-[版本2]
[版本2]-down-[版本1]
}
[文件]-版本数据库
}

@enduml
~~~

* 集中式版本控制（CVCS）

~~~ plantuml
@startuml
rectangle "中央VCS服务器"{
rectangle "版本数据库"{
[版本3]-down-[版本2]
[版本2]-down-[版本1]
}
rectangle "计算机A"{
[文件1]<-left-版本数据库
}

rectangle "计算机B"{
[文件2]<-left-版本数据库
}

}

@enduml

~~~

* 分布式版本控制（DVCS）

~~~ plantuml
@startuml
rectangle "服务器计算机"{
    rectangle "版本数据库"{
[版本3]-[版本2]
[版本2]-[版本1]
    }
}
rectangle "计算机A"{
  rectangle "版本数据库a"{
  [版本3a]-[版本2a]
  [版本2a]-[版本1a]
  }
  [文件a]<-down-版本数据库a
}

rectangle "计算机B"{
  rectangle "版本数据库b"{
  [版本3b]-[版本2b]
  [版本2b]-[版本1b]
  }
  [文件b]<-down-版本数据库b
}

服务器计算机<->计算机A
服务器计算机<->计算机B
计算机B<->计算机A

@enduml
~~~

## git基础

* git 保存的是快照，而不是差异
* 几乎所有操作在本地进行
* git所有数据在存储前都进行校验与计算
* git 通常只增加数据
* 文件的三种状态，在git中，文件可以处于以下三种状态：
  * 已提交（commited），表示数据安全存入本地数据库中；
  * 已修改（modified），表示改动了文件，但未提交到数据库；
  * 已暂存（staged），表示对已修改文件的当前版本做出标识并将其加入下一次要提交的快照中。
* Git项目的区域：Git目录（仓库）、工作目录及暂存区

~~~ plantuml
@startuml
工作目录->暂存区:暂存修改
暂存区->Git目录:提交
Git目录->工作目录:检出项目
@enduml
~~~

* Git工作流程：
  1. 修改工作目录中文件；
  2. 暂存文件，将文件快照加入暂存区；
  3. 提交暂存区中文件，将文件的快照永久地保存在Git目录中。
* Git配置
  * /etc/gitconfig 包含系统中所有用户及其仓库的值，使用下面命令：

   ~~~ code
    git config --system
   ~~~  

  * \~/.gitconfig或~/.config/git/config 针对用户自己的，使用命令：

   ~~~ code
   git config --global
   ~~~

  * 当前仓库git目录中的config，针对单个仓库。

* 用户身份设置，使用--global参数，设置一次就行：

  ~~~ code
    git config --global user.name "ygitourname"
    git config --global user.email youremail
    git config --global core.editor "editor"
  ~~~

* 检查个人设置

 ~~~ code
  git config --list
  git config <key>
 ~~~

* 获得帮助

 ~~~ code
   git help <verb>
   git <verb> --help
 ~~~

## 获取Git仓库

建立Git项目方法主要有两种:

* 在现有目录中初始化Git仓库

~~~ code
  git init //进入目录执行
  git add * //跟踪需要的文件
  git commit -m 'init' //提交
~~~

* 克隆现有的仓库

~~~ code
  git clone [url]
  git clone [url] 新文件夹
~~~

## Git仓库中记录变更

工作目录下文件都是两种状态之一：已跟踪（tracked）或者未跟踪（untracked）。已跟踪文件是指上一次快照中包含的文件，这些文件分为未修改、修改或者已暂存三种状态；其他就称之为未跟踪文件。
文件状态生命周期：

~~~plantuml
@startuml
未跟踪<-未修改:移除文件
未修改->已修改:编辑文件
已修改->已暂存:暂存文件
已暂存->未修改:提交
未跟踪->已暂存:添加文件
@enduml
~~~

* 查看当前文件状态

~~~ code
git status
~~~

* 跟踪新文件

用git add 命令开始跟踪新文件

~~~ code
git add <filename>
~~~

* 暂存已修改的文件

git add是一个多功能文件，既可以用来跟踪新文件，也可以用来暂存文件，还可以有其他功能。把git add 命令理解成“添加内容到下一次提交中”。

* 显示跟简洁的状态信息

~~~ code
git status -s
~~~

文件列表旁的标记分两列，左列表明文件是否暂存，右列表明文件是否修改。A标记已暂存的新文件，M标记一个已修改的文件，？？标记一个未跟踪的文件。

* 忽略文件

如果不希望某一类文件被git自动添加，可以创建.gitignore文件。匹配规则如下：
  
  1. 空行或者以#开始的行被忽略
  2. 支持标准glob模式(简化版正则表达式)
  3. 以斜杠（/）开头的模式可用于禁止递归匹配
  4. 以斜杠（/）结尾的模式表示目录
  5. 以感叹号（！）开始的模式取反
