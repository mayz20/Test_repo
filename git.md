# git 学习指北

写在前面：

- 我深受于不会使用git和GitHub带来的麻烦
- 对服务器和本地的代码同步与版本管理有很大的障碍
- 希望通过对git的学习来解决这一问题。
- git是一个版本控制的工具，GitHub是一个代码托管平台

### git的工作流程

- 克隆git资源作为工作目录
- 在克隆的资源上添加或修改文件
- 将本地的修改更新至资源库
- 如果发现错误，可以进行版本回退

### git工作区域

- 远程git仓库：**实现代码备份、共享，多人同步更新，集中化管理**
- 本地git仓库：**最终确定的文件保存到仓库，成为一个新的版本**
- 暂存区：**暂存已经修改的文件，最后统一提交到git仓库中**
- 工作区：**本地修改文件等操作** 
- add -> commit -> push 从下往上三步走

### 基本git命令

`git init` 使用当前目录作为git仓库，对它进行初始化

命令执行之后，当前目录会多出一个.git 文件夹



git本质上就是在上述四个区之间进行交互。通过如下的6个命令。

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214017719.png" alt="image-20220920214017719" style="zoom:67%;" />

- git init - 初始化仓库。
- git add  - 添加文件到暂存区。
- git add . 添加当前目录下所有文件到暂存区。
- git commit - 将暂存区内容添加到仓库中。

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214141585.png" alt="image-20220920214141585" style="zoom:80%;" />

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214154752.png" alt="image-20220920214154752" style="zoom:80%;" />

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214233866.png" alt="image-20220920214233866" style="zoom: 80%;" />

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214258278.png" alt="image-20220920214258278" style="zoom: 80%;" />



### git分支管理

每个分支代表一条独立的开发线

<img src="D:\Appdata\Typora\typora-user-images\image-20220921085752010.png" alt="image-20220921085752010" style="zoom:67%;" />

创建分支命令：`git branch (branchname)`

**没有参数时，git branch会列出本地的分支，在git init之后，默认会创建master分支**

切换分支命令：`git checkout (branchname)`

合并分支命令：`git merge`

以下是一个关于分支的测试demo

```
$ mkdir gitdemo
$ cd gitdemo/
$ git init
Initialized empty Git repository...
$ touch README
$ git add README
$ git commit -m '第一次版本提交'
[master (root-commit) 3b58100] 第一次版本提交
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README
 $ git branch
* master
$ git branch testing
$ git branch
* master
  testing
 
```

使用分支将 工作区分开，使我们可以在不同的开发环境进行不同的操作，并灵活切换

！！这是会同时改变工作区目录的 好厉害

当然 分支合并的时候可能产生冲突，这是需要我们手动处理的。

git log可以查看历史提交记录，git blame可以查看某文件的历史修改记录