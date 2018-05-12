虽然没写文章，但倒腾博客倒是花了些时间，把使用Hexo+Github Pages搭建博客的过程整理分享一下。



# Hexo

直接阅读Hexo官方文档，搭建好博客。

`npm install hexo-cli -g `

博客目录建成后在source/_posts目录下新建文章，或通过命令`hexo new`新建文章。

生成博客

`hexo g`

发布博客

`hexo d`





# Github Pages

Github Pages本身不多做介绍了，直接在Github上建立以xxx.github.io命名的项目，该地址也为Github Pages的访问地址。



为了方便博客发布，在本地配置好个人Github的SSH Key，为了在各个多端写博客，可以将自己的hexo项目放到Github上。



# 域名

我的域名是在阿里云购买的，也就是[万网](https://wanwang.aliyun.com/)提供的服务。最近.top域名非常便宜，4RMB就能买一年。域名购买好之后就可以在后台配置域名解析，和我们的Github Pages进行绑定。



## 1. 获取Github Pages的IP地址

直接在命令行中Ping Github Pages地址，如我的：hengz.github.io，得到IP地址。如下图所示：

![](https://i.loli.net/2018/05/12/5af6b688d7e8e.png)

我的Github Pages IP是：185.199.108.153



## 2. 配置域名解析

在阿里云后台找到域名解析，点击域名解析。如下图所示：

![](https://i.loli.net/2018/05/12/5af6b762c0555.png)

然后我添加了两条解析，「记录类型」为**A**，「主机记录」分别配置为**www**和**@**，「解析线路」为**默认**，「记录值」为要解析的IP，「TTL值」默认**10分钟**，然后保存即可。如下图所示：

![](https://i.loli.net/2018/05/12/5af6bd2905ab5.png)

域名刚申请的时候这里可能默认有一些默认配置，直接删除即可。配置完成后如图所示：

![](https://i.loli.net/2018/05/12/5af6b82dd0c31.png)



## 3. 配置Github Pages的Custom domain

打开Github Pages项目的配置页面，如图：

![](https://i.loli.net/2018/05/12/5af6bebd1101e.png)

然后往下找到GitHub Pages的配置，并填写你的域名，保存即可。如下图所示：

![](https://i.loli.net/2018/05/12/5af6bf309aa85.png)

完成后，就可以直接通过设置的域名，访问你的Github Pages了！如我自己的是：hengz117.top