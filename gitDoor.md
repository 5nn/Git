
##本地一般操作

经常用到的命令


```
$git init
$git status
$git add xxx.md
%git commit -m "add a file .md"

```


## <a name="editor-pane"></a>后面如果修改了则

* git add xxx.md
* git commit -m "fix something"


##<a name="editor-pane"></a>回退
git reset --head HEAD^  `
  回退到上一个版本
`

git reset --hard 555666
`
回退到版本号为开头为555666的版本
`

##<a name="editor-pane"></a>查看工作区和版本区代码的不同

git diff HEAD -- xxx.md


##查看所有版本
git log --pretty=oneline

##公司网络下将项目上传到github

git remote rm origin

git remote add origin https://github.com/5nn/gitDoor.git

git config --global https.proxy https://name:password@10.10.10.10:3128

git config --global http.proxy http://name:password@10.10.10.10:3128

git pull --rebase origin master

git push -u origin master 
`第一次提交加 -u 进行关联 以后提交本地作业只需要
git push origin master
`