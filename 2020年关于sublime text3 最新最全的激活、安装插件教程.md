# 2020年关于sublime text3 最新最全的激活、安装插件教程

### 前言介绍

写者是一个刚刚接触Web前端的小白，在学HTML时安装其IDE费了好多功夫，看了很多博客帖子，发现很少有最新的关于sublime text3的教程，所以在此写下sublime text3的激活、安装插件的教程。

### 教程篇

* **激活篇**

  首先软件的下载就不说了，直接搜索官网下载即可，安装过程一路next，这样软件就安装好了，也能使用。但是，这时你的软件并没有激活，激活需要在官网购花80美刀买注册码，我也是后来才知道的，你会发现未激活的软件顶部会有unregistered(未注册)。作为初学者我们当然选择白嫖：
  
	1. **首先可以查看我们软件的版本号：**
  
     菜单栏->help->about  sublime text，可以查看到你安装的软件版本，一般从官网下载的都是最新的，网上有很多教程局限于版本，但不要怕本教程不受限制。
  
  2. **注册码（软件激活码）：**
  
     激活软件很简单，只需要输入有效的注册码即可完美激活，但如果按照网上的教程操作，却出现下图所示的问题，软件依然没有激活。
  
  ​           ！[激活失败]( https://raw.githubusercontent.com/coder-zc/learngit/master/MDPhotos/1.png )
  
  3. **改hosts：**
  
     百度hosts文件的位置，用记事本或者notepad++打开编辑。加上下面这段代码：
  
     ```
     127.0.0.1    www.sublimetext.com
     127.0.0.1    sublimetext.com
     127.0.0.1    sublimehq.com
     127.0.0.1    license.sublimehq.com
     127.0.0.1    45.55.255.55
     127.0.0.1    45.55.41.223
     0.0.0.0     license.sublimehq.com
     ```
  
  4. **输入注册码：**
  
     一定要改一下hosts在输入注册码，否则可能失败。菜单栏->enter license,复制粘贴下列全部粘贴至打开的对话框。
  
     ```
     ----- BEGIN LICENSE -----
     Member J2TeaM
     Single User License
     EA7E-1011316
     D7DA350E 1B8B0760 972F8B60 F3E64036
     B9B4E234 F356F38F 0AD1E3B7 0E9C5FAD
     FA0A2ABE 25F65BD8 D51458E5 3923CE80
     87428428 79079A01 AA69F319 A1AF29A4
     A684C2DC 0B1583D4 19CBD290 217618CD
     5653E0A0 BACE3948 BB2EE45E 422D2C87
     DD9AF44B 99C49590 D2DBDEE1 75860FD2
     8C8BB2AD B2ECE5A4 EFC08AF2 25A9B864
     ------ END LICENSE ------
     ```
  
     接下来应该是显示激活成功，激活成功后可将之前hosts文件添加内容删掉，如下图所示：
  
     ！[激活成功]( https://raw.githubusercontent.com/coder-zc/learngit/master/MDPhotos/2.png )
  
  5. **设置软件不更新：**
  
     菜单栏->preferences->settings,在右侧代码框里添加下面这句代码
  
     ```
     "update_check":false
     ```
  
     注意添加的位置，我给出了示意图，不要忘了再上一句代码加上一个英文状态下的逗号：
  
     ！[效果图]( https://raw.githubusercontent.com/coder-zc/learngit/master/MDPhotos/8.png )
  
     

​               激活篇教程主要参考这篇帖子：[1]( http://blog.jdk5.com/zh/sublime-text-3-license-key/ )

​               这两篇也有参考价值：

​					[2]( https://cloud.tencent.com/developer/article/1545498 )

​					[3]( https://www.jianshu.com/p/b6fae22fee0f )



* **安装插件**

  你以为就这样完了吗？安装插件的问题真的非常多。但是插件的功能很强大啊，可以一键写出html代码框架，可以汉化等等。

  1. **失效的教程**
  
    话不所说，先上插件包的官方安装网址：[插件包安装网址]( https://packagecontrol.io/installation )。首先我们搞清楚我们是要下载一个插件包，是一个名字叫“Package Control”的文件,所有的插件都是通过插件包下载的。我们在网上看到的大多数教程，是复制一段代码在sublime text3的控制台输入即可下载，仔细看你会发现大多都是几年前的教程，而如今的插件包安装网址已经没有对应的选项，这该怎么办呢？
  
  2. **换一个教程：**
  
       不慌，我们还是打开前面的插件包网址，仔细阅读其内容，如果英文状态下有难度可以翻译网页，网页的大致意思是：提供了自动安装的方法和手动安装方法，自动方法虽然简单，但是在科学上网的前提下也没有反应，那我们只能采取手动的方法，按照网页上的教程一步步来应该没问题，将“Package Control”包下载放在Installed Packages/路径下 。当然如果你找不到 Installed Packages/ 的位置，大致在C:\Users\84139\AppData\Roaming\Sublime Text 3\Installed Packages（这与你软件的安装时设置的路径无关）。重启一下软件,菜单栏->preferences,弹出列表框出现有“ Package settings"、“Package Control”表示安装成功。
  
  3. **有可能还没结束：**
  
     菜单栏->preferences->Package Control,弹出的对话框如下图所示，则可以下载各自插件了。
  
     ！[这个状态可以下载插件]( https://raw.githubusercontent.com/coder-zc/learngit/master/MDPhotos/6.png )
  
  当然很多人可能会出现这个问题 “There Are No Packages Available For Installation” ,原因我们可以打开菜单栏->view->show console,控制台报错：
  
  ```
  Package Control: Error downloading channel. HTTP error 404 downloading https://packagecontrol.io/channel_v3.json.
  ```
  
  是无法下载channel_v3.json文件，我在科学上网状态下也报错。网上借鉴大佬们的解决方法，在官网下载channel_v3文件，[下载地址](https://packagecontrol.io/channel_v3.json) ，传到自己的GitHub上 。这里提供我的地址：就是下面代码方括号里的内容，你也可以换成你自己上传的地址。
  
  然后打开软件->菜单栏->preferences->Package settings->Package control->settings user,将下面的代码复制粘贴至打开的代码框里。显示效果如图：！[粘贴效果]( https://raw.githubusercontent.com/coder-zc/learngit/master/MDPhotos/9.png )

```
"channels":
	[
		"https://raw.githubusercontent.com/coder-zc/learngit/master/channel_v3.json"
	]
```

这样再打开菜单栏->preferences->Package Control就可以正常下载插件了。如果还出现了问题可以继续往下看。



4. **这个过程参考有用的博客**：

   [1]( https://www.jianshu.com/p/c2f41ef12834 )

   [2]( https://blog.csdn.net/zr15829039341/article/details/73136319 )



* **其他问题**

1. **问题一：**

   如图，手动安装package control 包时名字搞错了，必须严格是“Package Control”,大小写也要注意，注意不要有空格，我就犯了这个错误好半天没看出来。

​               ！[问题一报错图片]( https://raw.githubusercontent.com/coder-zc/learngit/master/MDPhotos/5.png )

2. **问题二：**

   安装emmet插件后报错，emmet插件可以快速写出html代码框架：！[报错图片]( https://raw.githubusercontent.com/coder-zc/learngit/master/MDPhotos/7.png )

​       解决方法这边博客已给出，亲测有效，点击[解决方法](https://blog.csdn.net/forAlienZHOU/article/details/53427093) 



### 总结篇

  没想到这个sublime text3的安装这么复杂，网上搜到的教程大多都是几年之前很多已经失效，而且总结不是很全面，于是我花了很多时间搜索和阅读，总结了软件的激活和插件的安装，这也是我为什么写这篇博客的原因，同时也是为了练习markdown的写作。如果以后遇到类似问题，还是需要不停的搜索，总会找到解决的方法。创作不易，如果对你有帮助，请点个赞，谢谢！