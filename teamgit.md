

##一次愉快的合作！

##proxy
git clone https://github.com/Tomikes/Tomikes.github.io.git

git config --global http.proxy http://name:password@10.10.10.10:3128


##demo
```
mis-3216026:AFNetworking mikeshang$ LS
AFNetworking			Framework
AFNetworking.podspec		LICENSE
AFNetworking.xcodeproj		README.md
AFNetworking.xcworkspace	Tests
CHANGELOG.md			UIKit+AFNetworking
CONTRIBUTING.md			fastlane
Example
``` 
###查看git状态  --master主支上
```
mis-3216026:AFNetworking mikeshang$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```
```
mis-3216026:AFNetworking mikeshang$ git branch
* master
```
###git checkout -b <name>  创建并切换分支
```
git branch <name>  --创建
git checkout <name>  --切换
```
```
mis-3216026:AFNetworking mikeshang$ git checkout -b 5nn
Switched to a new branch '5nn'
```
```
mis-3216026:AFNetworking mikeshang$ git status
On branch 5nn
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   AFNetworking/AFNetworkReachabilityManager.m

no changes added to commit (use "git add" and/or "git commit -a")

```
```
mis-3216026:AFNetworking mikeshang$ git add  AFNetworking/AFNetworkReachabilityManager.m
```
```
mis-3216026:AFNetworking mikeshang$ git commit -m "good string"
[5nn ef24195] good string
 1 file changed, 3 insertions(+), 1 deletion(-)

```
```
mis-3216026:AFNetworking mikeshang$ git branch
* 5nn
  master
```  

##切回主支并合并分支
```
mis-3216026:AFNetworking mikeshang$ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

```
```
mis-3216026:AFNetworking mikeshang$ git merge --no-ff -m "merge with no-ff" 5nn
Updating 4f3c694..ef24195
Fast-forward
 AFNetworking/AFNetworkReachabilityManager.m | 4 +++-
 1 file changed, 3 insertions(+), 1 deletion(-)
```
##删除分支
``` 
mis-3216026:AFNetworking mikeshang$ git branch -d 5nn
Deleted branch 5nn (was ef24195).

```

##git tag
```
git tag -a v0.1 -m "version 0.1 released" 3628164xxxx

```
```
git tag
v0.9
v1.0
```
```
git show v0.9

commit fce77fc4c044a89ff59ccea9d2bdf8dbc78018c0
Author: xxxxx
Date:   Wed Oct 26 16:02:07 2016 +0800

    push local to master

diff --git a/gitDoor.md b/gitDoor.md
index 4e13fd8..dee7098 100644
--- a/gitDoor.md
+++ b/gitDoor.md
@@ -47,4 +47,9 @@ git config --global https.proxy https://name:password@10.10.10.10:3128
 
 git config --global http.proxy http://name:password@10.10.10.10:3128
 
-git pull --rebase origin master
\ No newline at end of file
+git pull --rebase origin master
+
+git git push -u origin master 
+`第一次提交加 -u 进行关联 以后提交本地作业只需要
+git push origin master
+`

```
```
git push origin --tags   ---可以推送全部未推送过的本地标签
git tag -d <tagname>     ---可以删除一个本地标签
git push origin :refs/tags/<tagname> ---可以删除一个远程标签,一般不用
```