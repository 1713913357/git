#### 学习新技术的三个步骤：

1.它是什么？

2.它能解决你什么问题？能给你带来什么好处？

3.学习（官网）


### git是什么？

**git是一个开源的，分布式的版本控制系统，他可以管理从极小到非常大的项目。**

和git类似的还有svn

**svn是集中式的版本控制系统**。

什么是集中式？什么分布式？



```
全局配置用户名：

git config --global user.name  xxx

全局配置邮箱：

git config --global user.email wewewe@163.com

git config --list 查看全局的配置

```


命令 | 说明
---|---
git init | 初始化本地版本库
git status | 查看工作区和暂存区的状态
git add . | 把工作区所有的修改提交到暂存区
git commit -m "描述" | 把暂存区的修改提交到本地版本库
git log | 查看历史记录
git reflog | 查看所有的历史记录
git diff | 查看工作区具体的修改
git diff --cached | 查看暂存区具体的修改
git checkout -- 文件路径 | 撤销工作区的修改
git push origin master（分支） | 向远程仓库推送（提交）代码 
git pull origin master（分支） | 从远程仓库拉取代码
git checkout -b 分支名 | 创建并切换分支
git branch 分支名 | 新建分支
git checkout 分支名 | 切换分支
git branch | 查看本地所有的分支
git branch -r | 查看远程所有的分支
git branch -a | 查看远程和本地所有的分支
git branch -d 分支名 | 删除本地分支
git push origin -d 分支名 | 删除远程分支
git stash | 保存工作区的修改
git stash pop | 恢复工作区的修改


```
git pull  ：远程拉取代码并和本地的代码合并

git fetch ： 把远程的代码拉取到本地不合并

git merge origin/分支名： 合并代码

git pull = git fetch + git merge
```



把工作区的修改提交到本地版本库：

1.git add . 

2.git commit -m "描述"


```
第一种情况：撤销工作区的修改

git checkout -- 文件路径

第二种情况：撤销暂存区的修改

第一步：git reset 文件路径  从暂存区撤销回工作区

第二步：git checkout -- 文件路径

第三种情况：回退版本

git reset --hard HEAD^ 回退到上一个版本 ^^上上个版本

git reset --hard commit_id  回退到指定版本

```

#### github

**github是一个面向开源及私有的软件项目托管平台。**

github支持两种协议：**https ssh**

克隆远程仓库：**git clone 仓库地址**


ssh协议:配置公钥和秘钥

**ssh-keygen**  生成公钥秘钥

https协议：需要输入用户名和密码

本地添加远程仓库：

```
git remote add origin 仓库的地址

git remote -v 查看关联的远程仓库
```
- **冲突**
```
<<<<<<< HEAD
=======
>>>>>>> 3cc035502fa68540def174f7d2203dcb4b144282

冲突，需要手动去解决冲突，执行git add ---》 git commit -m ===> git push origin 分支
```
- 忽略文件 ：.gitignore
















