# git 学习指北

写在前面：

- 我深受于不会使用git和GitHub带来的麻烦
- 对服务器和本地的代码同步与版本管理有很大的障碍
- 希望通过对git的学习来解决这一问题。git_tutorial 文件夹将被同步于Github上的同名仓库

**git 是目前运用最广的版本控制软件**

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
- git commit - 将暂存区内容添加到仓库中。

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214141585.png" alt="image-20220920214141585" style="zoom:80%;" />

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214154752.png" alt="image-20220920214154752" style="zoom:80%;" />

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214233866.png" alt="image-20220920214233866" style="zoom: 80%;" />

<img src="D:\Appdata\Typora\typora-user-images\image-20220920214258278.png" alt="image-20220920214258278" style="zoom: 80%;" />