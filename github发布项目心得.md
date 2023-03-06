# 过程

首先，开始我没打算用这个，但是在gitbook制作好静态网页电子书之后，需要找个仓库挂上去，因此就需要用到GitHub的仓库

## git安装

先去官网下载一个git，具体的安装过程可以去看一下这篇文章[[(23条消息) Git 详细安装教程（详解 Git 安装过程的每一个步骤）_git安装_mukes的博客-CSDN博客](https://blog.csdn.net/mukes/article/details/115693833)]

安装好之后看看开始菜单栏是否有git bash等相关的git文件，如果有则是安装成功，然后在对你要进行发布的文件夹，鼠标右键，git bash here，然后就会打开一个终端界面，使用git init指令尝试是否能够正常使用，因为我之前安装过另外一个版本的git，再次重装时出现了错误，我就把之前的那个卸载了，重新下载了一个，然后就能成功；

## 创建GitHub仓库

创建好仓库名之后，我都是无脑下一步，创建好之后，发现会提供一个SSH地址和HTTPS地址，

## 创建主分支

在终端下输入git init指令把当前目录当作仓库，成功之后，在输入git  add .指令，将当前文件夹的所有内容添加进入仓库，添加成功之后，使用git commit -m "自定义"，成功之后将刚才的HTTPS地址复制过来，输入指令git remote  add origin "HTTPS地址"，然后使用git push -u origin master即可成功将文件夹中的内容发布在仓库中了，最后一步可能会出现unable to access的错误，这是文件夹的权限的问题，解决方法：点击文件夹-右键属性-安全-高级-在所有者那里点击更改-点击高级-立即查找-找到自己的用户名双击-确定-勾选替换子容器和对象的所有者以及使用可以从对象集成的权限项目替换所有子对象的权限项目-点击确定，再次使用git push -u origin master 即可成功发布

##  创建其它分支

在当前的文件夹下删除不需要的文件，将需要的文件添加进来，再次使用git init指令,然后输入git checkout --orphan 分支名，然后就会切换到其它分支，接着git add .添加你刚才在文件夹中文件，git commit -m "自定义"，git remote  add origin "HTTPS地址"，git push origin 分支名，然后其他分支也就创建成功了，以此类推



详细请看：https://www.bilibili.com/video/BV1H54y1t7fD/?spm_id_from=333.337.search-card.all.click&vd_source=69c34be98546fc9be1ed77c35104cf83





