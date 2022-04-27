---
title: Git & GitHub使用指南
---

---

#### 介绍

**1. Git & GitHub的发展历史**

Linux 之父 Linus 在 1991 年创建开源的 Linux 操作系统之后，Linus 花了十天时间用 C 语言写好了一个开源的版本控制系统（Version Control System），就是著名的 Git。


2007 年旧金山三个年轻人觉得 Git 是个好东西，就搞了一个公司名字叫 GitHub，第二年上线了使用 Ruby 编写的同名网站 GitHub，这是一个基于 Git 的免费代码托管网站（有付费服务）

Github被微软收购

---

### Github Desk简单操作

<i class="fa fa-arrow-circle-down" aria-hidden="true"> 教学步骤</i>：

**1. 下载安装Github**

https://desktop.github.com/

**2. 注册账号**

https://github.com/

**3. 新建项目** 

启动Github，菜单栏File，选择 New repository，

填写Name，选择Local path

**4. 文件夹更新项目内容** 

提交Summit

**5. 发布项目** 

菜单栏New repository，选择Push 

---

### Git简单操作

<i class="fa fa-arrow-circle-down" aria-hidden="true"> 教学步骤</i>：

**1. Start a project**

登录Github，https://github.com/， 点击Start a project

**2. Create a new repository**

填写Repository name，选择Public/Private， 点击Create Repository

**3. 获取链接**

https://github.com/sheldonyue/machineLearning.git

---

**4. 下载安装Git**

https://git-scm.com/
默认设置，一路Next

**5. 检查Git安装**

打开终端Command Prompt，输入git version

**6. 创建项目**

cd 项目路径 
如：D:\AI\03RNN\AI-Writer-project

**7. 配置Git**

git config --global user.name 'sheldonyue' 

git config --global user.email 'sheldonyue@sina.com'

**7. 检查配置**

git config -l

查看最后两行name 和 email

---

**8. 初始化本地仓库**

git init

**9. 关联远端Git仓库**

git remote add origin https://github.com/sheldonyue/machineLearning.git

查看最后两行name 和 email

**10. 查看本地项目文件夹变化**

git status

**11. 更新本地Git项目**

git add *

git commit -m "first commit"

！注意：必须用双引号

**12. 推送到远端**

git push -u origin master

说明：推送小于100MB的项目

---

### Git-LFS上传大文件

<i class="fa fa-arrow-circle-down" aria-hidden="true"> 教学步骤</i>：

**1. 下载文件**


```python
https://git-lfs.github.com/
```

**2. 安装到git目录下**


```python
C:\Program Files\Git\bin\Git LFS
```

**3. 上传大文件**


```python
git init #创建本地仓库环境
git lfs install #安装大文件上传应用
git lfs track * #追踪要上传的大文件，*表示路径下的所有文件
git add .gitattributes #添加先上传的属性文件(要先上传属性文件，不然有可能失败)
git commit -m "pre" #添加属性文件上传的说明
git remote add origin https://github.com/Youpeng-Zhang/MOP.git #建立本地和Github仓库的链接
git push origin master #上传属性文件
git add * #添加要上传的大文件，*表示路径下的所有文件
git commit -m "Git LFS commit" #添加大文件上传的说明
git push origin master #上传大文件
```

---

### Github获取开源项目

<i class="fa fa-arrow-circle-down" aria-hidden="true"> 教学步骤</i>：

**1. Fork**

**2. 修改文件**

commit changes

**3. 提交修改**

菜单pull request， 点击New pull request， create pull request

**4. 项目创建人收到 Pull request**

Merge pull request，confirm merge

---

### Github  Pages制作网站

**1. 创建仓库**

登录Github， 创建仓库名为username.github.io

注意：username必须与你的用户名完全匹配

**2. 创建网站**

勾选Add a README file

**3. 添加网站模板**

点击setting， 找到Github pages， 点击choose a theme， 选择模板

**4. 保存网站**

点击commit changes

---

### Github+ Gridea建设网站

**1. 下载Gridea客户端**

https://gridea.dev/

**2. 获取个人访问令牌**

点击Github头像， 点击Setting， 进入Develper settings，进入Personal access tokens
，生成新token， 输入Github密码， 输入token名称， 选择范围全部打勾，生成令牌

保存好token: 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

**3. Gridea与Github建立连接**

点击远程， 输入Github域名， 仓库名称， 分支默认， Github用户名， Github用户名， Github邮箱

保存， 检测远程连接， 成功后点击同步，检查Github仓库是否多出一些文件夹。

**4. 美化网站**

选择主题，网站相关信息更新

https://www.bilibili.com/video/BV1Fb4y1Y7e4/?spm_id_from=333.788.recommend_more_video.7


```python
https://www.bilibili.com/video/BV1ME41147bv/?spm_id_from=333.788.recommend_more_video.-1
```

### 提高Github访问速度

**1. 修改hosts**


```python
Windows hosts目录：C:\windows\system32\drivers\etc\
    
# Github
192.30.253.113 github.com
151.101.185.194 github.global.ssl.fastly.net
203.98.7.65 gist.github.com
13.229.189.0 codeload.github.com
185.199.109.153 desktop.github.com 
185.199.108.153 guides.github.com  
185.199.108.153 blog.github.com
18.204.240.114 status.github.com
185.199.108.153 developer.github.com
185.199.108.153 services.github.com
192.30.253.175 enterprise.github.com   
34.195.49.195 education.github.com    
185.199.108.153 pages.github.com  
34.196.237.103 classroom.github.com
```

**2. 刷新DNS网页缓存**

DNS网页缓存刷新CMD指令：ipconfig /flushdns


```python
https://www.bilibili.com/video/BV1Fb4y1Y7e4/?spm_id_from=333.788.recommend_more_video.7
```
