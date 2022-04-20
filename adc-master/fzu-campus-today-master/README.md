# fzu-campus-today

> Create By ZhangRongRong [项目源码miyarr](https://gitee.com/miyarr/mysite)
>
> Modify By Una

## Gitee

1. 注册一个gitee账号，创建一个仓库
2. 在本地创建一个文件夹当做仓库，右键`git bash here`

```
git config --global user.name "你的名字或昵称"

git config --global user.email "你的邮箱"

ssh-keygen -t rsa -C "你的GitTee注册邮箱" # 生成ssh密钥

cat ~/.ssh/id_rsa.pub # 查看密钥

#添加公钥：gitee.com→用户头像→Settings→SSH and GPG keys→New SSH key→将id_rsa.pub中的内容复制到Key文本框中，然后点击Add SSH key(添加SSH)按钮

git clone git@gitee.com:xxx/xxx.git # 克隆自己的项目

cd xxx  # 进入项目，将fzu文件夹复制到项目里

git add . # 保存到缓存区

git commit -m “要描述的内容” # 描述这次提交的内容 (推送到本地库中)

git push origin master # 提交
```

3. 开启`Gitee Pages`服务

   ![](https://una-love.oss-cn-beijing.aliyuncs.com/figured/20210316130105.png)

   开启服务之后将你的网站地址加上`/fzu/fzu.html`就是今日校园扫描界面

   > http://xxx.gitee.io/xxx/fzu/fzu.html

   ![](https://una-love.oss-cn-beijing.aliyuncs.com/figured/20210316130040.png)

4. 生成二维码

   利用[在线二维码生成网站](https://www.wwei.cn/)将网址输入生成二维码，手机存到相册后，用xx校园app扫它~


## 一卡通

> 因为现在今日校园无法使用了，所以对项目进行更新，添加了一卡通的页面
>
> 如果有用到这个项目的朋友希望是部署到自己的网站上而不是用我的链接，好人一生平安

1. `card`文件夹为一卡通的页面和资源文件

2. `page1.html`为参数页面，传入例如姓名学号等参数，通过五个按钮来选择显示哪个头像

3. `page2.html`为一卡通主页面，只有一码通按钮有用，实现跳转到一码通页面，头像资源在`card/images/`文件夹下，分别为`ZY.png`，`CC.png`，`ZF.png`，`LB.png`，`DC.png`，如果想显示自己的照片，把自己证件照复制到这个文件夹下，然后覆盖`ZY.png`，那`page1.html`赵云按钮显示的就是自己的照片。

4. `page3.html`为现在的一码通，需要注意的是跳动的标语是每日更新的，

5. 将`card`文件夹下载然后进行照片替换放到自己gitee仓库下，上传更新就可以使用了。

6. 微信打开链接

   > http://xxx.gitee.io/xxx/card/page1.html