---
title: 在Windows上部署Stable Diffusion教程
date: 2023-06-20 20:20:20
tag: AI
categories: AI
---

Stable-Diffusion-webui(以下简称SD)是由AUTOMATIC1111建立的一个项目，为我们使用AI绘画提供了很多便利。
接下来我将详细介绍如何在本地部署SD。
其实本身也没什么难的，只要弄好网络环境就行。
PS：仅限N卡，A卡请另寻他路。
PSS：恕不提供其他软件下载地址。

 *开始部署*
你需要准备的：
# **Python3.10**
安装Python的时候记得勾选上add to path(不然就等着去手动加吧)

# **Git**
我们使用Git来clone仓库地址，以便部署。
这是我们更新SD必备的工具(你也不想每次重新部署吧)

准备工程做好，接下来开始安装SD。

# **代理工具**
找到你的本地代理地址并记住
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/%E4%BB%A3%E7%90%86%E5%9C%B0%E5%9D%80.png)

# **Clone仓库**
找到一个你要放置SD的目录，shift+右键打开终端
输入以下命令
git config --global http.proxy 代理地址:端口号 
git config --global https.proxy 代理地址:端口号
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/202309191046764.png)
然后输入git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git
图中的代理地址输错了，照着后面来就行(
因为我已经在E盘部署了一个，所以换了一个目录
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/SD%E9%83%A8%E7%BD%B2.png)

# **安装SD**
我们CD进入SD根目录，运行webui-user.bat
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/SD%E5%AE%89%E8%A3%85.png)
然后就会自动安装依赖什么的，等待安装完成就行

最后我们就可以运行SD了
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/SD%E8%BF%90%E8%A1%8C%E7%95%8C%E9%9D%A2.png)
可以看到URL后面有一栏 http://127.0.0.1:7860
我们在浏览器(推荐使用Chrome和Edge)中输入并进入SD界面可以看到如图就是成功了
![](https://tenicol.oss-cn-shanghai.aliyuncs.com/website/SD%E7%95%8C%E9%9D%A2.png)

## *结束部署*
接下来就尽情生成图片吧！

PS:如果安装途中有重启过终端，请重新设置代理，不然大概率会报错
PSS:如果你本身设置了国内源，可以不设置代理，但是注意当遇到卡在installing gfpgan或者报错提示找不到合适的tb-nightly版本时应该切换成阿里源




