# [git中Bash基本操作命令](https://www.cnblogs.com/weibanggang/p/9663623.html)

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
1）、cd : 改变目录。
2）、cd . . 回退到上一个目录，直接cd进入默认目录
3）、pwd : 显示当前所在的目录路径。
4）、ls(ll): 都是列出当前目录中的所有文件，只不过ll(两个ll)列出的内容更为详细。
5）、touch : 新建一个文件 如 touch index.js 就会在当前目录下新建一个index.js文件。
6）、rm: 删除一个文件, rm index.js 就会把index.js文件删除。
7）、mkdir: 新建一个目录,就是新建一个文件夹。
8）、rm -r : 删除一个文件夹, rm -r src 删除src目录， 好像不能用通配符。
9）、mv 移动文件, mv index.html src index.html 是我们要移动的文件, src 是目标文件夹,当然, 这样写,必须保证文件和目标文件夹在同一目录下。
10）、reset 重新初始化终端/清屏。
11）、clear 清屏。
12）、history 查看命令历史。
13）、help 帮助。
14）、exit 退出。
15）、#表示注释
git remote：查看远程库信息 
git remote -v：远程库详细信息
git branch -r ， git branch -a 查看远程分支
git push 将当前分支推送到远程对应的分支（若远程无对应分支，则推送无效） 
git push origin dev 将分支dev提交到远程origin/dev（远程没有则创建, 远程没有dev则创建） 
git branch –set-upstream branch-name origin/branch-name 建立本地分支和远程分支的关联
git checkout -b dev origin/dev 创建远程的origin/dev分支到本地
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

## 分支常用命令

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
查看分支：git branch 
创建分支：git branch name 
切换分支：git checkout name 工作区文件内容会立即变化成对应分支的内容 
创建+切换分支：git checkout -b name 
合并某分支到当前分支：git merge name 
删除分支：git branch -d name

查看分支合并情况：git log –graph –pretty=oneline –abbrev-commit

合并分支（fast forward）：git merge name 
合并分支（禁用 Fast forward）：git merge –no-ff -m “描述” dev
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

## 标签常用命令

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
1、创建标签git tag tagname 对当前版本建立标签 
git tag tagname commit_id 对历史版本建立标签 
git tag -a tagname -m “描述…” commit_id 添加说明 
git tag 查看所有标签 
git show tagname 查看某个标签具体信息2、删除标签git tag -d tagname 删除本地标签3、推送标签git push origin tagname 推送本地的某个标签到远程 git push origin –tags 一次性推送所有分支4、删除远程标签git tag -d tagname 先删除本地 git push origin :refs/tags/tagname 从远程删除
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

##  Git配置 - git config

使用git config -l 查看现在的git环境详细配置

![img](https://img2018.cnblogs.com/blog/1418466/201809/1418466-20180917181213712-1409777778.png)

## 设置用户名与邮箱（用户标识，必要） 

```
　$ git config --global user.name "[名称]"  
  $ git config --global user.email [邮箱]   
```

 

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
# 添加指定文件到暂存区
$ git add [file1] [file2] ...

# 添加指定目录到暂存区，包括子目录
$ git add [dir]

# 添加当前目录的所有文件到暂存区
$ git add .
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

# 使用vue-cil搭建项目

###### 大纲

> 1、安装NodeJs
> 2、安装vue-cli
> 3、创建项目
> 4、启动项目
> 5、打包项目
> 6、项目实例

###### 1、安装NodeJs

> NodeJs安装好之后会连带着安装一个npm，nodeJs的安装流程很简单，按着步骤一步一步下来即可。
> 安装完成之后在控制台上输入npm -v 以及 node -v若成功则会输出对应版本，并且已经将npm和node部署到了全局的环境变量。

###### 2、安装vue-cli

> 安装完成之后，可以通过vue list来查看可以使用哪些模板



```undefined
npm install -g vue-cli
```

![img](https://upload-images.jianshu.io/upload_images/12738399-9634e8c7df324c14.png?imageMogr2/auto-orient/strip|imageView2/2/w/800/format/webp)

安装vue-cli

###### 3、创建项目

> 完成项目的一系列配置



```kotlin
vue init webpack <your project>
```

![img](https://upload-images.jianshu.io/upload_images/12738399-a1fade5070c8efe6.png?imageMogr2/auto-orient/strip|imageView2/2/w/677/format/webp)

image.png

###### 4、启动项目



```undefined
npm run dev
```

> 启动之后的提示端口8080中打开了应用

![img](https://upload-images.jianshu.io/upload_images/12738399-00493b8b5f929090.png?imageMogr2/auto-orient/strip|imageView2/2/w/677/format/webp)

启动项目

###### 5、打包项目



```undefined
npm run build
```

###### 6、项目实例

> [vue项目实例](https://github.com/crk123kk/vue-example)中的vue-base中就是我自己搭建的vue的初始项目。