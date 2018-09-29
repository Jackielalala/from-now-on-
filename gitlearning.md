git config --global user.email ""
git add . <当前文件全部传到暂存区>
git commit -am ""
git pull
git init <自己的文件夹非仓库时，初始化为仓库>

将本地库推送到远程：
git remote add origin SSH
git push (-u) origin master

git remote -v <查看本地库中的远程库地址>
git push -f origin master <强制推送，可能会覆盖别人的代码>
git remote add abc SSH <再添加一个远程库的标签abc,abc相当于另一个origin>
git remote remove abc <删除abc标签>
git remote set-url origin SSH <修改origin标签对应的地址>
git remote rename abc coding <把abc标签改名为coding>

分支操作 <允许多人同时开发然后合并到主干上>：
git branch -a <查看所有分支>
git branch A <新建分支>
git checkout A <切换分支>
可在分支中添加文件
git push origin A <将分支推送到远程>
将分支推送到开发机上观看是否可行，再合并到主干上就可以发布上线了
git checkout master/git merge A <分支推送到主干上>

冲突：当自己和别人更改同一个分支的同一个地方，在执行git pull时更新本地合并时会出现冲突，此时需要修改冲突文件，用vim命令行进行文件内容的选择，再重新提交。


