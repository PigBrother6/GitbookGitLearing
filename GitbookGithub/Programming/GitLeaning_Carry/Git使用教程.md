# Git 使用教程

# 一、常用命令

- 初始化为 git 仓库 `git init`
- 添加文件到版本库 `git add .` 其中 “.” 可以是具体的文件名或文件夹名
- 提交到本地仓库 `git commit -m "提交说明"`
- 时刻掌握仓库当前的状态 `git status`
- 查看文件修改内容 `git diff 文件名`
- 查看提交历史记录 `git log`，简化输入信息 `git log --pretty=oneline`
- 回退到上一个版本 `git reset --hard HEAD`，回退到指定版本将 HEAD 改为 git log 中查出来的 commit id 即可
- 记录每一次提交命令 `git reflog`，可以使用此命令查看所有提交的 commit id  ，让我们可以在任意版本中穿梭
- 撤销文件修改 `git checkout -- 文件名`
- 删除不要的文件 `git rm 文件名` 并 `git commit -m "说明"`

# 二、同步远程仓库

- `git remote add origin 远程仓库地址`
- 如果新建远程仓库穿在文件，需要向同步远程仓库文件，`git pull origin master --allow-unrelated-histories`
- `git push -u origin master`由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令，后期用 `git push origin master`即可

如果第一次报错 ，可以强制提交
 `git push -f origin master`

git  init初始化仓库

git  add参数“。”为添加当前目录所有文件，也可以单独添加需要push远程的文件比如  git  add  text.txt

git  commit  提交

git  pull  --rebase  origin  master合并远程仓库代码到本地

git  push  -u  origin  master  同步  本地代码到远程仓库

git  remote  add  origin  远程仓库地址

git  checkout  develop  切换分支（分支名）

git  checkout  -b  develop切换到指定分支，如果不存在，就创建

git  clone  克隆

git  checkout  develop  origin/develop





作者：小强唐
链接：https://www.jianshu.com/p/8f0e6461673d
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。