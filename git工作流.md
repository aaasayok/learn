```
git 团队协作的一些命令

1.开分支

git branch 新分支名
例如，在master分支下，新开一个开发分支：
git branch dev


2.切换到新分支

git checkout 分支名
例如，在master分支下，切换到新开的dev：
git checkout dev


3.开分支和切换分支合并到一个命令

git checkout -b 新分支名
例如，新开一个开发分支，并立即切换到该分支：
git checkout -b dev


4.切换回原分支

git checkout 原分支名
例如，切换回master
git checkout master
注意：当前分支有修改，还未commit的时候，会切换失败，应当先commit，但可以不用push


5.合并分支

git merge 需要合并的分支名
例如，刚刚已经切换回master，现在需要合并dev的内容：
git merge dev
建议在GitLab(或者其他git系统)上面创建merge request的形式来进行分支的合并和代码审核。


6.查看本地分支列表

git branch -a
前面带remotes/origin 的，是远程分支


7.查看远程分支列表

git branch -r


8.向远程提交本地新开的分支

git push origin 新分支名
例如，刚刚在master下新开的dev分支：
git push origin dev


9.删除远程分支

git push origin :远程分支名
例如，删除刚刚提交到远程的dev分支：
git push origin :dev


10.删除本地分支

git branch 分支名称 -d
例如，在master分支下，删除新开的dev分支：
git branch dev -d
注意：如果dev的更改，push到远程，在GitLab(或者其他git系统)上面进行了merge操作，但是本地master没有pull最新的代码，会删除不成功，可以先git pull origin master，或者强制删除
git branch dev -D


11.更新分支列表信息

git fetch -p
```

12. 忽略文件不提交

	git update-index --assume-unchanged logs/*.log

	重置改标识：git update-index --no-assume-unchanged




