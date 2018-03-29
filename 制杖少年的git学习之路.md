# 制杖少年的git学习之路

## 配置git
    - 首先在本地创建ssh key
        ssh-keygen -t rsa -C "your_email@youremail.com"
        后面的your_email@youremail.com改为你在github上注册的邮箱，之后会要求确认路径和输入密码，我们这使用默认的一路回车就行。成功的话会在~/下生成.ssh文件夹，进去，打开id_rsa.pub，复制里面的key。
        回到github上，进入 Account Settings（账户配置），左边选择SSH Keys，Add SSH Key,title随便填，粘贴在你电脑上生成的key。
    - 验证是否成功
        ssh -T git@github.com
        如果是第一次的会提示是否continue，输入yes就会看到：You've successfully authenticated, but GitHub does not provide shell access 。这就表示已成功连上github。
    - 配置全局环境
        git config --global user.name "your name"
        git config --global user.email "your_email@youremail.com"

## 将本地文件上传到远程仓库
    - git init //初始化仓库 
    - git add .(文件name) //添加文件到本地仓库
    - git commit -m "first commit" //添加文件描述信息
    - git remote add origin + 远程仓库地址 //链接远程仓库，创建主分支
    - git pull origin master // 把本地仓库的变化连接到远程仓库主分支
        - git pull 出错办法
        - git pull origin master --allow-unrelated-histories
    - git push -u origin master //把本地仓库的文件推送到远程仓库   
    
## 下载别人仓库的文件
    - git clone git@github.com:shilihepan/mesona.git 