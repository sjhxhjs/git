完全空白项目关联

首先讲一种简单的场景，如果我们新建项目的时候没有生成任何的初始化文件，我们需要做的就是将本地的项目和空白的仓库关联起来，这种情况下的命令是：

#git初始化
git init
#设置remote地址
git remote add 地址
#将全部文件加入git版本管理 .的意思是将当前文件夹下的全部文件放到版本管理中
git add .
#提交文件 使用-m 编写注释
git commit -m "注释"
#推送到远程分支
git push

有文件的项目关联

然后就考虑最开始说的情况，就是远程仓库里已经有文件，这时候你执行上面的步骤是不可以的，因为需要把远程仓库的文件先更新下来。步骤如下

#git初始化
git init
#设置remote地址
git remote add  origin 地址
#获取远程仓库master分支上的内容
git pull origin master
#将当前分支设置为远程仓库的master分支
git branch --set-upstream-to=origin/master master
#将全部文件加入git版本管理 .的意思是将当前文件夹下的全部文件放到版本管理中
git add .
#提交文件 使用-m 编写注释
git commit -m "注释"
#推送到远程分支
git push


git 创建分支
git branch 分支名
切换分支
git checkout 分支名
提交分支
git push origin 分支名
合并分支
git merge 分支名
删除本地分支
git branch -d 分支名
删除远程分支
git push origin --delete 分支名 
