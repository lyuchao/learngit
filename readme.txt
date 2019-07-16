Edit on dev
test for learning git
pull from github.com
Creating a new branch is quick and simple.
from chao's laptop and now is 15:31

学习笔记：
抓取分支：
查看远程库信息： git remote -v

多人协作
创建远程origin的dev分支到本地：
git checkout -b dev origin/dev 二者名字最好一致
做完修改后
git add some files
git commit -m "comments"
git push origin dev
如果推送失败，说明有小伙伴比你先提交。
我们可以用git pull 把最新的提交从origin/dev抓下来，然后和本地合并，手动解决冲突，再推送
git pull
如果显示失败 no tracking information for the current branch则需要先关联本地的dev和远程的origin/dev
git branch --set-upstream-to=origin/dev dev
手动修改冲突后
git commit -m "conflict fixed"
git push origin dev

1. 当远程程序有了新的branch的时候，我们需要使用 git pull,然后再用
git checkout -b dev origin/dev 来构建他们之间的联系。
2. 只需要一个文件夹来管理同一个程序，不需要给定不同的文件夹名称。
