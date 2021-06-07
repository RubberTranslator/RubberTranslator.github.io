## 0. 视频介绍

<iframe id="spkj" src="//player.bilibili.com/player.html?aid=800861081&bvid=BV1Wy4y1e7HG&cid=271513284&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width=100%> </iframe>
<script type="text/javascript">  
document.getElementById("spkj").style.height=document.getElementById("spkj").scrollWidth*0.76+"px";
</script>

## 1. 基础功能

### 1.1 手动翻译

作为翻译软件最基础的功能，RubberTranslator 也是支持手动翻译的，如：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/oRsHcgsqvQ.gif" style="zoom: 80%;" />

### 1.2 翻译引擎选择&源/目标语言设置

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/S24b0bnOaP.gif" style="zoom: 80%;" />

默认支持，谷歌翻译，百度翻译和有道翻译。（百度和有道翻译需要配置 API 信息才可以使用，详情可参看：[ocr,百度，有道配置](https://github.com/ravenxrz/RubberTranslator/wiki/OCR%EF%BC%8C%E7%99%BE%E5%BA%A6%E5%92%8C%E6%9C%89%E9%81%93%E9%85%8D%E7%BD%AE)

### 1.3 文本格式化

文本格式化是用来做什么的呢？我们平常在阅读 pdf 文档的时候，经常有这样的一个问题，从 pdf 中拷贝的文本粘贴到其它地方会多出很多换行，如：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/image-20200515203036559.png" style="zoom:80%;" />

可以看到，因为多出很多空行，翻译会变得非常的不准确，一般来说，我们会手动替换掉所有的换行符，RubberTranslator 默认开启”文本格式化“功能，可以用来解决问题，在替换掉换行符的同时，**尽量保持分段格式**，功能展示：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/HpgwWgEwNd.gif" style="zoom:80%;" />

### 1.4 监听剪切板

开启监听剪切板功能，只要 PC 剪贴板中有新文本或图片时，RubberTranslator 会自动翻译，也就是说只要有”复制“(Ctrl+C 或鼠标复制）动作，RubberTranslator 就会复制。如：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/iasVDY9BIQ.gif" style="zoom:80%;" />

### 1.5 拖拽复制

每次都手动进行复制显得过于麻烦，所以拖拽复制可以实现自动复制，拖拽复制在以下两种情况下会触发：

1. 鼠标双击；
2. 鼠标点击->移动一定距离->释放。如果移动距离过近，则不会触发复制。

配置监听剪切板功能，即可实现自动翻译。演示：

双击：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/bG2PZ7pfaF.gif" style="zoom:80%;" />

拖拽：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/94VVcyPHtK.gif" style="zoom:80%;" />

### 1.6 自动复制

自动复制用于自动复制译文，RubberTranslator 在翻译完一段文本后，会自动将译文文本放入到系统剪切板中，此时用户通过"粘贴"功能即可在任何地方输入译文了。

> tips: v3.6.3 后，可自动复制 OCR 原文，使用方法为，将"翻译引擎"改为"none"即可。

### 1.7 自动粘贴

自动粘贴用于就地替换原文，如下：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/mYHGWcR1eQ.gif" style="zoom:80%;" />

### 1.8 增量复制

增量复制用于解决阅读过程中，”文本翻页“的情况，如：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/AncXUT56Pq.gif" style="zoom:80%;" />

### 1.9 OCR 翻译

对于一些无法复制的 pdf 文本，可以通过 ocr 进行翻译，如：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/vI26MTVGa3.gif" style="zoom:80%;" />

ocr 功能需要配置百度 ocr api key。[ocr,百度，有道配置](https://github.com/ravenxrz/RubberTranslator/wiki/OCR%EF%BC%8C%E7%99%BE%E5%BA%A6%E5%92%8C%E6%9C%89%E9%81%93%E9%85%8D%E7%BD%AE)

### 1.10 历史记录

RubberTranslation 也支持历史记录。

### 1.11 专注模式

专注模式只保留译文，整体布局更为紧凑，适合在阅读论文时使用。

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/image-20200515211515270.png" style="zoom:80%;" />

### 1.12 对比模式

同时展示多种翻译引擎翻译结果。

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/123.gif" alt="123" style="zoom:80%;" />

### 1.13 记录模式

该模式下，会记录所有翻译文本，并导出原文、译文或双语的文档。 用于导出翻译文献非常有用。

[<img src="https://camo.githubusercontent.com/38a05132a190b375934f48376f7e10d7ce672499c94da96b363e28ac7646c512/68747470733a2f2f696d672e696d6764622e636e2f6974656d2f3630323132363532336666613764333762336162653861612e6a7067" alt="image-20210204152707436" style="zoom:80%;" />](https://camo.githubusercontent.com/38a05132a190b375934f48376f7e10d7ce672499c94da96b363e28ac7646c512/68747470733a2f2f696d672e696d6764622e636e2f6974656d2f3630323132363532336666613764333762336162653861612e6a7067)

### 1.14 翻译接力

一直使用同一个翻译引擎时，可能会出现翻译失败的情况，在这种情况下，RubberTranslato 会自动选择下一个翻译引擎进行翻译。

## 2. 高级设置

### 1. 过滤器

此功能暂时仅限 Widnows 平台。

过滤器用于设置不需要进行复制翻译的程序，考虑一个场景，在看论文时，我们需要在浏览器中搜寻一些资料，但是我们并不需要自动翻译浏览器中的内容，这时就可以将浏览器加入我们的过滤名单中。

操作：高级设置->过滤器,点击添加，找到浏览器的 exe 文件(快捷方式也可以）即可：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/image-20200515211034440.png" style="zoom:80%;" />

### 2. 翻译文本替换

这个功能用于将译文中的特定词组替换为自己想要的词组，可以用于替换为专有名词。举个例子，在计算机数据结构或算法上，有一个术语叫做 binary search，一般中文称为二分查找，而使用翻译引擎翻译，则会被翻译为二进制搜索，这让人非常的别扭。通过”翻译文本替换“功能，我们可以还原为二分查找。

先看，没有添加词组前：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/Gu9OkaJ3Q8.gif" style="zoom:80%;" />

再看添加词组后：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/MD3Q6XYcnu.gif" style="zoom:80%;" />

**支持 java 正则表达式。**

### 3. 翻译文本批量导入

如果你有大量词组需要导入，一条条输入是非常慢的，此时可以使用“批量导入”功能，如下：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/image-20210122095723696.png" alt="image-20210122095723696" style="zoom:67%;" />

选中一个 txt 文件，这个 txt 文件存放的就是你的词组文件，具体格式为：

```
译文：替换为
```

每行一个词组。

如：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/image-20210122095855003.png" alt="image-20210122095855003" style="zoom: 67%;" />

代表两个词组，将缓存线替换为 cacheline, 将商店替换为 store。

另外，如果重复选择一个 txt 文件，添加可能会看到重复行，如：

<img src="https://img.imgdb.cn/item/600a32133ffa7d37b3e4c0c6.png" alt="image-20210122100023609" style="zoom: 67%;" />

**RubberTranslator 只会选择其中一组保存。**

### 4. 历史记录数量设置

可以设置历史记录的数量，但注意历史记录在程序关闭后就会消失，每次重启应用都会重新记录历史。

### ~~5. 自定义样式~~

**自 v3.6.0 开始，取消本功能。** 改用 GUI 设置。

~~RubberTranslator 支持自定义 css 样式。 如，设置护眼模式，更改字体大小的 css：~~

```css
#main {
  /* 主模式 */
  -fx-font-size: 10pt;
}

#focus {
  /* 专注模式 */
}

#compare {
  /* 对比模式 */
}

.text-area {
  -fx-font-size: 10pt;
}

.text-area .content {
  -fx-background-color: rgb(199, 237, 204);
}
```

效果：

<img src="https://cdn.jsdelivr.net/gh/ravenxrz/PicBed/img/image-20200515212539191.png" style="zoom:67%;" />

更多可设置效果，请参考

[javafx css](https://docs.oracle.com/javafx/2/api/javafx/scene/doc-files/cssref.html)

### 6. OCR 百度和有道 APi 设置

[ocr,百度，有道配置](https://rubbertranslator.github.io/docs/config/index.html)

## 3. 开源许可

GPL v3.0
