# `git学习笔记` #

1.git checkout -- aa.txt 恢复本地删除的文件

2.git checkout master

3.git merge testing 合并分支


## 建立分支 ##

git branch test

git remote -v 查看git远程库地址

git 删除 git rm debug.log git commit -m "rm de=bug.log" git push orgin master / git push

$ git reset HEAD readme.txt //撤销修改

vi 取消操作 esc u 粘贴 esc p 删除 esc d 退出 esc :wq

git学习 Creating a new branch is quick Creating a new branch is quick AND simple.

git add . 添加所有 git commit -m "" 提交 git push origin master 推送 git pull
origin master 拉取

git clone http://地址 下载

git add remote httP://地址 添加远程

git status 查看

## Git鼓励大量使用分支： ##

查看分支：git branch 

创建分支：git branch <name> 

切换分支：git checkout <name> 

创建+切换分支：git checkout -b <name> 

合并某分支到当前分支：git merge <name> 

删除分支：git branch -d <name> 

查看远程分支：git branch -a
