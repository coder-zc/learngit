#  Python 的IDLE打不开了？
PS：这是我第一次写博客。在配置PyQt 的环境过程中遇到了IDLE打不开的问题，并通过搜索csdn找到答案，中间试错了好几次都没有解决好，在于没有找到为什么打不开的原因。通过参考[夜风的博客](https://blog.csdn.net/k183000860/article/details/88712161)找到我的问题并解决了。
## 行文思路：
问题背景：
解决过程：
小结：

### 问题背景
先是下载了python3.7,运行都没有问题。接着下载Qt，PyQt。最后按照王伟波所著的Python Qt GUI与数据可视化编程的书中第10页的内容：在IDLE中开启对PyQT5的代码提示功能，对C:\Python37\Lib\idlelib下的文件config-extensions.def和autocomplete.py进行了相应的修改。

问题来了：当我打开python下的IDLE却怎么也没有反应，打不开？

**该教程适用于改了相关文件内容打不开的情况**


### 解决过程
于是乎我开始在CSDN上寻找解决方法，果然有类似的问题，经过仔细阅读后我开始尝试博主提供的方法：
有说是在命令窗口输入一个命令删除其中跳出来的文件；
有说是配置环境变量；
还有的说是重新安装一下python安装包点击Repair修复；
看到评论中有的说有用有的说还是不行，可我都试过没一个行的通的。因为到目前为止我还没有意识到我打不开的原因。
于是我看到了夜风的博客，意思到我之前修改了config-extensions.def和autocomplete.py的内容。于是按照他的操作运行了idle.py。
![,](https://img-blog.csdnimg.cn/20191225180219269.png?x-o首先ss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM2MDc0Mg==,size_16,color_FFFFFF,t_70)
win+R打开cmd终端：需要用到cd \ 目录名(返回到指定的目录文件下)、cd 目录名 （到达当前文件下一级目录），命令窗口在C:\Python37\Lib\idlelib>这个路径下运行 `python idle.py`命令，如果没有问题IDLE会被打开。可是现在打不开了，当然就有错误：我的就报错了如下图所示：（我对python报错的格式做了分析，帮助不会看错误的同学理一下）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191225182654440.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM2MDc0Mg==,size_16,color_FFFFFF,t_70)
于是我发现了在修改autocomplete.py文件中我把一个语句漏料了一个字母导致出错。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191225183330479.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM2MDc0Mg==,size_16,color_FFFFFF,t_70)
所以呀！在修改的过程中一定要仔细，然后我改完之后再在C:\Python37\Lib\idlelib>这个路径下运行 `python idle.py`命令，就没有问题了，IDLE可以正常打开了。
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019122518375978.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDM2MDc0Mg==,size_16,color_FFFFFF,t_70)
### 小结
1、解决问题要对症下药，不要盲目的应用教程的方法有可能并不适用。
2、第一次写博客，有点啰嗦大家见谅！