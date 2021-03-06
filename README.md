
**请先看 ChangeLog 了解最新变化**

## About

MarkDown 相信已经成为技术人员的写文档，博客的标配啦。

自然, 博客中经常要插入图片或者 GIF ，对于这些，我们经常选择七牛或者 LeanCloud 来作为图传。但这个过程也稍微有点繁琐，要打开浏览器，寻找图片路径，点击上传图片，复制 URL 。

利用 Python 的 Drop ， Handle 思想，写出了该脚本。如下 GIF 所示，你只需要将图片或者 GIF 拖动到脚本上，即可生成 MarkDown 格式 URL 在你 TXT 文档和你的黏贴板中，直接右键黏贴即可。省去了不少步骤。


## Install

四个配置参数的地方：

![markDownHelper2.png](http://7xrl8j.com1.z0.glb.clouddn.com/markDownHelper2.png)
![markDownHelper1.png](http://7xrl8j.com1.z0.glb.clouddn.com/markDownHelper1.png)

依次填入即可：

``` python
# you need get yours msg here
access_key = "XXXX"
secret_key = "XXXX"
bucket_name = 'XXXX'
bucket_url = 'XXXX'
```

## Steps

* 安装好 Python 环境。
* 安装七牛的 SDK pip install qiniu ，这个过程中你也需要安装一下 pip 这个工具。
* 完成上述步骤后，脚本默认的打开方式应该是 python，也就是脚本的图标应该是有 Python 标志的,也就是 Tips 中第二张图 MdHelper.py     那个样子。如果不是，请右击选择默认打开方式为 Python。
* 拖动图片到脚本上即可。
* 如果拖动没有反应，大家可以自己调试。在 CMD 窗口下找到脚本**所在的路径**如我的脚本在 C:\Users\allen\Desktop\MDHelper 那么我打开 CMD 后 cd C:\Users\allen\Desktop\MDHelper，接着输入 python MarkDownHelper.py 即可。报错信息在 CMD 窗口都能看得到。

## Tips

最后建议你们这样来使用这个脚本：在桌面上新建一个文件夹:MdHelper,把所有截图和脚本都可以放在这个文件夹内。**拖动图片到脚本上即可**。

另外，图片的命名不要是中文，因为你中文托上去好像没有反应。

## Usage

![MarkDownHelper3.gif](http://7xrl8j.com1.z0.glb.clouddn.com/MarkDownHelper3.gif)

## ChangeLog

*  in 1.0 version,你可以在上传成功后,在生成的 txt 文档中复制 MarkDown URL
*  in 1.1 version,将最近上传的图片 URL，保存在黏贴板中，你也可以直接黏贴到你的 MarkDown 编辑器中。 
*  in 1.2 version，这个版本支持私有空间哦。具体你可以看 mdScript2.py 这个脚本。只需要黏贴一点代码到 MarkDownhelper.py 中即可。
*  in 1.3 version,在1.3 版本中，增加了删除本地文件图片的功能。这个功能很好用，因为文件夹中图片越来越多，你也看着不爽。不过删除是从系统     中删除哦，意味着，回收站内也没有。当然，如果你不想要这个功能，注释 MarkDownHelper 一句代码即可。
*  in 1.4 version,这个版本我在如下平台测试了: win7,win10,Ubuntu。
*  in 1.5 version,增加了压缩图片的功能，因为七牛云免费容量有限。利用 tinyPNG     的图片压缩功能压缩图片至原图的三分之一。但是带来的影响就是图片拖动反应变慢。所以这个版本是一个选择版本，你可以在 markDownHelper2.py 中选择使用该功能。[TinyPNG 的 API 文档](https://tinypng.com/developers/reference/python)

## Thanks

脚本的灵感来源:[laobie's WriteMarkdownLazily](https://github.com/laobie/WriteMarkdownLazily),感谢。

## License

MIT





