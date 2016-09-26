# EasyCommons-EasyImageUtils API

---------------

EasyImageUtils is [EasyCommons](https://github.com/ushelp/EasyCommons "EasyCommons") project group image processing component. 

## 1. API
EasyImageUtils includes the following components:

1. **EasyImageCompressionUtils**: change the image size compression tools, support network pictures, geometric, higher maximum wide variety of modes.
 **Scene** : compression to upload pictures of different sizes.
 ```JAVA
  /**
  * Four kinds of image compression:
  * - According to the maximum width
  * - According to the maximum height
  * - According to the maximum width and height
  * - According to the width and height
  * 
  * @param file To compress the source image files, support path (string path) and a file (file object) as a parameter
  * @param toFile After the output of the compressed file, do not specify the output file overwrite the source, support path (string path) and a file (file object) as a parameter
  * @param maxWidth To compress the maximum width, geometric
  * @param maxHeight To compress the maximum hieght, geometric
  * @param width To compress the maximum width and height, geometric
  * @param height To compress the width and height, geometric
  */
  compressPicByMaxWidth(file, [toFile], maxWidth);
  compressPicByMaxHeight(file, [toFile], maxHeight);
  compressPicByMaxWidthAndMaxHeight(file, [toFile], maxWidth, maxHeight);
  // widht or heigh -1 for the width or height values representative of image width and height
  compressPicByWidthAndHeight(file, [toFile], width, height);
 ```

2. **EasyImageSrcUtils**:Image address extraction tools. The string contents of the image path extracted.
 **Scene** : at the time of publication of news content, the content automatically extract all images, or extract the first image as a news cover.
 ```JAVA
  /**
  * Three kinds of picture path extraction method:
  * - Extract the contents of all the pictures src Address
  * - Extract the contents of the image in addition to the network address of photos src address
  * - Extract the first picture of the src attribute value
  *
  * @param content To extract the image address string contents
  */
  findAllSrc(content)
  findAllSrcNoNet(content)
  findFirstSrc(content)
 ```

3. **EasyImageWaterMarkUtils**:Image watermark tools. Support for the picture add a picture watermark or text watermark. 
 **Scene**: Add a watermark to upload pictures. 
 ```JAVA
  /**
  * Two kinds of way to add a watermark image:
  * - Picture Watermark
  * - Text watermark
  * 
  * @param sourceImgFile To add a picture watermark source files, support path (string path) and a file (file object) as a parameter
  * @param waterImgFile Image watermark files, support path (string path) and a file (file object) as a parameter
  * @param targetImgFile Produce image files with a watermark, do not set the default cover the source file, supporting path (string path) and a file (file object) as a parameter
  * @param content To add a text watermark content
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


## End

[Comments](http://www.easyproject.cn/easycommons/en/index.jsp#about 'Comments')

If you have more comments, suggestions or ideas, please contact me.

Email:<inthinkcolor@gmail.com>

[http://www.easyproject.cn](http://www.easyproject.cn "EasyProject Home")
