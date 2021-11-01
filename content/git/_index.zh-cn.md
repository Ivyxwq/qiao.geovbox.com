---
title: Git笔记
weight: 4
pre: "<b></b>"
---

Ivyxwq学习Git的笔记。

* [搭建Git服务器 ]({{%relref "init/_index.zh-cn.md" %}})
* [多个git账号的登录与切换]({{%relref "multuser/_index.zh-cn.md" %}})
* [fork后，更新到原作者的主分支]({{%relref "fork/_index.zh-cn.md" %}})
* 设置用户 
	```
	git config --global user.name "geovbox"
	git config --global user.email "geovbox@163.com"
	```
	
* 本地仓库pull+push
	```
	git remote add origin https://github.com/Ivyxwq/git.git
	git clone https://github.com/Ivyxwq/qiao.geovbox.com
	git pull origin master先将远程仓库master中的信息同步到本地仓库master中
	git status 查看工作区代码相对于暂存区的差别
	git add . 将当前目录下修改的所有代码从工作区添加到暂存区 . 代表当前目录
	git commit -m ‘注释’ 将缓存区内容添加到本地仓库
	git push origin master 将本地版本库推送到远程服务器
	密码要记得使用TOKEN
	```
	
* 重命名文件夹/文件 
	```
	git mv -f content/rocks/advance/ content/rocks/share`
	```
	
* 修改 Git 远程仓库地址 `gedit .git/config`
```
[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
[remote "origin"]
        fetch = +refs/heads/*:refs/remotes/origin/*
        #设置使用哪个远程库
        url = ssh://li_changsheng@ip:1234/home/vpost.git
#       url = https://github.com/demsheng/vpost.git
[branch "master"]
        remote = origin
        merge = refs/heads/master
```

* [修改默认端口号]({{%relref "port/_index.zh-cn.md" %}})
