

只显示提交信息的第一行: 
git log --pretty=short  

git log后面加上目录名,便会只显示该目录下的提交  

切换回上一个分支  
git checkout -


1 要让仓库的HEAD, 暂存区, 当前工作树回溯到指定状态,需要用git reset --hard命令,git reset --hard也可以往前回溯
2 如何往前推进: git log只能查看以当前状态为终点的历史日志,这里需要使用git reflog命令,查看当前仓库的操作日志,在日志中找出回溯历史之前的哈希值,最后通过git reset --hard commitid恢复到回溯历史前的状态:  
首先执行git reflog命令,查看当前仓库执行过的操作日志  
只要不进行git的gc, 在日志中就可以看到commit, checkout, reset, , merge等git命令的操作记录,



git中需要填commit id的地方,commit id至少4位


git rebase -i HEAD~2,可选定当前分支中包含HEAD(最新提交)在内的两个最新历史记录为对象


git push -u origin master
-u可以在推送同时,将origin仓库的master分支设置为本地仓库当前分支的上游(upstream),

