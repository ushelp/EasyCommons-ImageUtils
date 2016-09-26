# EasyCommons-EasyImageUtils

---------------
EasyImageUtils 是 [EasyCommons](https://github.com/ushelp/EasyCommons "EasyCommons") 项目组下的图片处理组件。

## 1. API
EasyImageUtils 包括如下组件：

1. **EasyImageCompressionUtils**：图片大小压缩改变工具类，支持网络图片，等比，最大宽高等多种模式。 <br/>
 **适合场景**：上传图片时压缩到不同大小。 
 ```JAVA
  /**
  * 四种图片压缩方式：
  * - 按照最大宽度
  * - 最大高度
  * - 最大宽高
  * - 固定宽高
  * 
  * @param file 要压缩的源图片文件，支持path（字符串路径）和file（文件对象）作为参数
  * @param toFile 压缩后输出的文件，不指定则输出覆盖源文件，支持path（字符串路径）和file（文件对象）作为参数
  * @param maxWidth 要压缩的最大宽度，等比
  * @param maxHeight 要压缩的最大高度，等比
  * @param width 要压缩的固定宽度
  * @param height 要压缩的固定高度
  */
  compressPicByMaxWidth(file, [toFile], maxWidth);
  compressPicByMaxHeight(file, [toFile], maxHeight);
  compressPicByMaxWidthAndMaxHeight(file, [toFile], maxWidth, maxHeight);
  // widht或heigh为-1代表为width或height值为图片宽高
  compressPicByWidthAndHeight(file, [toFile], width, height);
 ```

2. **EasyImageSrcUtils**：图片地址提取工具类。将字符串内容中的图片路径提取出来。 
 
 **适合场景**：在发表新闻内容时，自动提取内容中所有的图片，或提取第一张图片作为新闻封面。 <br/>
 ```JAVA
  /**
  * 三种图片路径提取方式：
  * - 提取内容中的所有的图片src地址
  * - 提取内容中除了网络图片地址以外的所有图片src地址
  * - 提取第一幅图片的src属性值
  *
  * @param content 要提取图片地址的字符串内容
  */
  findAllSrc(content)
  findAllSrcNoNet(content)
  findFirstSrc(content)
 ```

3. **EasyImageWaterMarkUtils**：图片水印工具类。支持为图片添加图片水印或文字水印。 
 
 **适合场景**：上传图片时添加水印。 <br/>
 ```JAVA
  /**
  * 两种图片添加水印方式：
  * - 图片水印
  * - 文字水印
  * 
  * @param sourceImgFile 要添加图片水印的源文件，支持path（字符串路径）和file（文件对象）作为参数
  * @param waterImgFile 图片水印文件，支持path（字符串路径）和file（文件对象）作为参数
  * @param targetImgFile 生成带水印的图片文件，不设置，默认覆盖源文件，支持path（字符串路径）和file（文件对象）作为参数
  * @param content 要添加的文字水印内容
  */
 imageWatermark(waterImgFile, sourceImgFile [,targetImgFile]);
 textWatermark(sourceImgFile, content, [,targetImgFile])
 ```


## 2. Maven
```XML
<!-- EasyImageUtils -->
<dependency>
	<groupId>cn.easyproject</groupId>
	<artifactId>easycommons-image</artifactId>
	<version>1.4.2-RELEASE</version>
</dependency>
```


## 结束

[留言评论](http://www.easyproject.cn/easycommons/zh-cn/index.jsp#about '留言评论')

如果您有更好意见，建议或想法，请联系我。


联系、反馈、定制、培训 Email：<inthinkcolor@gmail.com>

<p>
<strong>支付宝钱包扫一扫捐助：</strong>
</p>
<p>

<img alt="支付宝钱包扫一扫捐助" src="http://www.easyproject.cn/images/s.png"  title="支付宝钱包扫一扫捐助"  height="256" width="256"></img>


[http://www.easyproject.cn](http://www.easyproject.cn "EasyProject Home")