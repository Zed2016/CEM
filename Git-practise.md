* git init

* git add

* git commit 可以将多次的add提交

* git log查看提交历史

* git diff 查看未add的与上次commit之间的差别， add之后就不能使用了

* git reset --hard (HEAD指当前，HEAD^指上一个版本，HEAD^^指上上一个版本)，后面直接加版本号也可以，五个字符就行。**HEAD相当于一个指针**

* git reflog 查看命令历史

* git checkout 撤销修改

  * 一种是`文件.txt`自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
  * 一种是`文件.txt`已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

* git reset HEAD <file> 把暂存区的修改撤销掉unstage，重新放回公共区

* git rm 

  * 1. 如果你用的rm删除文件，那就相当于只删除了工作区的文件，如果想要恢复，直接用git checkout -- <file>就可以
    2. .如果你用的是git rm删除文件，那就相当于不仅删除了文件，而且还添加到了暂存区，需要先git reset HEAD <file>，然后再git checkout -- <file>
    3. 如果你想彻底把版本库的删除掉，先git rm，再git commit 就ok了

* 创建SSH，添加key进入github，让github知道是这台电脑push的东西

* 添加远程库git remote add origin git@github.com:michaelliao/learngit.git

* git push 推送到远程库

* git clone 克隆远程版本库

* git-checkout - Switch branches or restore working tree files

* 查看分支：`git branch`

  创建分支：`git branch <name>`

  切换分支：`git checkout <name>`

  创建+切换分支：`git checkout -b <name>`

  合并某分支到当前分支：`git merge <name>`

  删除分支：`git branch -d <name>`

* git status 查看分支冲突的文件等

* git stash 暂存当前的工作，暂存之后工作区clean

* git stash list 查看暂存列表

* git stash apply 恢复暂存内容，但是不清理暂存列表

* git stash pop 恢复暂存内容，同时清理暂存列表

* git stash drop 清理暂存列表

* git branch -D <name>强行删除分支

* git remote -v 查看远程分支以及权限

* git push origin master/dev/feature 推送分支，就是把该分支上的所有本地提交推送到远程库。推送时，要指定本地分支，这样，Git就会把该分支推送到远程库对应的远程分支上

* 如果`git pull`提示`no tracking information`，则说明本地分支和远程分支的链接关系没有创建，用命令`git branch --set-upstream-to <branch-name> origin/<branch-name>`。

* ***Rebase以后再看***

* git tag vx.x 切换到需要的分支，然后打标签为vx.x

* git tag 查看标签

* 命令`git push origin <tagname>`可以推送一个本地标签；

* 命令`git push origin --tags`可以推送全部未推送过的本地标签；

* 命令`git tag -d <tagname>`可以删除一个本地标签；

* 命令`git push origin :refs/tags/<tagname>`可以删除一个远程标签。

* `.gitignore`文件，忽略文件
