# 在腾讯云运行 RUM public 节点

[>>> Rum 信息导航](rum-app/about.md)

## 0、为什么需要云？

您可以采用个人电脑、安卓手机等运行 RUM 客户端。您正在运行的 RUM 客户端，就是一个 RUM 节点。成为 RUM 节点不需要任何资格认证，没有硬件或技术门槛，只要您能把 RUM 客户端运行起来，就可以。真正的去中心化。

那为什么依然有少量用户额外选购云服务器来运行 RUM 客户端呢？比如想要 7*24H 在线的 public 节点；搭建私有种子网络，供多台设备或多个亲友建立连接；又或者仅仅是想要趁着双 11 价格便宜，买一台云服务器练练手。

所以，如果把购买云服务器并跑 RUM public 节点当做一件有趣好玩的事，心态会更轻松。

**千万不要急匆匆地购买云服务器**。

## 一、登录腾讯云官网

### 1、登录腾讯云官网

访问官网 https://cloud.tencent.com/login 并登入

登入后，如果提示绑定微信号，可扫码。也可跳过。

![](https://docs.prsdev.club/rum-app/images/cloud_wechat.png)


### 2、进入控制台

在左上角的 `云产品` 找到 `轻量应用服务器` 或 `云服务器` —— 跟你所买的服务器类型有关。这次大家按娟娟推荐买，应该都是 `轻量应用服务器`。

点击它:

![](https://docs.prsdev.club/rum-app/images/cloud_server.png)

### 3、查看服务器概要

在 `服务器` 这个页签下，可以看到你买到的服务器。点服务器名字，可以打开一个新的页面，展示着服务器的概要。

![](https://docs.prsdev.club/rum-app/images/cloud_home.png)

在这个页面上，我们将完成服务器的初次设置。以后你也会频繁登入腾讯云官网来操作。

## 二、服务器初次设置

现在，你已经按照 `一` 的部分，来到了服务器概要页面。

作为新购服务器，需要完成以下三个操作。


### 1、更改操作系统（如果更熟悉 windows）

先是操作系统。

如果你不了解 linux 操作（它确实有门槛），更熟悉 windows，那么建议你就用 windows 来跑 RUM 足够了。

如果你熟悉 linux 操作，则可忽略这一步。

找到 `镜像信息`，点击 `重置应用`：

![](https://docs.prsdev.club/rum-app/images/cloud_mirror.png)

在新弹出的页面中，选择 windows 2016 （也可以选择其它 windows 版本，但大家版本一致，如果你遇到异常时，方便交流和获取帮助）。

因为这次大家都是新服务器，所以，`确认备份` 勾选一下即可，不需要做什么特别操作。

然后点击确认。等它完成后，回到服务器概要页。

![](https://docs.prsdev.club/rum-app/images/cloud_windows.png)

### 2、重置密码

在服务器概要页，找到 `重置密码`，点击它。

![](https://docs.prsdev.club/rum-app/images/cloud_pwd.png)

在弹出的页面的两个输入框，输入或粘贴你的新密码。

因为这次大家都是新服务器，所以，一开始是没有密码的（或系统自动生成的密码），建议设置一个复杂点的密码，并妥善保管好。以后远程登录服务器时会经常用到。

保管好密码后，再点击下一步。

![](https://docs.prsdev.club/rum-app/images/cloud_pwd2.png)


如果要重启服务器，没关系，勾选让它重启即可。重启完成后，回到服务器概要页。

### 3、打开TCP端口

从服务器概要切换到 `防火墙` 页。点击 `添加规则` 按钮。

![](https://docs.prsdev.club/rum-app/images/cloud_tcp.png)

![](https://docs.prsdev.club/rum-app/images/cloud_tcp1.png)

选择 `全部TCP`，其它不用动，点击确定。提交后，列表中会多出来一行 `全部TCP` 相关信息。

OK，服务器基本信息的三大更改完成了。接下来开始远程登录云服务器了。

## 三、登录你的云服务器

登录云服务器介绍两种方法，任选选一个即可：

### 方法一：VNC 登录

在服务器概要页，找到下述的 `VNC登录`，点击它。

![](https://docs.prsdev.club/rum-app/images/cloud_vnc.png)

现在，你通过本地的浏览器，可以看到你的云服务器的登入画面啦。

![](https://docs.prsdev.club/rum-app/images/cloud_login.png)

在左上角找到 `发送远程命令`，然后点击 `CTLD-ALT-DELET` 这个选项。右侧画面会展示一个 windows 电脑的登入窗口。

输入你的密码。也就是上面 `重置密码` 时，你所用到的密码。你有妥善保管好它，对吧？它很常用的。

登入成功后，你会被一个服务器管理窗口霸满屏幕，没关系，右上角点击 `x` 关掉它。

这时候，你可以看到你的云服务器桌面了。

以后你会经常通过该办法来访问和操作你的云服务器。

当你一段时间不操作会自动断开连接，提示是：`连接已断开，请刷新重试`，就关掉该网页，重新 `VNC 登录` 即可。

### 方法二：远程桌面登录（本地是 Windows 系统）

复制公网 IP，公网 IP 在服务器 `概要` 页 `网络信息` 板块查看，复制它：

![](https://docs.prsdev.club/rum-app/images/20211105181522.png)

开始菜单中找到 `运行` 打开（Win 10 可以用搜索输入 `run` 快速找到它）：

![](https://docs.prsdev.club/rum-app/images/20211105180431.png)

弹出窗口输入 `mstsc`，确定：

![](https://docs.prsdev.club/rum-app/images/20211105180713.png)

弹出窗口点击 `显示选项`：

![](https://docs.prsdev.club/rum-app/images/20211105204409.png)

接着在 `计算机` 后面，粘贴云服务器的公网 IP；`用户名` 后输入服务器的管理员帐号（默认是 `Administrator`）：

![](https://docs.prsdev.club/rum-app/images/2021-11-05_20-39-51.png)

然后转到 `本地资源`，点击 `详细信息`，展开 `驱动器`，选择一个盘（**这个选项非常好用，例如你选择了 F 盘，则链接到服务器后，F 盘本地和云端都可以用，可以随便复制、粘贴文件**），确定后点击 `链接`（两次）：

![](https://docs.prsdev.club/rum-app/images/2021-11-05_20-39-56.png)

弹出对话框选 `是`：

![](https://docs.prsdev.club/rum-app/images/20211105182626.png)

如此，您已经远程登录云服务器。将弹出的 `服务器管理器仪表板` 点击右上角 `x` 关掉，就进入桌面啦。

## 四、下载安装 RUM

下载安装 RUM 有两个办法，一个是直接云端打开浏览器下载安装；一个是本地下载好传给云端安装。任选一个方法即可：

### 方法一：云端浏览器下载安装

登录云服务器后，打开 IE 浏览器。云服务器已经自动安装了 IE 浏览器，且安全级别很高。使用推荐设置即可，点击确定。

![](https://docs.prsdev.club/rum-app/images/cloud_ie1.png)

终于出来了 IE 界面，鼠标选中地址栏的地址，清空它。

保持鼠标在地址栏输入框，然后点击上面的 `这里`。

![](https://docs.prsdev.club/rum-app/images/cloud_ie2.png)

在弹出的窗口粘贴 RUM 下载页的网址：https://docs.prsdev.club/#/rum-app/test

你会发现，地址栏会自动输入刚刚粘贴的网址。回车，会跳转到上述网页。

不过这是 IE 浏览器的安全模式会弹出各种窗口。

下面这种，点击 `添加`：

![](https://docs.prsdev.club/rum-app/images/cloud_ie3.png)

下面这种，点击 `添加` 后，点击 `关闭`。

![](https://docs.prsdev.club/rum-app/images/cloud_ie4.png)

就顺利打开 RUM 下载页的网址啦。

当你用 IE 浏览器访问其它网站也会遇到类似情况，麻烦点没关系，至少最大可能安全。

在 RUM 下载页，找到 windows 的安装包，点击，会触发下载。你会重复上述 IE 设置过程。直到 RUM 下载被顺利加载出来。点击 `保存` 的 `另存为`（三个选项任选一个都可以，另存为方便找到安装包），等待下载完。

![](https://docs.prsdev.club/rum-app/images/2021-11-05_18-50-43.png)

下载完后，双击安装包，云服务器会提示你 `.exe` 不安全，不用担心，继续往下操作，运行它，会安装好 RUM。

![](https://docs.prsdev.club/rum-app/images/20211105171627.png)

接下来就如同本地电脑一样使用 RUM 就可以啦。

如果 RUM 有新版本更新，就点击 RUM 检查更新，按提示更新和重启即可~

### 方法二：本地传给云端安装

该方法适合 `远程桌面登录`。

本地打开上述 RUM 的下载网址将安装包下载下来（**注意要下载到远程桌面登录时 `本地资源` 与远程共享的那个盘**）。

在远程桌面中打开资源管理器，再打开本地和远程同时共用的那个盘：

![](https://docs.prsdev.club/rum-app/images/20211105195827.png)

找到安装包复制到远程桌面上（也可以直接双击安装包安装，可能慢一点）：

![](https://docs.prsdev.club/rum-app/images/20211105203452.png)

复制完了，双击复制过去的安装包安装即可。

## 五、云服务器中 RUM 怎么玩？

你的云服务器上的 RUM 节点，在下面简称为 `云节点`。

### 0、创建节点

首次使用，在启动RUM后，选择 `创建节点`，选择文件夹就直接选择 C 盘即可。（也没别的盘可选嘛）

### 1、检查你的节点状态

如果你是 1.x 版本的 RUM，点击左上角的小人头像，找到 `网络状态` 可以查看到是 `public`。

如果你是 2.x 版本的 RUM，点击右上角的 `节点信息`，找到 `网络状态` 可以查看到是 `public`。

如果你的云节点不是 public，请联系娟娟咨询。

### 2、加入已有公开群组，为网络作贡献

建议你加入已有公开群组，为整个网络提供信息中转。

可在 RUM 的加入群组界面，找到 `有哪些公开群组可加入`，或直接在IE浏览器 https://docs.prsdev.club/#/rum-app/test 切换到种子文件，拷贝种子粘贴。

注意，拷贝文本时，最后面可能会多出来 `json` 几个字符，手动移除一下。

### 3、加入私有群组，帮忙中转

**所谓的私有群组，是你只想少部分人用，不想所有人都知道、都来用。**

如果你在本地创建了群组，可以让云节点加入它，这样，更多设备可方便访问该私有群组。

不过本地设备下线，就无法出块了。

### 4、创建私有群组，可 24H 在线出块

你可以直接在云节点创建群组，并把种子文件发给自己其它设备的节点来加入。


### 5、如何把云节点的文本，拷贝到本地电脑？

如果是 `远程桌面登录`，将远程文本复制、粘贴到共享的那个盘，本地就接收到了。

如果是 `VNC 登录`，有以下一些选择：

#### 5.1 无法 100% 确保保密（除了你，别人也会看到的）：

下面是一个仅有我们这些云节点加入和使用的私有群组，大家云端和本地都加入该群组，可以帮自己从云端转文本到本地。——你在这个群组发的文本，群组的其他人都可以看到。

```seed

{"genesis_block":
{"BlockId":"5780f238-cdb9-43ec-a219-46b2e19a7b37",
"GroupId":"0140aa1d-1898-4120-b1d5-37f51fb97d7c",
"ProducerPubKey":"CAISIQNdBCQunnrWJN41s8SUgg9RvsqUapOCNv1KVDnSZgKTBA==",
"Hash":"WV9o+10Fh/lrdAKu5piEUaF8p1OxzI6ZqaQffmFy5mU=",
"Signature":"MEYCIQDkOFEDjpmK5mnXOK47haHiR85jlluMDXSUDnNtb/NsNwIhAIvPnD/MiO7CXQl7co0NNO3t0twmKJ4wTznSAcPAj9ea",
"TimeStamp":"1636098449432113600"},
"group_id":"0140aa1d-1898-4120-b1d5-37f51fb97d7c",
"group_name":"我们在云端",
"owner_pubkey":"CAISIQNdBCQunnrWJN41s8SUgg9RvsqUapOCNv1KVDnSZgKTBA==",
"owner_encryptpubkey":"age1y4eetly0mu6j8lnhw5xufzju8zpf0gam4yhs6dykzcys2mpds4rs9g8pt5",
"consensus_type":"poa","encryption_type":"public",
"cipher_key":"5b9591ee881be8633cca9b20f99e9a29b0029f55bafa01d4726c23c3f1fa88f2",
"app_key":"group_timeline","signature":"30440220116d1880dcb7290a27d62802b5d6dc91ab64abd670ff3e1fa541c749fa38417a02202616aaa6e69cc11ed86d289377c24d61eab0112bf3f7e0f343fd560172b7219a"
}

```

#### 5.2 确保只有你自己可以看到的办法：

1) 用 IE 浏览器访问你的邮箱，在云端给自己发邮件，本地收邮件。

**建议注册新邮箱，专用于此类情况**。

2) 聊天工具也可以。云端开一个，本地开一个，就可以发文本和文件了。

比较灵活，大家各自发挥。

---

祝大家玩得愉快~！


---

## This's end.
