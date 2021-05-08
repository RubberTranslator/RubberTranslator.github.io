如果在使用过程中遇到任何问题，请**一定**在提问前，认真阅读本文档。

## 1. 问题汇总

### 1.1 如何安装/卸载本软件？

Win和Linux用户：

安装：本软件无需安装，在Github或蓝奏云下载压缩包，解压到**任意无中文路径**即可。

卸载: 删除解压包即可。

Mac用户：

安装：

**请一定提前打开允许任意安装来源**，如下：

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/rC1uw2kSIwh2DWmJpm-QUQ)

打开方法：

打开终端，执行 

```
sudo spctl --master-disable
```

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/JicS0XJIt7g2cj-aZl9Jvw)

然后下载dmg镜像，拖动RT到应用程序中即可。

卸载：

常规卸载方法即可。

下载地址：

Github：https://github.com/ravenxrz/RubberTranslator/releases

蓝奏云：https://ravenxrz.lanzous.com/b01bezbcf

### 1.2 如何启动本软件？

Windows端：点击解压包下的 Launcher.exe 即可。注意，如果解压在C盘，请使用管理员权限运行,其他盘则不需要。

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/nxCzlN2323xD64vuCdloSQ)

如果给予管理员权限？

右键，然后：

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/zCQjBkeoLj0_56En7E_U1A)

Linux端：使用终端进入bin目录下，然后运行Launcher即可。注意，如果没有可执行权限，请给予, 使用命令 chmod +x Launcher

Mac端：

找到RT图标，点击启动，**并给予辅助功能权限。**

### 1.3 为什么不能实现像视频中说的自动翻译？

确保基础设置中的**“拖拽复制”**和**“监听剪切板”**两个选项都已经打开。

### 1.4 可以使用QQ截图或者微信截图实现OCR吗？

可以使用任意截图软件，只要截图后保存在剪切板中即可，对于QQ截图，截图后点击√即可。

mac用户推荐使用snipaste，如果使用QQ截图，可能会出现 #fffxxx之类的文字, 这是因为QQ自带了取色器功能，这个功能和"拖拽复制"有点冲突。

### 1.5 截图了，为什么OCR没反应？

OCR需要自己手动配置，具体请参考：[这里](https://rubbertranslator.github.io/docs/config/index.html)

如果成功配置，在高级设置->Key&Secert设置->OCR中可以看到类似如图的界面：

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/N-4dcv75fhRd_QKsbbi-sg)

### 1.6 为什么不能使用百度翻译和有道翻译？

百度翻译和有道翻译需要自己手动配置，具体请参考：[这里](https://rubbertranslator.github.io/docs/config/index.html)

### 1.7 谷歌翻译无法使用？

有极少数同学会出现无法使用谷歌翻译，这种情况一般是因为你所在的校园网络无法访问谷歌翻译。打开浏览器，访问 [https://translate.google.cn/ ](https://translate.google.cn/) ，如果不能打开，说明你的网络无法确实无法访问。解决方法为切换电脑网络，如开手机热点给笔记本电脑使用。或者手动配置百度翻译或者有道翻译。

### 1.8 为什么完全无法翻译?

这个问题是1.6+1.7问题的合并，即你没有配置百度和有道，同时谷歌翻译也被禁用了。


### 1.9 如何设置字体大小，背景颜色？

**从v3.6.0开始** 
已支持GUI方式字体大小更改，目前暂不支持背景颜色更改。

通过高级设置->界面设置即可设置。
> Linux用户注意：部分Linux桌面环境可能会出现设置界面打不开，此时也可手动修改json配置下的 app_font_size 和 text_font_size 两个字段。

**v3.6.0 之前 (不包括v3.6.0)**
支持字体更改和背景颜色更改等。
设置字体大小略微复杂，首先在RubberTranslator/config目录下新建style.css文件，打开该文件，填入：

```css
.root{
	/* -fx-font-size: 10pt; */	
}

.text-area {
	/* 文本区相关设置 */
	/* -fx-font-size: 10pt; */
}

.text-area .content{
	/* 文本区背景颜色 */
    /* -fx-background-color: rgb(199,237,204); */
}
```

修改相应的font-size, 打开RubberTranslator，高级设置->自定义样式，在弹出的选择框中选择刚才新建的style.css文件。 最后重启软件即可。

**注意：每次修改style.css文件后，都需要重启软件； v3.2.1及其之前版本不支持compare标识修改；**

### 1.10 如何批量导入词组？

如果你有大量词组需要导入，一条条输入是非常慢的，此时可以使用 “批量导入” 功能，如下：

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/2oDX9LBI7mTbYwYES27m4g)

选中一个 txt 文件，这个 txt 文件存放的就是你的词组文件，具体格式为：

译文：替换文

每行一个词组。如：

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/570GuuSJQ_b-wa48qB2Qbw)代表两个词组，将缓存线替换为 cacheline, 将商店替换为 store。

另外，如果重复选择一个 txt 文件，添加可能会看到重复行，如：![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/Gmvvmvcc0DeK1ddzTU_16w)

**Rt会进行去重处理，只保留最旧的版本。**

### 1.12 如何手动更新？

一般情况下，RT可直接热更新，但部分情况下可能会出现热更新失败。这时需要用户自行手动更新：

打开蓝奏云：https://ravenxrz.lanzous.com/b01bezbcf

下载最新版，如：

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/fqM2fDx19ETpDdKg9cMNgg)![img](https://docimg2.docs.qq.com/image/rDD7Rns8m8goCWxE5dJTVQ?w=968&h=65)

最后全量替换到你之前的RT安装目录下即可。

### 1.13 剪切操作失效?

执行该操作，需要关闭【监听剪切板】和【拖拽复制】(仅在v3.5.0之后版本生效)


## 2. 私聊我

如果至此，依然无法解决问题，请加群私聊我。

QQ群号：118149802

一般私聊我，我都会让你上传一个log文件，log文件路径为

Win/Linux：

 RubberTranslator/log，会看到类似如下文件：

![img](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/jqNMPjSrO-ircWYAxpSYLw)

Mac:

在用户目录/log下：

![](https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/OcM1_U7tZfDxIcvyK8DkWQ.png)



选择当天日期的log文件发送给我。